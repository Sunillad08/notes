# dirb
[Back to cyber security page](../index.md)

---

## What is dirb?
DIRB IS a Web Content Scanner. It looks for existing (and/or hidden) Web Objects. It basically works by launching a dictionary basesd attack against a web server and analizing the response.

---

## Syntax
dirb <url_base> <url_base> <wordlist_file(s)> options
```bash
-a 		<agent_string> Specify your custom USER_AGENT.  (Default is: "Mozilla/4.0
		(compatible; MSIE 6.0; Windows NT 5.1)")
-b      Don't squash or merge sequences of /../ or /./ in the given URL.
-c <cookie_string>
        Set a cookie for the HTTP request.
-E <certificate>
        Use the specified client certificate file.
-f      Fine tunning of NOT_FOUND (404) detection.
-H <header_string>
        Add a custom header to the HTTP request.
-i      Use case-insensitive Search.
-l      Print "Location" header when found.
-N <nf_code>
        Ignore responses with this HTTP code.
-o <output_file>
        Save output to disk.
-p <proxy[:port]>
        Use this proxy. (Default port is 1080)
-P <proxy_username:proxy_password>
        Proxy Authentication.
-r      Don't Search Recursively.
-R      Interactive Recursion.  (Ask in which directories you want to scan)
-S      Silent Mode. Don't show tested words. (For dumb terminals)
-t      Don't force an ending '/' on URLs.
-u <username:password>
        Username and password to use.
-v      Show Also Not Existent Pages.
-w      Don't Stop on WARNING messages.
-x <extensions_file>
        Amplify search with the extensions on this file.
-X <extensions>
        Amplify search with this extensions.
-z <milisecs>
               Amplify search with this extensions.
```

---

### Source
- Man page