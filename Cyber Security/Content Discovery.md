# Content Discovery
[Back to cyber security](Cyber%20security.md)
- --
##  What is Content Discovery?
Discovering confidential and hidden pages or portals intended for staff usage, older versions of the website, backup files, configuration files, administration panels, etc.

3 ways to do it:
- Manually
- Automatically
- OSINT

- --
## Robots.txt
The robots.txt file is a document that tells search engines which pages they are and aren't allowed to show on their search engine results or ban specific search engines from crawling the website altogether. 

Method:
Check Robots.txt for hidden sites. 
Example : https://example.com/robots.txt
- --
## Favicon
The favicon is a small icon displayed in the browser's address bar or tab used for branding a website.

Sometimes when frameworks are used to build a website, a favicon that is part of the installation gets leftover, and if the website developer doesn't replace this with a custom one, this can give us a clue on what framework is in use. 

Method :
curl favicon_link | md5sum
match sum with this database : https://wiki.owasp.org/index.php/OWASP_favicon_database

- --
## Sitemap.xml

Unlike the robots.txt file, which restricts what search engine crawlers can look at, the sitemap.xml file gives a list of every file the website owner wishes to be listed on a search engine. These can sometimes contain areas of the website that are a bit more difficult to navigate to or even list some old webpages that the current site no longer uses but are still working behind the scenes.

Method :
Example : https://example.com/sitemap.xml
- --
## HTTP Headers
When we make requests to the web server, the server returns various HTTP headers. These headers can sometimes contain useful information such as the webserver software and possibly the programming/scripting language in use. In the below example, we can see the webserver is NGINX version 1.18.0 and runs PHP version 7.4.3. Using this information, we could find vulnerable versions of software being used. Try running the below curl command against the web server, where the -v switch enables verbose mode, which will output the headers (there might be something interesting!).

Method :
curl https://example.com -v
- --
## Framework Stack

Once you've established the framework of a website, either from the above favicon example or by looking for clues in the page source such as comments, copyright notices or credits, you can then locate the framework's website. From there, we can learn more about the software and other information, possibly leading to more content we can discover.

Method :
Check documentation of framework to find hidden or authorities page.
- --
## Google Hacking / Dorking
Read : https://en.wikipedia.org/wiki/Google_hacking
- --
## Wappalyzer

Wappalyzer (https://www.wappalyzer.com/) is an online tool and browser extension that helps identify what technologies a website uses, such as frameworks, Content Management Systems (CMS), payment processors and much more, and it can even find version numbers as well.
 
 Method:
 wappalyzer.com and search website.
- --
## Wayback Machine

The Wayback Machine (https://archive.org/web/) is a historical archive of websites that dates back to the late 90s. You can search a domain name, and it will show you all the times the service scraped the web page and saved the contents. This service can help uncover old pages that may still be active on the current website.

Method:
Find history of website
- --
## GitHub

To understand GitHub, you first need to understand Git. Git is a **version control system** that tracks changes to files in a project. Working in a team is easier because you can see what each team member is editing and what changes they made to files. When users have finished making their changes, they commit them with a message and then push them back to a central location (repository) for the other users to then pull those changes to their local machines. GitHub is a hosted version of Git on the internet. Repositories can either be set to public or private and have various access controls. You can use GitHub's search feature to look for company names or website names to try and locate repositories belonging to your target. Once discovered, you may have access to source code, passwords or other content that you hadn't yet found.

- --
## S3 Buckets
S3 Buckets are a storage service provided by Amazon AWS, allowing people to save files and even static website content in the cloud accessible over HTTP and HTTPS. The owner of the files can set access permissions to either make files public, private and even writable. Sometimes these access permissions are incorrectly set and inadvertently allow access to files that shouldn't be available to the public. The format of the S3 buckets is http(s)://{name}.s3.amazonaws.com where {name} is decided by the owner, such as tryhackme-assets.s3.amazonaws.com. S3 buckets can be discovered in many ways, such as finding the URLs in the website's page source, GitHub repositories, or even automating the process. One common automation method is by using the company name followed by common terms such as {name}-assets, {name}-www, {name}-public, {name}-private, etc.

- --
### Source:
- [Tryhackme](https://tryhackme.com/room/contentdiscovery#)
- [Wiki google hacking](https://en.wikipedia.org/wiki/Google_hacking)
- [Wappalyzer] (https://www.wappalyzer.com/)
- 