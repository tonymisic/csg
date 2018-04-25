---
title: "SSH Keys"
date: 2018-03-28T22:23:06-04:00
weight: 10
---

SSH Keys are a method of method of authenticating trusted computers without the use of passwords. With SSH Keys, you will be able to SSH into servers without having to enter a password in every time.

## Generating SSH Keys

### Linux or macOS

Generating SSH keys is simple in unix-like operating systems.

In the terminal, execute the following commands

#### Generate Key

```
$ ssh-keygen -t rsa
Generating public/private rsa key pair.
```

Using the above command will generate a 2048 bit rsa key pair.

```
$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
Generating public/private rsa key pair.
```

If you plan on using your keys with Github, or other services, it would be useful to add your email address to your key using the -C flag. The -b 4096 flag above specifies to create a 4096 bit key.

#### Save Key

```
Enter file in which to save the key (/home/you/.ssh/id_rsa):
```

For simplicity, pressing enter will save the key in its default location.

#### Enter Passphrase

```
Your identification has been saved in /home/you/.ssh/id_rsa.
Your public key has been saved in /home/you/.ssh/id_rsa.pub.
The key fingerprint is:
a9:36:01:90:a5:8b:3e:50:ff:18:c0:be:71:a1:f2:28 you@localhost
```

Entering a passphase will hamper use of your key by others should it become compromised (unattended computer, theft of key).

### Windows

RSA Keys can be generating using [PuTTYgen](http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html).

## Using SSH Keys

When generating SSH keys, two files are created, one contains your private key, and the other contains your public key. Your public key is what you use on other servers to authenticate your computer. In the above tutorial, this is the id_rsa.pub file.

### Adding SSH Keys to DCS Moon Server

In order to log into the DCS Moon servers without entering your password, you have to add your public key to the ~/.ssh/authorized_keys file. Here are step by step instructions:

```
$ mkdir ~/.ssh
$ touch ~/.ssh/authorized_keys
$ nano ~/.ssh/authorized_keys
```

In the text editor of your choice, paste the contents of id_rsa.pub into the file, and then exit and save changes. Log out of the Moon server and log back in to verify your SSH keys were set up properly.
