# smbclient
[Back to cyber security page](../index.md)

---

## What is smbclient?
ftp-like client to access SMB/CIFS resources on servers

---

## Options
Usage: smbclient service password

```bash
  -R, --name-resolve=NAME-RESOLVE-ORDER     Use these name resolution services only
  -M, --message=HOST                        Send message
  -I, --ip-address=IP                       Use this IP to connect to
  -E, --stderr                              Write messages to stderr instead of stdout
  -L, --list=HOST                           Get a list of shares available on a host
  -m, --max-protocol=LEVEL                  Set the max protocol level
  -T, --tar=<c|x>IXFvgbNan                  Command line tar
  -D, --directory=DIR                       Start from directory
  -c, --command=STRING                      Execute semicolon separated commands
  -b, --send-buffer=BYTES                   Changes the transmit/send buffer
  -t, --timeout=SECONDS                     Changes the per-operation timeout
  -p, --port=PORT                           Port to connect to
  -g, --grepable                            Produce grepable output
  -q, --quiet                               Suppress help message
  -B, --browse                              Browse SMB servers using DNS
```

- Help options:
```bash
  -?, --help                                Show this help message
      --usage                               Display brief usage message
```

- Common samba options:
```bash
  -d, --debuglevel=DEBUGLEVEL               Set debug level
  -s, --configfile=CONFIGFILE               Use alternate configuration file
  -l, --log-basename=LOGFILEBASE            Base name for log files
  -V, --version                             Print version
      --option=name=value                   Set smb.conf option from command line
```

- Connection options:
```bash
  -O, --socket-options=SOCKETOPTIONS        socket options to use
  -n, --netbiosname=NETBIOSNAME             Primary netbios name
  -W, --workgroup=WORKGROUP                 Set the workgroup name
  -i, --scope=SCOPE                         Use this Netbios scope
```

- Authentication options:
```bash
  -U, --user=USERNAME                       Set the network username
  -N, --no-pass                             Don\'t ask for a password
  -k, --kerberos                            Use kerberos (active directory) authentication
  -A, --authentication-file=FILE            Get the credentials from a file
  -S, --signing=on|off|required             Set the client signing state
  -P, --machine-pass                        Use stored machine account password
  -e, --encrypt                             Encrypt SMB transport
  -C, --use-ccache                          Use the winbind ccache for authentication
      --pw-nt-hash                          The supplied password is the NT hash
```                                                                                