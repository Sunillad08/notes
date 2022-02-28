# Sherlock
[Back to cyber security page](./index.md)

---

## What is sherlock??
🔎 Hunt down social media accounts by username across social networks!

---

## Usage
get git repo on device
pip3 install -r requirements.txt
python3 sherlock USERNAME


|Option|Purpose|
|:--|:-|
|-h, --help |show this help message and exit|
|--version | Display version information and dependencies.|
|--verbose, -v, -d, --debug|Display extra debugging information and metrics.|
|--folderoutput FOLDEROUTPUT, -fo FOLDEROUTPUT|If using multiple usernames, the output of the results will be saved to this folder.|
| --output OUTPUT, -o OUTPUT|If using single username, the output of the result will be saved to this file.|
| --tor, -t |Make requests over Tor; increases runtime; requires Tor to be installed and in system path.|
|--unique-tor, -u |Make requests over Tor with new Tor circuit after each request; increases runtime; requires Tor to be installed and in system path.|
| --csv|Create Comma-Separated Values (CSV) File.|
|--site SITE_NAME|Limit analysis to just the listed sites. Add multiple options to specify more than one site.|
|--proxy PROXY_URL, -p PROXY_URL| Make requests over a proxy. e.g. socks5://127.0.0.1:1080|
|--json JSON_FILE, -j JSON_FILE| Load data from a JSON file or an online, valid, JSON file.|
|--timeout TIMEOUT |Time (in seconds) to wait for response to requests. Default timeout is infinity. A longer timeout will be more likely to get results from slow sites. On the other hand, this may cause a long delay to gather all results.|
|--print-all | Output sites where the username was not found.||
|--print-foun| Output sites where the username was found.|
|--no-color  | Don't color terminal output|
|--browse, -b| Browse to all results on default browser.|
|--local, -l | Force the use of the local data.json file.|


---

### Source:
- [Null Byte YT video](https://youtu.be/HrqYGTK8-bo)
- [Sherlock repository](https://github.com/sherlock-project/sherlock)