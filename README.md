# SSH Manager

A simple SSH manager in Python because I'm lazy. Your private key must be on the server via `ssh-copy-id` or another method.

# Install

Simply make the Python file an executable via `chmod +x ssh-manager`

# Usage

## General Help Output

```bash
./ssh-manager -h
usage: ssh-manager [-h] {connect,list,create,delete} ...

positional arguments:
  {connect,list,create,delete}
                        actions
    connect             Connect to a connection
    list                List connections
    create              Create a connection
    delete              Remove a connection

optional arguments:
  -h, --help            show this help message and exit
```

## Connect Output

```bash
./ssh-manager connect
Choose a connection:
1) tyler-king@host-name.com
2) ilove@domain.com

Use: [number-here]
```

## List Output

```bash
./ssh-manager list
1) tyler-king@host-name.com
2) ilove@domain.com

There are 2 connections on file
```

## Create Help Output

```bash
./ssh-manager create -h
usage: ssh-manager create [-h] --host HOST --username USERNAME

optional arguments:
  -h, --help           show this help message and exit
  --host HOST          The SSH host IP or domain name
  --username USERNAME  THe SSH username
```

## Delete Output

```bash
./ssh-manager delete -h
usage: ssh-manager delete [-h] [--host HOST] [--username USERNAME]

optional arguments:
  -h, --help           show this help message and exit
  --host HOST          The SSH host IP or domain name
  --username USERNAME  THe SSH username
```

```bash
./ssh-manager delete
Choose a connection:
1) tyler-king@host-name.com
2) ilove@domain.com

Delete: [number-here]

Success: ilove@domain.com has been deleted.
```