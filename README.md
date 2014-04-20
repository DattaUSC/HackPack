![Alt](http://highgroundhackers.org/wp-content/uploads/2014/04/HackPack.png)
Hack Pack 1.0 [![Dependency Status](https://david-dm.org/sahat/hackathon-starter.svg?theme=shields.io)](https://david-dm.org/sahat/hackathon-starter) [![Build Status](https://travis-ci.org/sahat/hackathon-starter.svg?branch=master)](https://travis-ci.org/sahat/hackathon-starter) [![Analytics](https://ga-beacon.appspot.com/UA-47447818-2/hackathon-starter?pixel)](https://github.com/igrigorik/ga-beacon)
=====================

<a href="https://github.com/sahat/hackathon-starter/zipball/master">
  <img src="https://lh5.googleusercontent.com/-QYRVFFig8fI/U0xzuHnAWbI/AAAAAAAAEBM/qU5rHrPvpOI/w840-h272-no/Screenshot+2014-04-14+19.46.12.png" height="68">
</a> <a href="http://hackathonstarter.herokuapp.com" target="_blank">
  <img src="https://lh4.googleusercontent.com/-NXCLKSnPU60/U0xzuGt37_I/AAAAAAAAEBY/QjWLUHowgzY/w792-h272-no/Screenshot+2014-04-14+19.47.22.png" height="68">
</a>

Jump to [What's new in 2.0?](#changelog)

A boilerplate for **Node.js** web applications.

If you have attended any hackathons in the past, then you know how much time it takes to
get a project started: decide on what to build, pick a programming language, pick a web framework,
pick a CSS framework. A while later, you might have an initial project up on GitHub and only then
can other team members start contributing. Or how about doing something as simple as *Sign in with Facebook*
authentication? You can spend hours on it if you are not familiar with how OAuth 2.0 works.

When I started this project, my primary focus was on **simplicity** and **ease of use**.
I also tried to make it as **generic** and **reusable** as possible to cover most use cases of hackathon web apps,
without being too specific. In the worst case you can use this as a learning guide for your projects,
if for example you are only interested in **Sign in with Google** authentication and nothing else.

Chances are you do not need all authentication methods or API examples. As of **Hackathon Starter 2.0**
it is possible to selectively check which authentication methods you need by running `generator.js`. For now
you still have to manually remove API examples that you don't need.

<h4 align="center">Flatly Bootstrap Theme</h3>

![](https://lh6.googleusercontent.com/-hcbsNx9tagc/U0xhUuAAPSI/AAAAAAAAEAg/kppd76NPORs/w1210-h952-no/Screenshot+2014-04-14+18.28.02.png)

<h4 align="center">Default Theme</h3>

![](https://lh5.googleusercontent.com/-KmlaMLKGCqg/UuWt4MrXzeI/AAAAAAAAD6o/KUucObo33zU/w1170-h860-no/Screenshot+2014-01-26+19.52.03.png)

<h4 align="center">Hackathon Starter Generator</h3>

![](https://lh6.googleusercontent.com/-61huCORb8w0/U0wq1xj3IiI/AAAAAAAAD_8/tnkfKnwOpGM/w1370-h962-no/Screenshot+2014-04-14+14.33.06.png)

Table of Contents
-----------------

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Generator](#generator)
- [Obtaining API Keys](#obtaining-api-keys)
- [Project Structure](#project-structure)
- [List of Packages](#list-of-packages)
- [Useful Tools and Resources](#useful-tools-and-resources)
- [Recommended Design Resources](#recommended-design-resources)
- [Recommended Node.js Libraries](#recommended-nodejs-libraries)
- [Recommended Client-side Libraries](#recommended-client-side-libraries)
- [Pro Tips](#pro-tips)
- [FAQ](#faq)
- [How It Works](#how-it-works-mini-guides)
- [Mongoose Cheatsheet](#mongoose-cheatsheet)
- [Deployment](#deployment)
- [Changelog](#changelog)
- [Contributing](#contributing)
- [License](#license)

Features
--------

- **Local Authentication** using Email and Password
- **OAuth 1.0a Authentication** via Twitter
- **OAuth 2.0 Authentication** via Facebook, Google, GitHub, LinkedIn, Instagram
- Flash notifications with animations by [animate.css](http://daneden.github.io/animate.css/)
- MVC Project Structure
- Node.js clusters support
- Rails 3.1-style asset pipeline by connect-assets (See FAQ)
- LESS stylesheets (auto-compiled without any Gulp/Grunt hassle)
- Bootstrap 3 + Flat UI + iOS7
- Contact Form (powered by Mailgun or Sendgrid)
- **Account Management**
 - Gravatar
 - Profile Details
 - Change Password
 - Forgot Password
 - Reset Password
 - Link multiple OAuth strategies to one account
 - Delete Account
- CSRF protection
- **API Examples**: Facebook, Foursquare, Last.fm, Tumblr, Twitter, Stripe, LinkedIn and more.

Prerequisites
-------------

- [MongoDB](http://www.mongodb.org/downloads)
- [Node.js](http://nodejs.org)
- Command Line Tools
 - <img src="http://deluge-torrent.org/images/apple-logo.gif" height="17">&nbsp;**Mac OS X**: [Xcode](https://itunes.apple.com/us/app/xcode/id497799835?mt=12) (or **OS X 10.9 Mavericks**: `xcode-select --install`)
 - <img src="http://dc942d419843af05523b-ff74ae13537a01be6cfec5927837dcfe.r14.cf1.rackcdn.com/wp-content/uploads/windows-8-50x50.jpg" height="17">&nbsp;**Windows**: [Visual Studio](http://www.visualstudio.com/downloads/download-visual-studio-vs#d-express-windows-8)
 - <img src="https://lh5.googleusercontent.com/-2YS1ceHWyys/AAAAAAAAAAI/AAAAAAAAAAc/0LCb_tsTvmU/s46-c-k/photo.jpg" height="17">&nbsp;**Ubuntu**: `sudo apt-get install build-essential`
 - <img src="http://i1-news.softpedia-static.com/images/extra/LINUX/small/slw218news1.png" height="17">&nbsp;**Fedora**: `sudo yum groupinstall "Development Tools"`
 - <img src="https://en.opensuse.org/images/b/be/Logo-geeko_head.png" height="17">&nbsp;**OpenSUSE**: `sudo zypper install --type pattern devel_basis`

:exclamation: **Note:** If you are new to Node or Express, I recommend to watch
[Node.js and Express 101](http://www.youtube.com/watch?v=BN0JlMZCtNU)
screencast by Alex Ford that teaches Node and Express from scratch. Alternatively,
here is another great tutorial for complete beginners - [Getting Started With Node.js, Express, MongoDB](http://cwbuecheler.com/web/tutorials/2013/node-express-mongo/).

Getting Started
---------------

The easiest way to get started is to clone the repository:

```bash
# Fetch only the latest commits
git clone --depth=1 git@github.com:sahat/hackathon-starter.git my-project

cd my-project

# Install NPM dependencies
npm install

node app.js
```

:exclamation: **Note:** I highly recommend installing [Nodemon](https://github.com/remy/nodemon).
It watches for any changes in your  node.js app and automatically restarts the
server. Once installed, instead of `node app.js` use `nodemon app.js`. It will
save you a lot of time in the long run, because you won't need to manually
restart the server each time you make a small change in code. To install, run
`sudo npm install -g nodemon`.

Generator
---------

Hackathon Starter Generator is still in alpha stage. It is tighly tied to the
project code. As soon as you start changing and moving things around, it will
probably no longer work as expected. That is why it's best to use when you first
download Hackathon Starter.

:exclamation: **Note:** Generator has a "destructive" behavior, it will physically
modify your code. *There is no undo action.* To be on a safe side, always commit
your code to Git, so you could go back and undo the changes.

Currently it supports adding/removing authentication providers and switching
between SendGrid/Mailgun email services. In the future you'll be able to use
it to quickly add Socket.io support to your app, add Mozilla Persona sign-in,
generate new pages (create new routes, templates and controllers for you
automatically).

Obtaining API Keys
------------------

To use any of the included APIs or OAuth authentication methods, you will need
to obtain appropriate credentials: Client ID, Client Secret, API Key, or
Username & Password. You will need to go through each provider to generate new
credentials.

**Hackathon Starter 2.0 Update:** I have included dummy keys and passwords for
all API examples to get you up and running even faster. But don't forget to update
them with *your credentials* when you are ready to deploy an app.

<img src="http://images.google.com/intl/en_ALL/images/srpr/logo6w.png" width="200">
- Visit [Google Cloud Console](https://cloud.google.com/console/project)
- Click **CREATE PROJECT** button
- Enter *Project Name*, then click **CREATE**
- Then select *APIs & auth* from the sidebar and click on *Credentials* tab
- Click **CREATE NEW CLIENT ID** button
 - **Application Type**: Web Application
 - **Authorized Javascript origins**: http://localhost:3000
 - **Authorized redirect URI**: http://localhost:3000/auth/google/callback
- Copy and paste *Client ID* and *Client secret* keys into `config/secrets.js`

:exclamation: **Note:** When you ready to deploy to production don't forget to
add your new url to *Authorized Javascript origins* and *Authorized redirect URI*,
e.g. `http://my-awesome-app.herokuapp.com` and
`http://my-awesome-app.herokuapp.com/auth/google/callback` respectively.
The same goes for other providers.

<hr>

START WITH HEROKU:

1. Go to https://www.heroku.com and Sign Up

2. Click on "Add-Ons"

** Add SendGrid **

3. Click on Sendgrid

4. Open Terminal and type in: heroku addons:add sendgrid

<hr >

SETUP MAILGUN:

1. Go to https://mailgun.com/signup and Sign Up

2. Copy script on next page and open up your terminal and paste it

3. Check your email, you should have received an email 

<hr>

<p>Heroku</p>
<p>MongoDB</p>
<p>Twilio</p>
<p>Twitter</p>
<p>BitSync Torrent</p>
<p>MailGun</p>
<p>Google</p>
