---
title: "Mail"
date: 2018-03-28T22:07:42-04:00
weight: 40
---

As a computer science student, you have a central @ryerson.ca email address, as well as an @scs.ryerson.ca email address through the Department of Computer Science. This email is tied to your SCS account on the moons. It is where all department announcements get sent, and is required to get access to your VMWare and Microsoft Dreamspark accounts.

## Logging In

Your scs email address uses the same login name and password as your account on the Computer Science Moons. You can access scs email by going to the [DCS home page](http://www.cs.ryerson.ca/) and clicking the ["scs web mail"](https://webmail.scs.ryerson.ca/src/login.php) link on the top of the page.

## Forwarding Your Mail

Instead of manually checking your DCS mail through its web interface, you can forward it to another email account. It is recommended to send it to your Ryerson email account.

To forward your CS email to the email account of your choice, you need to make a .forward file in your home directory with 644 permissions. Your home directory must have 711 permissions as well. In the .forward file you list all the email addresses you wish to forward your email to, one per a line.

### Instructions

SSH into one of the [Moons](/facilities/moons/) server, or log into linux on any of the lab machines and execute the following commands.

```
cd ~
chmod 711 ~
touch .forward
chmod 644 .forward
nano .forward
```

In the open file, list the emails you want to forward mail to (one per line), and then exit and save the program by pressing CTRL+X and then type "y". You should now have your emails forwarded to the email addresses you have listed in there.

## Using DCS Mail Through a Mail Client

{{% notice info %}}
You must be in the DCS network (either physically or through VPN) in order to send and receive email through a mail client.
{{% /notice %}}

DCS Mail can be accessed through e-mail clients on personal computers.

- Outgoing Server: smtp.scs.ryerson.ca
- Incoming Server: imap.scs.ryerson.ca (SSL Port 993)
- Username: Your DCS username
- Password: Your DCS password