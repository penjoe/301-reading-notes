# Code Fellows 301d61 Reading Notes

[Table of Contents](https://penjoe.github.io/301-reading-notes/)

## **Class 06**:

### **Article: Intro to Node.js**

#### **What is Node.js?**
What is Node.js, or just Node for short? According to Node's homepage, it is:

>Node.js® is a JavaScript runtime built on Chrome’s V8 JavaScript engine.

But what does that mean? While there are lots of technical terms that could be used to explain what Node is, it's a;; based around the V8 JavaScript engine. So lets start by figuring out what that is.

The V8 engine is an open source JS engine that runs inside of Google's Chrome browser and other similar chromium based browsers like Opera. It is responsible for compiling JS into code that your computer can process. What Node does is not execute code directly in your browser, but instead offer a runtime environment in which to execute JS.

#### **Installing Node**

There are two ways to download and install Node. Through the official [Node download page](https://nodejs.org/en/download/) or through a package manager on [npm](https://www.npmjs.com/).

Once you download Node directly, install it on your computer. Once installed, ensure that it was properly working via your terminal. Type
```
node --version
```
You should get back a version number, signifying that you have Node properly installed.

An alternative to a direct download is npm. Npm is the premier package handler for JS, having over 1,000,000 packages available. Once you have npm installed, running this command will install a global package:
```
npm install -g filename
```
Whichever method you use to get Node, once installed it will give you access to run JS through the Node runtime environment. Now we can install and run various build tools that will help us develop modern JS applications.

#### **Using Node**

Node.js lets us run JS on the server. Here's a visualization of how Node works:
![node](https://dab1nmslvvntp.cloudfront.net/wp-content/uploads/2012/10/1516152673node_event_loop.png)

Here are some additional resources for understanding and working with Node:
- [A beginner's guide to webpacks - article](https://www.sitepoint.com/webpack-beginner-guide/)
- [The anatomy of a odern JS application - article](https://www.sitepoint.com/anatomy-of-a-modern-javascript-application/)
- [What the heck is the event loop anyway? - video](https://www.youtube.com/watch?v=8aGhZQkoFbQ)