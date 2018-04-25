---
title: "Moons"
date: 2018-03-28T22:07:15-04:00
weight: 20
---

The Debian GNU/Linux servers known as collectively as "the moons" make up the departments main computing environment. When connecting to moon.scs.ryerson.ca, you will connect to either Elara, Thebe, Europa or Metis.

## Logging In

### Linux or macOS

Students running a unix-like operating system can log into the moons server simply by using the ssh command from your terminal.

```bash
ssh [user name]@moon.scs.ryerson.ca
```

Where [user name] is the username you use to log into DCS computers.

You will be prompted for your password, this is the same password you use to login to CS lab machines, as well as your [department mail](/facilities/mail). If you would like to bypass entering your password in every time, you can generate SSH keys for your account.

#### SSH Config

Using the SSH config file is an elegant way of storing SSH connections, including host, username, key paths and other SSH connection options.

The command below will create the config file for you, if it does not already exist.A

```bash
touch ~/.ssh/config
```

Populate the created file with the following information.

```
Host ryerson
    HostName moon.scs.ryerson.ca
    User [user name]
```

Subbing in your moon username into the file will allow you to use the following command to login:

```bash
ssh ryerson
```

The SSH config file is quite powerful for other purposes such as fowarding ports and setting up proxy jumps. The latter of which is useful in CPS510 for accessing the class database from behind the department firewall.

### Windows

Students running Windows must use a separate application such as [PuTTY](https://www.putty.org) or [SSH Secure Shell Client](http://sils.unc.edu/it-services/servers/using-ssh).
