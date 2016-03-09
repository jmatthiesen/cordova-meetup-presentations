# Visual Studio TACO in 15 minutes
#Overview
Apache Cordova is an open-source framework that allows you to write apps for Android, iOS, Windows, and other mobile platforms, using nothing but HTML, CSS, and JavaScript. The apps built by Cordova are called hybrid apps - they aren't native apps and they aren't simple web apps, but a combination of both. Hybrid apps can have access to native device APIs and their layout rendering is done via Web views instead of the platform's native UI framework. 

To help you build apps using Cordova, Microsoft Visual Studio 2015 includes the Visual Studio Tools for Apache Cordova (also known as TACO). 

This tutorial takes you through the basics of Apache Cordova and Visual Studio TACO, by building a simple Getting Started app.

Want to see someone go through this demo? Check it out here (location TBD). 

## What will you learn in this session?
* Learn how to create a new Apache Cordova project in Visual Studio.
* Understand the basics of the Ionic framework, a popular JavaScript framework for Cordova developers.
* See how you can use Visual Studio to debug and test your app on Android, iOS, and Windows emulators and devices.

## Who is this session for?
This Quick Start Challenge is for any developer already familiar with Visual Studio. Prior experience with web development isn't needed, but the experience and languages will make more sense to you if you are a web developer. 

## What do you need to get started?
* Windows 10
* Install [Visual Studio 2015](http://www.visualstudio.com)
    * Include Apache Cordova features by following the [VS TACO Installation Guide](http://taco.visualstudio.com/en-us/docs/install-vs-tools-apache-cordova/)
    * Include the Visual Studio Emulator for Android feature
* [Ionic Project Templates for Visual Studio](https://visualstudiogallery.msdn.microsoft.com/4e44ba8b-a4c8-4106-b70e-00d63241a54a)
* (Optional) Setup iOS builds by following the [iOS Setup Guide](http://taco.visualstudio.com/en-us/docs/ios-guide/).

> **Note**: If you're going to use an existing Visual Studio 2015 installation, be sure you have the latest Updates to Visual Studio and TACO.

## Overview
Kick off with a crash course in basics. Use the Intro slide deck available at (TBD).
1. What is Apache Cordova?
1. How does it work?
1. What is Visual Studio?
1. What is TACO?
1. What does Visual Studio TACO do for you?

## Build a sample application
### Step 1: Create a new project in Visual Studio
First, launch Visual Studio 2015. Then, create a new project:

Select **Installed | Templates | JavaScript | Apache Cordova Apps | Ionic Tabs Template** as your project template.

![Ionic Tabs Template](/path/to/image)

Name the project and create it.

> **Note**: Ionic is a popular JavaScript framework built for Cordova development. You can learn more about it at [http://www.ionicframework.com](http://www.ionicframework.com).

You'll now see the default project structure in your solution explorer. A few things worth calling out here:
* The `www` folder is where your main app source code lives. In this template, `www/index.html` is the first screen of your app.
* `config.xml` is the Cordova configuration file.
* The `plugins` folder is a home for plugins that let you access native device capabilities.

### Step 2: Run the project in the browser
In the Debug Toolbar, choose the **Ripple - Nexus Galaxy** option to start debugging.

![Debug | Start Debugging](/path/to/image)

After the app is built, you will see the Google Chrome browser launch with your app contained in a mobile device simulator. This is the Ripple simulator. 

![App home page loaded in Ripple simulator](/path/to/image)

As you use the app in Ripple, you'll see messages similar to the following. You can choose the **Success!** button and the app will continue to work for testing. These dialogs appear because this template is using Cordova plugins that will work on an emulator or device, but will not work in Ripple.

![Dialog with "I Haz Cheeseburger?!?!" error](/path/to/image)

> **Note**: The Ripple simulator is available to use in Visual Studio for both iOS and Android development. Windows apps will be simulated natively in Windows.

You'll also see DOM Explorer and JavaScript Console windows opened in Visual Studio to help you debug the application.

![DOM Explorer and JavaScript Console windows](/path/to/image)



### Step 3: 

3. F5 run the Angular ToDo sample
4. Launch in Ripple - extension for Google Chrome that lets you simulate running an app on a device (we installed both Ripple and Chrome during initial setup)
5. Give overview of app
6. Set breakpoint in controller for addTodo (Story: I'm working on adding in video functionality and trying to analyze why it doesn't work)
7. Add a ToDo
8. Breakpoint hit
9. Make code change to fix error
    a. Show IntelliSense working
    b. Make change and stop
10. How that was done: Android Debug Bridge used to establish handshake with the app, Chrome Remote Debug Protocol then used as the format for communication to integrate diagnostics tools
	 
### Demo 2 - Run on a live device
1. Move to run on live device (Android Samsung)
1. Run
1. Show build output window:
  * We're using Node/NPM to acquire tools like the Cordova command line interface (CLI) dynamically
  * Building with the Cordova CLI
  * The Android build uses Ant, Java, and the Android SDK to build the apk that will be deployed to devices
  * Once built, the Android SDK is used to push the app over to the tethered device
1. Show DOM explorer opens
1. Select to inspect element
1. Hold up phone and touch on the screen, see how VS reacts
1. Show diagnostic tools hooked up
 
### Demo 3 - iOS build/deploy
1. Change device to iOS device
1. F5
1. Error, open
1. Show TypeScript type checking caught error
1. Fix error
1. Go to API definition, mention d.ts
1. F5
1. Switch to Mac, terminal window
1. Here a build agent as installed through NPM and has been waiting
1. See that build has started - VS passed along files to build
1. Converts apps into Cordova structure, runs Cordova build commands
1. App launches in iPhone simulator
1. Hold up iPad as well
 
I've just shown using Visual Studio to build Android and iOS apps using Cordova, with a set of emulators, on local devices, and in tandem with the Mac. We also support Windows and Windows Phone app development in this workflow, though I'm not showing that today.
