---
title: "Configuring Katalon Studio for Mobile Testing on Windows"
sidebar: katalon_studio_tutorials_sidebar
permalink: katalon-studio/tutorials/setting_mobile_application_automation.html
description: "Test automation for mobile app requires testing environment setup before performing any test. Learn how to perform mobile testing in Katalon Studio."
---
Test automation for mobile application requires users to setup a proper testing environment before performing any tests. To perform mobile testing in Katalon Studio, the following is required:

*   Node.js
*   Appium
*   Android/iOS device/emulator set up
*   AndroidSDK (packaged with Katalon Studio)

Follow this tutorial to set up an environment for mobile app automation on both Windows operating systems.

Installing Node.js
------------------

Navigate to URL '[https://nodejs.org/en/download/](https://nodejs.org/en/download/)' to download _Node.js_. Download the file according to the bit size of your operating system (32 bit or 64 bit) and install it.

For more details on how to install Node.js, please refer to [http://blog.teamtreehouse.com/install-node-js-npm-windows](http://blog.teamtreehouse.com/install-node-js-npm-windows).

To successfully use Katalon Studio for mobile app automation, it's required to run Node.js +6 and npm +3. To make sure you have the appropriate version of **Node** and **npm** installed, open Windows Command Prompt/MacOS Terminal and type node -v for Node and npm -v for npm.

![run Node.js in Katalon Studio](../../images/katalon-studio/tutorials/setting_mobile_application_automation/Install-Node.JS.png)

Installing Appium
-----------------

Open Command Prompt/Terminal and type the following command to install Appium:

**npm install –g appium**

To see if Appium was installed successfully, open Command Prompt/Terminal and type **appium**. This will show you the current version of your installed Appium (e.g: v1.6.5).

![Installing Appium in Katalon Studio](../../images/katalon-studio/tutorials/setting_mobile_application_automation/Install-Appium.png)

Setup the Appium directory after installation.

Setting Up the Appium Directory
-------------------------------

1.  Open Katalon Studio and go to **Window** Menu in the toolbar.
2.  Select **Katalon Studio Preferences > Katalon > Mobile**
3.  Set **Appium Directory** to the installed folder by browsing or pasting the path.

By default, it's usually installed at _C:\\Users\\{user login account}\\AppData\\Roaming\\npm\\node_modules\\appium._
