# About this project "FinalProject"
An app telling a joke with multiple flavors that uses multiple libraries and Google Cloud Endpoints. The free procut flavor has ad inside the APP but the paid product flavor doesn't.

## As a developer, what I used to build this project:
-   Add free and paid flavors to an app, and set up the build to share code between them
-   Set a banner ad inside the the mainActivity of the free app by implementing the admob sdk
-   Factor reusable functionality into a Java library
-   Factor reusable Android functionality into an Android library
-   Configure a multi-project build to compile the libraries and app
-   Use the Gradle App Engine plugin to deploy a backend
-   Configure an integration test suite that runs against the local App Engine development server

## Why this Project

As Android projects grow in complexity, it becomes necessary to customize the behavior of the Gradle build tool, allowing automation of repetitive tasks. Particularly, factoring functionality into libraries and creating product
flavors allow for much bigger projects with minimal added complexity.

## Overview
- Project Overview  
The multi-project build will look something like this. Proceed to the next slide for specific instructions.
<img align="center" src="https://github.com/mcf1727/FinalProject/tree/master/photos">

- The App consists of four modules:  
1.  A Java library that provides jokes
2.  A Google Cloud Endpoints (GCE) project that serves those jokes
3.  An Android Library containing an activity for displaying jokes
4.  An Android app that fetches jokes from the GCE module and passes them to the Android Library for display

- Start or stop your local server
Select the "appengineStart" or "appengineStop" gradle tasks in the foler "app engine standard environment" of "backend".

- Build a release
Before build a release apk, you need to go to "build.gradle" of app level to enter your signingconfigs information in order to configure automatic signing.