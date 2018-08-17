# Presentation: The State of Progressive Web Apps 2018

This repository contains the reveal.js slides and sample application for a presentation I recently gave at a local user group on Progressive Web Apps.  Please note that the contents of the repository are simply the personal opinions and thoughts of the author and are not offered as any kind guidance or advice.  The presentation and supporting material are the authors personal opinions and in no way represent his employer's views.  Please feel free to use the artifacts in this repository in accordance with the [MIT License](LICENSE).

I am really excited about the future of PWA technology and the advantages it will bring to both users and developers.  However, I am **not** an expert on Progressive Web Applications.  My main goal in preparing this presentation was as a means to learn more about these technologies and to share that knowledge with other local developers.  I hope it has inspired others to learn more!

## Intro
Progressive web applications have become a very popular topic in the web and mobile development communities.  They are receiving a lot of attention at technical conferences and presentations all over the world.  Large technology companies like Google, Microsoft, Apple, and Mozilla are providing (or working towards) support in their browsers and operating systems.  Building a single application that is delivered via the web and provides much of the same functionality and experience as a native or desktop application can be a very attractive option for many types of business applications.

In this presentation we will discuss what makes an application progressive and how it compares to other types of common web and mobile applications.  We will also discuss why you would consider building an application using a progressive approach.  This discussion will cover the basic technologies used to create progressive applications: progressive enhancement, responsive design, web application manifests, service workers, and an application shell architecture.  We will wrap up with a look at some of the current challenges and limitations of progressive web apps as well as the latest developments in the industry.

## Presentation
The presentation may be viewed in github pages:  
https://davidbwilson.github.io/StateOfPWAPresentation/#

## Helpful Links

Here are some references I found extremely useful while researching PWAs:

### Books:
Building Progressive Web Apps: Bringing the Power of Native to the Browser 1st Edition
https://www.amazon.com/Building-Progressive-Web-Apps-Bringing/dp/1491961651/ref=sr_1_1?ie=UTF8&qid=1510064612&sr=8-1&keywords=progressive+web+apps

### Documentation:
Google Developer Documentation
https://developers.google.com/web/progressive-web-apps/

Mozilla API Documentation
https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API

Angular Service Worker Support
https://angular.io/guide/service-worker-intro

Standards:
https://www.w3.org/TR/appmanifest/
https://www.w3.org/TR/service-workers-1/
https://www.w3.org/TR/push-api/

### Microsoft Support
Adding your PWA to the Microsoft Store
https://docs.microsoft.com/en-us/microsoft-edge/progressive-web-apps/microsoft-store

Accessing Windows features from a Store Installed app
https://docs.microsoft.com/en-us/microsoft-edge/progressive-web-apps/windows-features

### Presentations:
Microsoft Build 2018 
https://www.youtube.com/watch?v=6fb-t9ffDvo

### Articles:
Web Apps are only getting better
https://www.theverge.com/circuitbreaker/2018/4/11/17207964/web-apps-quality-pwa-webassembly-houdini

What's up with IOS?
https://dockyard.com/blog/2017/07/13/safari-ios-and-progressive-web-apps

Does service work run in background when browser is closed?
https://stackoverflow.com/questions/39201067/does-service-worker-runs-on-background-even-if-browser-is-closed

I built a Progressive Web App and published it in 3 app stores. Here’s what I learned.
https://medium.freecodecamp.org/i-built-a-pwa-and-published-it-in-3-app-stores-heres-what-i-learned-7cb3f56daf9b

Progressive web apps on IOS are here
https://medium.com/@firt/progressive-web-apps-on-ios-are-here-d00430dee3a7

The Ultimate Guide to Progressive Web Applications
https://scotch.io/tutorials/the-ultimate-guide-to-progressive-web-applications

The Gartner Hype Cycle
Gartner Hype Cycle  
https://en.wikipedia.org/wiki/Hype_cycle#/media/File:Hype-Cycle-General.png


Utilities:
Real Fav Icon Generator
https://realfavicongenerator.net

Can I use?
Https://caniuse.com

What can the web do today?
https://whatwebcando.today/

PWA Builder from Microsoft (builds manifest and appx)
https://www.pwabuilder.com/

Google Workbox
https://developers.google.com/web/tools/workbox/

## Setup the sample app

During this demonstration we use an **extremely** basic application to demonstrate the creation of a progressive web application.  This application consists of only one html page (index) and enough artifacts to support a service worker and a manifest.  It has no framework or server side behavior and is **not** a fully functional application.  This was done intentionally to allow us to focus on the basic technologies that are used to create a functioning PWA.

The sample application can be found in the [sampleApp](sampleApp) folder of this repository.

To set up and run:

1. Clone the repository
```
git clone https://github.com/davidbwilson/StateOfPWAPresentation.git
```
2. Setup a local web server.  This could be live-server or it could be something as simple as [Web Server for Chrome]( https://chrome.google.com/webstore/detail/web-server-for-chrome/ofhbbkphhbklhfoeikjpcbhemlocgigb?hl=en).
3. Open the index.html page in Chrome.

You should be able to:
* View the sample app.
* Pin it to the home page.  To force the pin bannner in the app -> open chrome dev tools, application tab, select manifest on the left, and Add to homescreen link on the right.  You may need to click on / interact with the web page to get Chrome to show the banner.  Click the add button in the banner at the top of the page.  Give the application a name and you should now be able to launch it from the desktop.
* Verify it is an authentic PWA using Lighthouse in the Chrome developer tools. 