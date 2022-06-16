# Jojo's IDrive Backup CLI

Small utility for following the progress of IDrive Backup for Linux, allowing to modify the bandwith percentage without need to connect to IDrive's Web Dashboard.
```
JiCli v0.1 (untested alpha) - Jojo's IDrive CLI - Copyright (C) 2022 Joris Heirbaut GPLv3

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
  export IDRIVE_USR=me@mymail.be        set idrive username
  jicli                                 show backup progress
  cat CONFIGURATION_FILE | jicli dec    decode configuration file
  jicli set bwthrottle 50               set BWTHROTTLE to 50 in configuration file 
```

Example output:
```
1 mnt/mydrive/dv/year.07.14 Veerse meer/dv.zzzzzz.07.avi:      100%    152Mb 140.21kB/s 2115/4820  0:18:30 
1 mnt/mydrive/dv/year.07.18-01 Champagny/dv.zzzzzz.00.avi:     100%    149Mb 121.95kB/s 2265/4820  0:20:57 
2 [connection established]
2 [building file list ...]
1 mnt/mydrive/dv/year.07.18-01 Champagny/dv.zzzzzz.16.avi:      76%    149Mb 120.75kB/s 2380/4820  0:04:58 
2 mnt/mydrive/dv/year.03.27 Bi...Linkeroever/dv.zzzzzz.24.avi: 100%    158Mb 150.38kB/s  158/4916  0:17:57 
2 mnt/mydrive/dv/year.04 Firenze/dv.zzzzzz.12.avi:             100%    157Mb 151.35kB/s  315/4916  0:17:45 
2 mnt/mydrive/dv/year.04 Firenze/dv.zzzzzz.05.avi:             100%    159Mb 151.80kB/s  475/4916  0:17:56 
2 mnt/mydrive/dv/year.04 Firenze/dv.zzzzzz.01.avi:             100%    156Mb 151.39kB/s  632/4916  0:17:41 
2 mnt/mydrive/dv/year.04 Firenze/dv.zzzzzz.07.avi:             100%    160Mb 153.25kB/s  793/4916  0:17:55 
2 mnt/mydrive/dv/year.04 Firenze/dv.zzzzzz.05.avi:             100%    161Mb 152.26kB/s  954/4916  0:18:03 
2 mnt/mydrive/dv/year.07.19-31 Champagny/dv.zzzzzz.21.avi:     100%    157Mb 153.49kB/s 1111/4916  0:17:29 
2 mnt/mydrive/dv/year.07.19-31 Champagny/dv.zzzzzz.02.avi:     100%    159Mb 147.07kB/s 1271/4916  0:18:33 
2 mnt/mydrive/dv/year.12.25-07...y &amp; mna/dv.zzzzzz.05.avi: 100%    158Mb 122.46kB/s 1430/4916  0:22:04 
2 mnt/mydrive/dv/year.04.08 Paasklokken/dv.zzzzzz.30.avi:      100%    161Mb 123.76kB/s 1591/4916  0:22:15 
2 mnt/mydrive/dv/year.04.13 Aa... &amp; uiop/dv.zzzzzz.08.avi: 100%    154Mb 124.25kB/s 1745/4916  0:21:10 
2 mnt/mydrive/dv/year.05.26 Communie xxxx/dv.zzzzzz.19.avi:    100%    160Mb 137.23kB/s 1905/4916  0:19:56 
2 mnt/mydrive/dv/year.07.18-01 Champagny/dv.zzzzzz.02.avi:     100%    161Mb 122.53kB/s 2067/4916  0:22:27 
2 mnt/mydrive/dv/year.07.18-01 Champagny/dv.zzzzzz.12.avi:      33%    158Mb 121.89kB/s 2120/4916  0:15:02
----------------------------------------------------------------------------------------------------------
GPLv3 h:help q:quit +/-:change bw=40 Tft=58/1932GB Quota=938/5000GB                                0:12:51
```
