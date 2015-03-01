wifi
====
wifi is a minimal and secure wifi network manager using GnuPG for password encryption.

## Requirements
 * python 3.4: https://www.python.org/
 * python-gnupg: https://pypi.python.org/pypi/gnupg/
 * requests: https://pypi.python.org/pypi/requests

## Features
* Connect to a list of predefined networks
* Add or delete networks
* Password encryption via GnuPG
* Aliases (for quick use)
* scan for available AP (coming soon)

## Usage
First, you have to init all the necessary stuff (folders, database file, GnuPG key) using the _init_ argument.
```sh
$ wifi -h
usage: wifi [-h] [-v] {add,connect,delete,init,list} ...

$ wifi init
Directory structure: done
Database: done
GnuPG: done

$ wifi add ACCESS_POINT1
Network password:
Access point ACCESS_POINT1 addedd successfully

$ wifi add ACCESS_POINT2 10.0.0.5 255.255.255.0 10.0.0.1
Network password:
Access point ACCESS_POINT2 addedd successfully

$ wifi list
1) ACCESS_POINT1
2) ACCESS_POINT2

$ sudo wifi connect ACCESS_POINT1
Connected to ACCESS_POINT1

$ sudo wifi connect 2
Connected to ACCESS_POINT2

$ wifi delete ACCESS_POINT1
Access point ACCESS_POINT1 deleted sucessfully
```

## Note
This script is a first draft/experiment around Python and it will be
certainly improved in a near future. It only intend to work on ipv4
networks, but you can quickly improve that if you need to. Thanks to 
my friend Tamentis for his help on this little project.
