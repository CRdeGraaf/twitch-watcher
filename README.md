


<h1 align="center">Twitch watcher</h1>
<p align="center"> I spent two days watching Valorant streams to get a drop. I got bored...</p>
<p align="center">
<img alt="GitHub package.json version" src="https://img.shields.io/github/package-json/v/frosty5689/twitch-watcher"> <img alt="GitHub" src="https://img.shields.io/github/repo-size/frosty5689/twitch-watcher"> <img alt="GitHub repo size" src="https://img.shields.io/github/license/frosty5689/twitch-watcher"> <img alt="GitHub issues" src="https://img.shields.io/github/issues/frosty5689/twitch-watcher">
</p>
<p align="center">
 <a href="https://asciinema.org/a/rob4Rh1EG4XFVfN4XWK67JSnf" target="_blank"><img src="https://asciinema.org/a/rob4Rh1EG4XFVfN4XWK67JSnf.svg" /></a>
</p>

## Features
- 🎥 True HTTP Live Streaming support (Forget the #4000 error code)
- 📦 Periodically check for drops and claim them
- 🔐 Cookie-based login
- 📜 Auto accept cookie policy
- 👨‍💻 The choice of a random streamer with drop-enabled tag
- 🤐 Unmuted stream
- 🛠 Detect mature content-based stream and interact with it
- 🛡 Proxy option
- 📽 Automatic lowest possible resolution settings
- 🧰 Highly customizable codebase
- 📦 Deployable to VPS by docker

## Requirements

 - Windows or Linux OS
 - Network connection (Should be obvious...)
 - [Nodejs](https://nodejs.org/en/download/) and [NPM](https://www.npmjs.com/get-npm)

## Installation
🎥 [Tutorial video by Ziyad](https://youtu.be/bwzv7wT44Ds) 🎥
### Windows
1. Login to your twitch account
2. Open inspector(F12 or Ctrl+Shift+I) on main site
3. Find the stored cookie section
4. Copy **auth-token**
5. Clone this repo
6. Install Chromium
7. Usually the path to the Chromium executable is: C:\\Program Files (x86)\\Google\\Chrome\\Application\\chrome.exe
8. Install the dependencies with `npm install`
9. Start the program with `npm start`
### Linux
1. Login to your twitch account
2. Open inspector(F12 or Ctrl+Shift+I) on main site
3. Find the stored cookie section
4. Copy **auth-token**
5. Clone this repo
6. Install Chromium: [TUTORIAL 🤗](https://www.addictivetips.com/ubuntu-linux-tips/install-chromium-on-linux/)
7. Locate Chromium executable: `whereis chromium` or `whereis chromium-browser`
8. Install the dependencies with `npm install`
9. Start the program with `npm start`

## Docker
<p align="center">
<img alt="Docker Image Version (latest by date)" src="https://img.shields.io/docker/v/frosty5689/twitch-watcher"> <img alt="Docker Pulls" src="https://img.shields.io/docker/pulls/frosty5689/twitch-watcher"> <img alt="Docker Image Size (latest by date)" src="https://img.shields.io/docker/image-size/frosty5689/twitch-watcher">
</p>


>Docker is a set of platform as a service (PaaS) products that uses OS-level virtualization to deliver software in packages called containers. Containers are isolated from one another and bundle their own software, libraries and configuration files. All containers are run by a single operating system kernel and therefore use fewer resources than virtual machines.
### Requirements
- [Docker](https://docs.docker.com/get-docker/)
- [Docker-Compose](https://docs.docker.com/compose/install/)

### Usage
1. Download docker-compose-example.yml
2. Rename docker-compose.yml
3. Open and replace the **token** environment record
4. Run with `docker-compose up -d` command
## Dependencies
<p align="center">
<img alt="GitHub package.json dependency version (subfolder of monorepo)" src="https://img.shields.io/github/package-json/dependency-version/frosty5689/twitch-watcher/puppeteer-core"> <img alt="GitHub package.json dependency version (subfolder of monorepo)" src="https://img.shields.io/github/package-json/dependency-version/frosty5689/twitch-watcher/cheerio"> <img alt="GitHub package.json dependency version (subfolder of monorepo)" src="https://img.shields.io/github/package-json/dependency-version/frosty5689/twitch-watcher/inquirer"> <img alt="GitHub package.json dependency version (subfolder of monorepo)" src="https://img.shields.io/github/package-json/dependency-version/frosty5689/twitch-watcher/dotenv"> <img alt="GitHub package.json dependency version (subfolder of monorepo)" src="https://img.shields.io/github/package-json/dependency-version/frosty5689/twitch-watcher/dayjs"> <img alt="GitHub package.json dependency version (prod)" src="https://img.shields.io/github/package-json/dependency-version/frosty5689/twitch-watcher/tree-kill">
</p>

## Troubleshooting

### How does the token look like?
auth-token: `rxk38rh5qtyw95fkvm7kgfceh4mh6u`
___


### Streamers.json is empty?

Try again with higher delay.
Default delay:
```javascript
const scrollDelay = 2000;
```
[Go to code](https://github.com/frosty5689/twitch-watcher/blob/12dce8065423861971b7088563ad936b2dcc2559/app.js#L15)
___
### Something went wrong?
Try non-headless mode. Set headless value to `true`, like this:
```javascript
const showBrowser = true;
```
[Go to code](https://github.com/frosty5689/twitch-watcher/blob/12dce8065423861971b7088563ad936b2dcc2559/app.js#L24)
___
### Proxy?

Yes, of course:
```javascript
const proxy = ""; // "ip:port" By https://github.com/Jan710
```
[Go to code](https://github.com/frosty5689/twitch-watcher/blob/12dce8065423861971b7088563ad936b2dcc2559/app.js#L25)

OR

With Docker env:
```
proxy=PROXY_IP_ADDRESS:PROXY_PORT
```
___
### Screenshot without non-headless mode
```javascript
const browserScreenshot = false;
```
[Go to code](https://github.com/frosty5689/twitch-watcher/blob/12dce8065423861971b7088563ad936b2dcc2559/app.js#L27)

## Donation
Please donate to keep alive this project!

Especially the drop farmers who gather tons of money with this software!🤓

<a href="https://www.buymeacoffee.com/frosty5689" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>


## Disclaimer
This code is for educational and research purposes only.
Do not attempt to violate the law with anything contained here.
I will not be responsible for any illegal actions.
Reproduction and copy is authorised, provided the source is acknowledged.
