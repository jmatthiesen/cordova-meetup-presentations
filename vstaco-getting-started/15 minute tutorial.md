# Visual Studio TACO in 15 minutes
This tutorial takes you through the basics of Apache Cordova and Visual Studio TACO, including making a simple Getting Started app. All of that, in 15 minutes.

Got more time? See the 45 minute tutorial (location TBD).

Want to see someone go through this demo? Check it out here (location TBD). 

## Pre-requisites
### Setup Mac Builds
Don't have a Mac? Consider using [MacInCloud](http://www.macincloud.com).

## Overview
Kick off with a crash course in basics. Use the Intro slide deck available at (TBD).
1. What is Apache Cordova?
1. How does it work?
1. What is Visual Studio?
1. What is TACO?
1. What does Visual Studio TACO do for you?

## Build a sample application
### Demo 1 - Show the app in a browser
1. Use an Ionic template to get started
1. Open controllers.js
2. Set launch target to Ripple
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
