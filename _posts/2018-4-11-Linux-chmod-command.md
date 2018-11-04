---
layout: post
title:  'Linux chmod Command'
date:   '2018-11-04'
categories: stories
tags: ['chmod', 'linux' ]
comments: true
---
I was Installing Jenkins from https://pkg.jenkins.io/debian-stable/ <br>

This is the Debian package repository of Jenkins to automate installation and upgrade. To use this repository, first add the key to your system: <br>

1) wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -<br>
Then add the following entry in your <strong>/etc/apt/sources.list:</strong><br> 

2) deb https://pkg.jenkins.io/debian-stable binary/ <br>
Update your local package index, then finally install Jenkins: <br>

3)sudo apt-get update <br>
sudo apt-get install jenkins

I was stuck at the 2nd Step while adding entry in /etc/apt/sources.list: due to Permission issue , so we will have to use  <strong>chmod</strong> command to change permissions of file : 

<div class="image">
    <a href="/public/img/permissionprob.png">
        <img alt="Permissions Problem" tab" src="/public/img/permissionprob.png" />
    </a>
</div>

<div class="image">
    <a href="/public/img/Permission Prob2.png">
        <img alt="Permission Problem" tab" src="/public/img/Permission Prob2.png" />
    </a>
</div>

So checking with <strong>ls -l</strong> command we can check the permissions of file :

<div class="image">
    <a href="/public/img/ls -l.png">
        <img alt="ls -l" src="/public/img/ls -l.png" />
    </a>
</div>

Here comes the role of <strong>chmod</strong> command <br>

chmod is used to change the permissions of files or directories.
On Linux and other Unix-like operating systems, there is a set of rules for each file which defines who can access that file, and how they can access it. These rules are called file permissions or file modes. The command name chmod stands for "change mode", and it is used to define the way a file can be accessed.
In general, chmod commands take the form:
chmod options permissions file name

Let's say you are the owner of a file named myfile, and you want to set its permissions so that:

    1)the user can read, write, ande xecute it;
    2)members of your group can read ande xecute it; and
    3)others may only read it.

This command will do the trick:
chmod u=rwx,g=rx,o=r myfile

This example uses symbolic permissions notation. The letters u, g, and o stand for "user", "group", and "other". The equals sign ("=") means "set the permissions exactly like this," and the letters "r", "w", and "x" stand for "read", "write", and "execute", respectively. The commas separate the different classes of permissions, and there are no spaces in between them.

Here is the equivalent command using octal permissions notation:

chmod 754 myfile

Here the digits 7, 5, and 4 each individually represent the permissions for the user, group, and others, in that order. Each digit is a combination of the numbers 4, 2, 1, and 0:

    4 stands for "read",
    2 stands for "write",
    1 stands for "execute", and
    0 stands for "no permission."

Now changing the Permission of source.list.save from command :
sudo chmod 777 source.list.save :
we have read write and execute permissions for user , group and other user 

<div class="image">
    <a href="/public/img/chmod.png">
        <img alt="ls -l" src="/public/img/chmod.png" />
    </a>
</div>

