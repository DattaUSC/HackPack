![Alt](http://highgroundhackers.org/wp-content/uploads/2014/04/hack11.png)
Hack Pack 1.0
=====================

<a href="https://github.com/sahat/hackathon-starter/zipball/master">
  <img src="http://highgroundhackers.org/wp-content/uploads/2014/04/buttonblack.png" height="44">
</a> <a href="http://hackathonstarter.herokuapp.com" target="_blank">
  <img src="http://highgroundhackers.org/wp-content/uploads/2014/04/gdemobutton.png" height="44">
</a>

A boilerplate for web applications.

If you've ever been to a Hackathon, you'll realize that most teams spend hours just setting up their basic infrastructure to connect code and deploy it. Setting up API's, connecting GitHub, and getting your project on the web all take precious time out of actually getting to the best part of your project - the final product or demo. We are putting together a Hack Pack to get you started. The goal is to make it easy enough for easy non-developers to install and deploy these technologies.

Chances are you do not need all authentication methods or API examples. As of **Hackathon Starter 1.0**

<hr />

<h4 align="center">Progressus Bootstrap Theme</h3>

![](http://highgroundhackers.org/wp-content/uploads/2014/04/progressus.png)

<hr />

<h4 align="center">Minimal Theme</h3>

![](http://highgroundhackers.org/wp-content/uploads/2014/04/minimal.png)

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
- [Meteor.js](https://www.meteor.com)
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

Getting Started With Heroku
---------------------------

<img src="http://www.coloandcloud.com/wp-content/uploads/2012/05/heroku_logo.jpg" width="200">

1. Go to https://toolbelt.heroku.com/ and dowload Heroku Toolbelt for Mac OSX

2. Create a folder on your desktop for your Git Repo

3. Go to Terminal - > go to folder in Term

git init (Install Command Line Tools)

- You should see a message that says “Initialized empty Git repository in Users/your.name/Desktop/HackPack/.git/

4. Download Sublime Text 2 and Open the Program

5. Write “Hello World!” and save it as ReadMe.md

6. Put ReadMe.md in your HackPack folder

7. git add ReadMe.md

8. git commit -m “This is my first push”
______

9. Go to https://github.com/ and create an account or Login to your existing account

10. Click on Repositories and then “New”

11. Name your repository “Urban Hack” and click on “Create Repository”
touch README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/DDcali2012/UrbanHack.git
git push -u origin master
Type in username / password for Github if prompted
______

12. Go to http://www.bootstrapzero.com/bootstrap-templates/starter and Download “simple vanilla template”

13. Rename as “index.html” and stick in HackPack folder

14. In Terminal type git add index.html

15. Type git push -u origin master

16. If done correctly, you will see your files on Github

______________

17. In Terminal type heroku create to create a new app for deployment

18. Type git push heroku master

<hr>

START WITH HEROKU:

1. Go to https://www.heroku.com and Sign Up

2. Create an App

3. Click on "Add-Ons"

** Add SendGrid **

4. Click on Sendgrid

5. Open Terminal and type in: heroku addons:add sendgrid

<hr >

SETUP MAILGUN:

1. Go to https://mailgun.com/signup and Sign Up

2. Copy script on next page and open up your terminal and paste it

3. Check your email, you should have received an email 

<hr>

Github App
-----------------

Install GitHub App for Mac: https://mac.github.com/

<hr>

Install Meteor.js
-----------------

**Step One, in Terminal type:**

curl https://install.meteor.com/ | sh

**Then type:**

$ meteor create ~/my_cool_app

$ cd ~/my_cool_app

$ meteor

<hr >

<p>Heroku</p>
<p>MongoDB</p>
<p>Twilio</p>
<p>Twitter</p>
<p>BitSync Torrent</p>
<p>MailGun</p>
<p>Google</p>
<p>Meteor.js</p>
