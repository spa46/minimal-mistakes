---
title: "Mobile: Ionic Framework"
header:
  image: main_doc1_1024.jpg
  teaser: iphone.jpg
  caption: "Photo credit: [**pixabay**](https://pixabay.com)"
tag: 
  - Ionic
  - Ionic setup
  - Ionic framework
  - IOS
  - Android
  - Mobile App
  - Mobile WebApp
  - Mobile Application
categories: 
  - Web & Mobile

author_profile: true
---

{% include toc %}

# Ionic
Ionic is a complete open-source SDK for hybrid mobile app development built on top of AngularJS and Apache Cordova. this helps developing hybrid mobile apps using Web technologies like CSS, HTML5, and Sass. 

# Cons & Pros

The purpose of using Ionic is that I can deploy both Android and IOS; furthermore even web, within same code.
So it would save my time to develop apps. However, generally, people say that this is bit slower than native apps.


# Type
Ionic supports two types: `Ionic1` and `Ionic2`. <br> 
Ionic 1 based on Angular 1 where Ionic 2 based on Angular 2

The advantage of Ionic 1:
	
	More classic than Ionic 1.
	Older than Ionic 2, so bit more stable.

The advantage of Ionic 2 over Ionic 1 is:

	Angular 2 is faster
	Angular2 use components instead of controller (developer feels simpler)
	Angular2 has simpler directive
	intuitive data binding

# Requirements

- download **ionic**: <br>
	[http://ionicframework.com/docs/overview/#download](http://ionicframework.com/docs/overview/#download "http://ionicframework.com/docs/overview/#download")

- download **nodejs**: <br>
	[https://nodejs.org/en/download/](https://nodejs.org/en/download/ "https://nodejs.org/en/download/")

- download **cordiva** npm package: (to support multi-platform)<br>  

		npm install -g cordova

- download **gulp** npm package: (ionic's build system)<br>

		npm install -g gulp

- download **bower** npm package: (to bring web components)<br>

		npm install -g bower

- For a simulation,<br> 
  download **ios-sim**: (for an ios simulation) <br>

		npm install -g ios-sim

- download **ios-deploy**: (for installation or debugging) <br>

	 	npm install -g ios-deploy
		
		if this is unable to install, try this:
			sudo npm install -g ios-deploy --unsafe-perm=true

First of all, tried OS X (Yosemite) installation on virtual machine, but was unstable (hang while booting and etc). Therefore, for second, "El Capitan" was installed; however, after few hours of using it, it has been realized that running both Android and IOS on OS X on top of virtual machine is difficult. Therefore, it is recommended to have Macbook pro for mobile and web development.   

# El Capitan Installation reference for Virtual box

To give you a guide to install "El Capitan", please refer to below. 

English    
> https://techsviewer.com/how-to-install-mac-os-x-el-capitan-on-pc-on-virtualbox/

Korean
> http://weixing.tistory.com/289

on the OS, you must have followings (need to be installed using npm):

- brew
- nodejs

# Full Screen for OS X

If you do not see OS in Full screen, try below:
 
	VBoxManage setextradata "VM name" VBoxInternal2/EfiGopMode N
    Where N can be, 

	0 – 640×480
	1 – 800×600
	2 – 1024×768
	3 – 1280×1024
	4 – 1440×900
	5 – 1920×1200 

Or,

	VBoxManage setextradata "El Capitan" CustomVideoMode1 1920x1080x32 

## XCode Installation Issue

Issue related to "**Simulator can't be opened**":
Click [Here](http://stackoverflow.com/questions/33413180/xcode-7-1-simulator-cant-be-opened-because-the-identity-of-developer-cannot-b)


## Test Ionic

1. `sudo ionic run ios --device`

2. Select a target: `ionic emulate ios --target="iPhone-4s"`

3. Change mode of directory to run the Ionic file: `sudo chmod -R 777 *`


## Reference:
http://blog.saltfactory.net/ionic/start-ionic-edge-book.html (Korean)