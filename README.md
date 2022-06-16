# jicli
```
JiCli v0.1 (untested alpha) -  Jojo's IDrive CLI  - Copyright (C) 2022 Joris Heirbaut GPL

JiCli is free software: you can redistribute it and / or modify it under the terms of the
GNU General Public License as published by the Free Software Foundation, either version 3
of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful,  but WITHOUT ANY WARRANTY
without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program
If not, see www.gnu.org/licenses/gpl-3.0

usage: jicli [-hvv] [-d <udir>] [-i <idir>] [-u <usr>] [-l <lusr>] [<command> [<arg>...]]
flags:
  -h    show help and exit
  -v    be verbose
  -vv   be very verbose
  -d    set idrive user directory (default /<idir>/idriveIt/user_profile/<lusr>/<usr>)
  -i    set idrive directory (default: /opt/Idrive)
  -u    set idrive user (default $IDRIVE_USR, ex. -u me@mymail.be)
  -l    set local  user (default $USER, ex. -l root or -l jojo :-)
commands:
  pgs|progress              show backup progress (default)
  enc|encode [<data>]       encode data or stdin
  dec|decode [<data>]       decode data or stdin
  set [<var> [<value>]]...  set configuration var(s) to value(s)
  get [<var>] [<var>]...    get configuration var(s)
examples:
  export IDRIVE_USR=me@mymail.be        ifirst set idrive username
  jicli                                 show backup progress
  cat CONFIGURATION_FILE | jicli dec    decode configuration file
  jicli set bwthrottle 50               set BWTHROTTLE to 50 in configuration file 
```
  
