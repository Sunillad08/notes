# Searchsploit
[Back to cyber security page](../index.md)
- --
## What is searchsploit ?
Exploit Database Archive Search
Allow you to search through exploits and shellcodes using one or more terms from Exploit-DB
- --
## Options
- Search Terms
```bash
-c, --case     [Term]      Perform a case-sensitive search (Default is inSEnsITiVe)
-e, --exact    [Term]      Perform an EXACT & order match on exploit title (Default is an AND match on each term) [Implies "-t"]
                                e.g. "WordPress 4.1" would not be detect "WordPress Core 4.1")
-s, --strict               Perform a strict search, so input values must exist, disabling fuzzy search for version range
                                e.g. "1.1" would not be detected in "1.0 < 1.3")
-t, --title    [Term]      Search JUST the exploit title (Default is title AND the file's path)
    --exclude="term"       Remove values from results. By using "|" to separate, you can chain multiple values
                                e.g. --exclude="term1|term2|term3"
```
- --
- Output
```bash
-j, --json     [Term]      Show result in JSON format
-o, --overflow [Term]      Exploit titles are allowed to overflow their columns
-p, --path     [EDB-ID]    Show the full path to an exploit (and also copies the path to the clipboard if possible)
-v, --verbose              Display more information in output
-w, --www      [Term]      Show URLs to Exploit-DB.com rather than the local path
    --id                   Display the EDB-ID value rather than local path
    --colour               Disable colour highlighting in search results
```
- --
-  Non-Searching
```bash
-m, --mirror   [EDB-ID]    Mirror (aka copies) an exploit to the current working directory
-x, --examine  [EDB-ID]    Examine (aka opens) the exploit using $PAGER
```
- --
- Non-Searching
```bash
-h, --help                 Show this help screen
-u, --update               Check for and install any exploitdb package updates (brew, deb & git)
```
- Automation
```bash
    --nmap     [file.xml]  Checks all results in Nmap's XML output with service version
                                e.g.: nmap [host] -sV -oX file.xml
```

- --
### Source
- Man page of searchsploit
- [Hackersploit youtube video](https://youtu.be/29GlfaH5qCM?t=326)
- [Youtube video](https://youtu.be/kSZ9IPk7srU)