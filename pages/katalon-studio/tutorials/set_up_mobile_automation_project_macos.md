---
title: "Configuring Katalon Studio for Mobile Testing on macOS"
sidebar: katalon_studio_tutorials_sidebar
permalink: katalon-studio/tutorials/set_up_mobile_automation_project_macos.html
description: "Using Katalon Studio, mobile automation testers can design automation tests for both Android and iOS to run on physical devices, cloud services and emulators."
---
Using Katalon Studio, testers can design mobile app automation tests for both Android and iOS to run on physical devices, cloud services or emulators.

This tutorial explains how to set up a mobile app testing project for Katalon Studio on macOS. It assumes that you are familiar with automated testing.

Setup Prerequisites
-------------------

Katalon Studio requires the latest installation of [Appium](http://appium.io/) and [Node.js](https://nodejs.org/en/). Please follow these steps to setup:

*   Install [Homebrew](http://brew.sh/) from **Terminal**:

```groovy
/usr/bin/ruby -e "$(curl -fsSL
https://raw.githubusercontent.com/Homebrew/install/master/install)"

```

*   Install [Carthage](https://github.com/Carthage/Carthage) with **Homebrew**:

```groovy
brew install carthage

```

*   Install **node** and **npm** with **Homebrew**:

```groovy
brew install node
 
brew install npm

```

_NOTE_: To make sure **Node.js** is installed correctly, run the command **which node** on Terminal.

*   Install **Appium** with **npm**

| npm install -g appium |
| --- |

*   Set Appium Directory to **"/usr/local/lib/node_modules/appium"** in Katalon Preferences (from Katalon menu, go to **Preferences > Katalon > Mobile)**.

Install and configure [Xcode](https://developer.apple.com/xcode/) to test on iOS devices. Please set up Xcode as follows:

*   Open **Xcode > Preferences > Accounts**: Add developer's Apple ID.

![Add-acocunt-in-Xcode](../../images/katalon-studio/tutorials/set_up_mobile_automation_project_macos/Add-acocunt-in-Xcode.png)

*   Open Terminal at **WebDriverAgent** in Appium directory folder:_<…>/appium/node_modules/appium-xcuitest-driver/WebDriverAgent_ and enter following command to initialize **WebDriverAgent** project:

```groovy
mkdir -p Resources/WebDriverAgent.bundle
 
sh ./Scripts/bootstrap.sh -d

```

*   Open project **WebDriverAgent.xcodeproj** under**WebDriverAgent** in Xcode.

![Open-WebDriverAgent.xcodeproj](../../images/katalon-studio/tutorials/set_up_mobile_automation_project_macos/Open-WebDriverAgent.xcodeproj.png)

*   Select **WebDriverAgentLib**. In the Signing section, check **Automatically manage signing** and select a team.

![Select-target-WebDriverAgentLib](../../images/katalon-studio/tutorials/set_up_mobile_automation_project_macos/Select-target-WebDriverAgentLib.png)

*   On Xcode's menu bar, select **Product > Build**.

![Select-Build](../../images/katalon-studio/tutorials/set_up_mobile_automation_project_macos/Select-Build.png)

*   Repeat the last two steps for **WebDriverAgentRunner**.

*   Build **WebDriverAgent** to verify whether the steps above work.

| xcodebuild -project WebDriverAgent.xcodeproj -scheme WebDriverAgentRunner -destination 'id=<udid>' test |
| --- |

_NOTE_: <udid> is the device UDID of your mobile device.


*   If the following dialog is shown, select **Always Allow**.

![Always-allow](../../images/katalon-studio/tutorials/set_up_mobile_automation_project_macos/Always-allow.png)

*   You should be able to see _Listening on USB_ in the build output as below:

![Build-Output](../../images/katalon-studio/tutorials/set_up_mobile_automation_project_macos/Build-Output.png)

Setup Devices
-------------

For Android devices:

*   Turn on your Android device's developer mode (go to **Settings** \> **Developer options**).
*   Connect the device to your computer via a USB cable. If prompted, confirm to accept/trust the device.

For iOS devices:

*   Connect your iOS Devices to your computer via a USB cable. If prompted, confirm to accept/trust the device.
*   **For iOS 8 and higher**, enable the service UI automation on the device (connect the iOS device to Xcode) as follows:
    1.  Plug in the iOS device
    2.  Open Xcode on Mac
    3.  Go to **Settings** on the device > **Developer** \> turn ON **UIAutomation**
*   **For iOS 6 and higher**, on your iOS device go to **Settings > Safari > Advanced** and enable **Web Inspector**.

To test an iOS native application file (**.ipa** or **.app** file), make sure the file is already built and signed properly to deploy on the device. Follow these steps to check if an application file is already built and signed correctly:

1. Open **Xcode** and navigate to **Window/Devices**
2. Choose your device from the Devices list
3. Press the "+" button and choose your application file

![Choose-your-application-file](../../images/katalon-studio/tutorials/set_up_mobile_automation_project_macos/Choose-your-application-file.png)

4. If installed successfully, the application will appear in the Installed Apps section as shown below:

![Installed-successfully](../../images/katalon-studio/tutorials/set_up_mobile_automation_project_macos/Installed-successfully.png)

Desired Capabilities
--------------------

You can modify extra **Desired Capabilities** when executing automation tests in Katalon Studio.

To define Desired Capabilities for local execution using Chrome, Firefox, IE, Safari or Edge, please access **Project > Settings > Execution > Default > Mobile > iOS** (or Android).

The example below shows Desired Capabilities settings for Android to enable Unicode inputs.

![Desired-capabilities-setting](../../images/katalon-studio/tutorials/set_up_mobile_automation_project_macos/Desired-capabilities-setting-1024x673.png)

Refer to [Desired Capabilities](https://github.com/SeleniumHQ/selenium/wiki/DesiredCapabilities) to know which properties of each web browser are supported by Selenium. To use Desired Capabilities with Appium, refer to [Appium server capabilities](https://appium.io/docs/en/writing-running-appium/caps/).
