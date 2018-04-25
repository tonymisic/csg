---
title: "Printing"
date: 2018-03-28T22:07:49-04:00
weight: 50
---

There are printers located in labs ENG202 and ENG206. These printers are accessible to students locally through lab computers, and remotely through the moon servers.

All Ryerson computer science students receive $60 printing credit, which lets students print up to 5000 pages.[1] Additional credit can be purchased through the DCS by visiting during department office hours.

## Printing Remotely

Documents can be printed remotely through the moon servers using the lpr command.

Running any of the following commands while SSH'd into a moon server will print the provided file.

```
lpr -Peng202 [ file ... ]
lpr -Peng202-single [ file ... ]
lpr -Peng206 [ file ... ]
lpr -Peng206-single [ file ... ]
```

### Checking Print Queue

The ```lpq``` command can be used to check the contents of the print queue.

```shell
lpq [ -P destination ] [ -l ] [ + [ interval ] ] [ request-ID ] [ user ] 
```

### Cancelling Print Job

The ```lprm``` command is used to remove print jobs from the print queue.

```shell
lprm [ -P destination ] [ - ] [ request-ID ... ] [ user ... ] 
```

---
See also, [Printing from UNIX/Windows: User Guide to DCS Facilities](http://www.cs.ryerson.ca/user_guide.php#a35).