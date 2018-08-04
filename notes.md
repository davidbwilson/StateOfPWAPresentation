XKCD comic while getting ready

Who am I?

	* David Wilson 
	* Not an expert in Progressive Web Apps

		* Presenting to learn about them and share knowledge
		* See a lot of advantages and want to implement for my teams applications


Introduction to Progressive Web Apps

	* Overview

		* What are they?
		* Why would we want to use them?
	* Core Technologies (Service Workers and Manifest)
	* Vendor Support


Demo - app.ft.com - financial times. code.nasa.gov or twitter?

	* Show service worker registration and manifest in dev tools
	* Compare to cnn (offline vs. online)
	* Pin to home and open as an application


What are Progressive Web Apps?

	* Demo
    * Frances Berriman and Alex Russell in 2015
	* A core set of technologies for building richer applications using web technologies.
        * Service workers
        * Manifest
        * App Shell Architecture
	* Combines the best of Native and Web Apps
		* Rich User Experience of Native combined with the cross-platform and delivery
		* Uses the web as the delivery mechanism and is just an enhancement to our existing web applications
	    * Fulfills initial promise of iPhone

What are the characteristics of a PWA?

	* According to Alex Russel:

		* Responsive: to fit any form factor
		* Connectivity independent: Progressively-enhanced with Service Workers to let them work offline
		* App-like-interactions: Adopt a Shell + Content application model to create appy navigations & interactions
		* Fresh: Transparently always up-to-date thanks to the Service Worker update process
		* Safe: Served via TLS (a Service Worker requirement) to prevent snooping
		* Discoverable: Are identifiable as “applications” thanks to W3C Manifests and Service Worker registration scope allowing search engines to find them
		* Re-engageable: Can access the re-engagement UIs of the OS; e.g. Push Notifications
		* Installable: to the home screen through browser-provided prompts, allowing users to “keep” apps they find most useful without the hassle of an app store
		* Linkable: meaning they’re zero-friction, zero-install, and easy to share. The social power of URLs matters.

Why would I want to use them?

	* Better web applications
	* Reach a broader audience
		* According to a 2016 comScore report, the average person spends 84% of his time on mobile devices using just the top 5 most popular apps. I’m sorry to say, these are not your apps. On tablets that number is even higher, with 95% of user time spent in the top 5 apps.  The same report also presents figures showing that it is much easier to reach a large audience on a mobile site than in a native app. 
	* Decrease application store friction

		* Store life-cycle - Publishing and Updating
		* Discoverability
		* Difficult to get users to install your app
	* Building and maintaining for multiple platforms

		* Maintaining multiple versions


Not Convinced?

	* 65% of users install 0 native apps a month

		* Comscore
	* 84% of users spend time in just 5 apps
	* 95% on tablets!
	* Web sites reach 4.5 times greater

		* There are close to 600 mobile web properties that reach audiences larger than 5 million visitors—nearly 4.5 times greater than the number of native apps with similar audiences. The top 1,000 mobile web properties have audiences that are almost 3 times the size of the top 1,000, apps and their audiences are growing twice as fast as native app audiences.


Are there any success stories?

	* https://www.pwastats.com/
    * https://pwa.rocks/

Bottom line:
Users are more likely to use your app if:

	* It's easily discoverable
	* Linkable (cross device)
	* It's single click access


What are the *core* technologies?

	* Service worker
		* Background sync, offline, push notifications, caching
	* Application manifest
	* Push notifications
	* CacheStoraget API
		* this is done in the most unopinionated way possible by exposing a number of basic methods, such as the ability to create and open any number of caches, and store, retrieve, or delete responses in them.  
		* By combining service workers with the power of CacheStorage, we can get direct programmatic control over what gets cached, what gets removed from the cache, and which responses are returned from the cache and which are returned from the network.
	* IndexDB
		* transactional
		* object based
		* indexed
		* browser based


Who maintains the standards?

	* World Wide Web Consortium
	* Notification API, Push API, Service Workers, Background Sync, 


This sounds awesome, what's the catch?

	* Still a new technology
		* Gartner's Hype Cycle - https://en.wikipedia.org/wiki/Hype_cycle#/media/File:Hype-Cycle-General.png
	* Changing standards
		* Many of the standards are still in draft and subject to change.
		* The browsers that are currently supporting the standards are in motion.
	* Functionality still evolving on key platforms.
		* Google has the best support, but Microsoft is embracing PWAs and Apple has even started supporting them.


Comparing Platforms
    * https://whatwebcando.today/
    * https://caniuse.com

Apple

	* Service worker and app manifest support


Microsoft
    * Excellent User Experience
        * Want web apps on windows to be your best experience.
        * Progressive store apps are first class citizens of the MS store - they want your pwa to be your windows store app
    * PWA In-Store Apps are UWP Apps
        * Proliferation of web frameworks and tools makes building UWP apps as a PWA very attractive.
    * Auto discovery or publish to the store
        * PWA Builder
    * sonarwhal - Scans and tells you how you can make improvements to your site
    PWAs installed on Windows 10 enjoy all the benefits of running as Universal Windows Platform (UWP) apps, including protection through Windows app sandboxing security and full access to Windows Runtime (WinRT) APIs, including those for:
    Controlling device features (such as camera, microphone, GPS)
    Accessing user resources (such as calendar, contacts, documents, music)
    Launching / navigating your app through Cortana voice commands
    Integrating with the Windows OS (through the Windows Action Center, desktop taskbar, and context menus)
    ...and these are only a few of the added possibilities for your PWA on Windows!

    A PWA installed as a Windows 10 app runs independently from the browser, in a standalone (WWAHost.exe process) window.  Has to be installed from the store to become a UWP app and not a web site running in Edge.

Demo 
    * Example Windows Store PWA - MyCARFAX
    * mobile.twitter.com - UWP PWA

Why would I build a progressive web app now?

	* Good option for enterprise applications
		* skip the app store
	* Performance, performance, performance - the most important app feature
	* Less expensive to build and deploy
		* Good option for smaller shops
	* Community Momentum / Increasing Support

Service Workers
	* JavaScript Worker
		* It's a JavaScript Worker, so it can't access the DOM directly. Instead, a service worker can communicate with the pages it controls by responding to messages sent via the postMessage interface, and those pages can manipulate the DOM if needed.  Service worker is a programmable network proxy, allowing you to control how network requests from your page are handled.
	* Runs outside the page context
		* It's terminated when not in use, and restarted when it's next needed, so you cannot rely on global state within a service worker's onfetch and onmessage handlers. If there is information that you need to persist and reuse across restarts, service workers do have access to the IndexedDB API.
	* Advanced caching, background sync, and push notifications
		* https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API
		* 

Demo: Simple service worker

Advanced Service Worker Topics

	* Versioning 
		* Service worker activation rules and dealing with new state
	* Caching Strategies - https://serviceworke.rs/strategy-network-or-cache.html
		* Cache 
		* Cache, falling back to network
		* Network only
		* Cache, then network
	* Background Synchronization
	* Push Notifications
	* Cross page communication

Web App Manifest

	* Allows pinning to home screen
	* Simple json file
	* Defines behavior of the application

		* https://developer.mozilla.org/en-US/docs/Web/Manifest
		* https://realfavicongenerator.net/
		* Generates app manifest and all the icons for different devices / browsers.
	* 


Demo: Web App Manifest

App Shell

	* Minimum artifacts to load the application
	* Optimize asset loading
	* Determine critical assets  

Future of the web

	* Accepting Payments with the Payment Request API
	* User Management with the Credential Management API
	* Real-Time Graphics with WebGL
	* Futuristic APIs with Speech Recognition
	* Slick Media Playing UIs
	* Virtual Reality in the Browser with WebVREasy Sharing to and from Your App


Thank you for your time.
Want to learn more?

Book: Building Progressive Web Apps: Bringing the Power of Native to the Browser 1st Edition
https://www.amazon.com/Building-Progressive-Web-Apps-Bringing/dp/1491961651/ref=sr_1_1?ie=UTF8&qid=1510064612&sr=8-1&keywords=progressive+web+apps

Google Developer Documentation
https://developers.google.com/web/progressive-web-apps/

What's up with IOS?
https://dockyard.com/blog/2017/07/13/safari-ios-and-progressive-web-apps

Real Fav Icon Generator
https://realfavicongenerator.net

Can I use?
Https://caniuse.com

What can the web do today?
https://whatwebcando.today/

Does service work run in background when browser is closed?
https://stackoverflow.com/questions/39201067/does-service-worker-runs-on-background-even-if-browser-is-closed

Use lighthouse cli to automate verification during build.
Who owns the standards?

https://www.w3.org/TR/appmanifest/
https://www.w3.org/TR/service-workers-1/
https://www.w3.org/TR/push-api/
Notification

Push
Safety Tip: Don’t send put your private key in source control!
Push standard only works in Chrome.  You will need to generate vapid keys for other browsers.

You don’t have to implement all features.  Your application can benefit from just a few.

Background sync is only available in desktop chrome at this time.  It is part of the service worker spec.
https://medium.freecodecamp.org/i-built-a-pwa-and-published-it-in-3-app-stores-heres-what-i-learned-7cb3f56daf9b
Microsoft Support
Adding your PWA to the Microsoft Store
https://docs.microsoft.com/en-us/microsoft-edge/progressive-web-apps/microsoft-store

Accessing Windows features from a Store Installed app
https://docs.microsoft.com/en-us/microsoft-edge/progressive-web-apps/windows-features



Build presentation by 
https://www.youtube.com/watch?v=6fb-t9ffDvo

- Want web apps on windows to be your best experience.
- Proliferation of web frameworks and tools makes building UWP apps as a PWA very attractive.
- Progressive store apps are first class citizens of the MS store - they want your pwa to be your windows store app
- Discovered or published to the store
-sonarwhal - Scans and tells you how you can make improvements to your site

Apple Support

Browser Comparison

Desktop - Safari, Edge, Chrome
