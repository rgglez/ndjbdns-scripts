# ndjbdns-scripts

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
![GitHub all releases](https://img.shields.io/github/downloads/rgglez/ndjbdns-scripts/total) 
![GitHub issues](https://img.shields.io/github/issues/rgglez/ndjbdns-scripts) 
![GitHub commit activity](https://img.shields.io/github/commit-activity/y/rgglez/ndjbdns-scripts)
![GitHub stars](https://img.shields.io/github/stars/rgglez/ndjbdns-scripts?style=social)
![GitHub forks](https://img.shields.io/github/forks/rgglez/ndjbdns-scripts?style=social)

Some scripts for performing administrative tasks for [ndjbdns](https://github.com/dterweij/ndjbdns). 

ndjbdns is a fork of the great djbdns (Tiny DNS) DNS server (which was abandoned some years ago). From the ndjbdns repo:

"Djbdns is a fully-fledged Domain Name System(DNS), originally written by the eminent author of qmail, Dr. D J Bernstein. This new release is a complete makeover to the original source(djbdns-1.05) and is meant to make life a lot more pleasant. The original source is in public-domain since late Dec 2007."

## Scripts

* **Makefile** - includes these rules:
     * *data.cdb* - creates a backup, creates the data text file from the zone files.
     * *backupdata* - moves the old data file to a backup directory.
     * *data* - creates the data text file from the zone files.
     * *remote* - executes *data.cdb* and copies the data fiel to a secondary DNS server using rsync over ssh.
     
  You'll need to modify the paths.
     
## Dependencies

This works in Linux. I think that it works in FreeBSD and other OS too, as long as you have the programs.

* [ndjbdns](https://github.com/pjps/ndjbdns) (of course)
* [make](https://en.wikipedia.org/wiki/Make_(software))
* [rsync](https://en.wikipedia.org/wiki/Rsync)
* ssh

## License

Copyright (c) 2003, Rodolfo González González.

Read the LICENSE file.
