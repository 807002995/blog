# React Blog 


[![LICENSE](https://img.shields.io/badge/license-Anti%20996-blue.svg)](https://github.com/996icu/996.ICU/blob/master/LICENSE)
[![996.icu](https://img.shields.io/badge/link-996.icu-red.svg)](https://996.icu)


For chinese , you can visit this [中文](https://github.com/faultaddr/react-blog/blob/main/README.zh-CN.md)

One-click installation & deployment of the React blog, freeing your hands so that you only need to change the configuration file to have a perfect personal technical blog!

This ReadMe file contains the following:

1. How to install and deploy a blog
2. How to configure front-end page information
3. How to configure sensitive back-end information


## Table of Contents

- [Background](#Background)
- [Install](#Install)
- [Usage](#Usage)
- [Features and Personalized Configuration](#Features-and-Personal-Configuration)
     - [Features](#Features)
     - [Personalized Configuration](#Personalized-Configuration)
     - [Personalized Information Configuration](#Personalized-Information-Configuration)
     - [Background sensitive information configuration](#Background-sensitive-information-configuration)
- [Maintainer](#Maintainer)
- [Contributing](#Contributing)
- [License](License)

## Background

`React Blog` was originally built on the basis of project [alvin0216/react-blog](https://github.com/alvin0216/react-blog) which was created by [alvin0216](https://github.com/alvin0216) , In order to fix some known issues and add more personalized elements, Last but no Least, I have added various security guarantees of the website, making it more cool and easier to use.


In order to build a personal website, you first need to rent a cloud server (centos is generally used instead in this article), and use Alibaba Cloud/Tencent Cloud/AWS to host the website. Or you can use Ngrok to do intranet penetration and deploy the website on your PC.


## Install

If you want to deploy on the Centos server, you can directly use our one-click installation deployment script:
```sh
$ sh install.sh
```
If you want to install and configure yourself, use [node](http://nodejs.org),[npm](https://npmjs.com),[yarn](),[forever]() for this project. Please make sure You have performed the correct installation locally.

```sh
$ npm install --global yarn
$ npm install --global forever
```


## Usage

If you use the one-click installation script mentioned above, please pay attention to whether the port is occupied when starting later:

```sh
$ yum install lsof
$ lsof -i:80
$ lsof -i:6060
```
If there is port occupation, please end the process or change the port

Then execute the following instructions for production deployment

```sh
$ cd src
$ yarn build
$ nohup serve -s build -l 80 &
$
$ cd server
$ forever start app.js
```

Or for development environment deployment

```sh
$ cd src
$ nohup yarn dev
$
$ cd server
$ forever start app.js
```



## Features and Personal Configuration

### Features

- [x] Front Desk: Homepage + List Page + Search Page + Category Page + Tab Page
- [x] Backstage: article management + user management
- [x] Responsive, article anchor navigation, back to top, `markdown` code highlighting, `mathjax` support
- [x] Users: users on the site, users authorized to log in by a third-party `github`
- [x] Users can comment and reply, as well as the status of **mail notification** reply
- [x] `md` file import and export function! You can directly upload the `md` file to generate an article
- [x] Separation of private and public articles
- [x] One-click comment without registration
- [x] Homepage background
- [x] Top of article
- [x] Gossip
- [x] Get the mailbox secret dynamically
- [x] Password transmission encryption
- [x] Background chart
- [x] Share Link for the admain to manage the visiablity of the private article
- [ ] Smart Recommendation (Related Recommendation)

