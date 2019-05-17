---
title: "Record Web Utility" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/record-web-utility.html 
redirect_from:
    - "/display/KD/Record+Web+Utility/"
    - "/display/KD/Record%20Web%20Utility/"
    - "/x/RwnR/"
    - "/katalon-studio/docs/record-web-utility/"
description: 
---
Record
------

### Record a New Test Case

*   Without opening any test case, click on **Web Record** icon to open Web Recorder. ![](../../images/katalon-studio/docs/record-web-utility/Screen-Shot-2018-06-27-at-09.41.37.png)
*   Google Chrome is Katalon Studio's default browser and the Chrome icon is displayed in the top right corner. You can change the default browser in **Preferences → Katalon → Recorder → Default browser**. You can also click on the drop-down button to select the browser you want to use:
    
    <table><thead><tr><th>Type</th><th>Description</th><th>Note</th></tr></thead><tbody><tr><td>New Browsers</td><td>Start a new browser</td><td><strong>Supported browsers:</strong><br>- Firefox<br>- Chrome<br>- Internet Explorer (only on Windows)</td></tr><tr><td>Active Browsers</td><td>Use the current browser (only Chrome)</td><td>Katalon Studio will install <a class="external-link" href="https://chrome.google.com/webstore/detail/katalon-recorder-selenium/ljdobmomdgdljniojadhoplhkpialdid" rel="nofollow">Katalon Recorder</a> as an add-on to help with recording for this type of browser<br><br><strong>Supported browsers:</strong><br>- Chrome<br>- Firefox (coming soon)</td></tr></tbody></table>
    
*   In this example, just select either Chrome or Firefox from '**New Browser**' type to start recording.
    
    > *   The browser will highlight and display its correspondent Xpath when you hover the mouse on that element.
    > *   Recorded steps will be generated in Recorded Actions.
    > *   When you type in a Password field, Web Recorder will automatically use '[Set Encrypted Text](/display/KD/%5BWebUI%5D+Set+Encrypted+Text)' keyword to encrypt the input's value and increase security.
    > 
    > ![](../../images/katalon-studio/docs/record-web-utility/Screen-Shot-2018-06-27-at-10.05.19.png)
    

### Record Using Existing Test Case

Creating a new test case whenever changes are made to the UI can be time-consuming. With the new Web Recorder, users can be more productive by modifying existing test cases, thereby minimizing any risks of overlooking how new changes might affect existing features. 

*   Open any existing Test Case you want to continue recording on.
*   Click on **Web Record** icon to open Web Recorder.
*   All the existing test steps will be imported as Recorded Actions and current [Test Case's variables](/display/KD/Variable+Types#VariableTypes-Localvariables) will be imported into the Variables tab in Web Recorder. You won't have to record the same test flow again.

![](../../images/katalon-studio/docs/record-web-utility/Screen-Shot-2018-06-27-at-11.23.30.png)

Modify Recorded Actions
-----------------------

Unlike the previous version of Web Recorder, the list of available actions is the same with Katalon Studio [built-in keywords](/display/KD/Built-in+Keywords). Add whatever actions you want depending on your requirements. You can call another test case and use Custom Keywords as well.

![](../../images/katalon-studio/docs/record-web-utility/Screen-Shot-2018-06-27-at-11.30.37.png)

Modify Recorded Objects
-----------------------

When the recording is complete, **Web Recorder** will export a list of test objects used in the test case. For more information on WebUI test objects, go [here](/x/tQTR). 

After creating your test case, click on **OK** to add the recorded steps to the test case. To continue, choose which directory to place your test objects. To help with optimization, Katalon Studio **automatically** **detects** similar **existing** objects in the Objects Repository and will ask you for further action.

![](../../images/katalon-studio/docs/record-web-utility/image2018-6-26-143A183A9.png)

Variables
---------

In the new Web Recorder interface, you can directly manage the [variables](/x/RoIw) directly related to your recording.

Execute
-------

We've added two new features that allows you to customize execution logs:

*   Logs: a real-time execution raw logs when you execute test steps. 
*   Run (with three types of run):
    *   Run all steps
    *   Run selected steps
    *   Run from selected step

![](../../images/katalon-studio/docs/record-web-utility/Screen-Shot-2018-06-27-at-11.46.04.png)

<table><thead><tr><th>Type of Run</th><th>Description</th></tr></thead><tbody><tr><td>Run all steps</td><td>Execute ALL steps that are enabled on Web Recorder.</td></tr><tr><td>Run selected steps</td><td><p>Execute only one or many selected steps.</p><blockquote class="important"><p>You can select many steps using either Ctrl or Shift key from your keyword. Selected steps will be highlighted e.g run step #2, #6, #9 and #11 are selected.</p><p><img src="../../images/katalon-studio/docs/record-web-utility/Screen-Shot-2018-06-27-at-11.45.48.png"></p></blockquote></td></tr><tr><td>Run from selected step</td><td><p>Execute the current selected step and all steps after selected one, e.g run step #4 and all steps after it.</p><p><img src="../../images/katalon-studio/docs/record-web-utility/Screen-Shot-2018-06-27-at-11.51.07.png"></p></td></tr></tbody></table>

After selecting any type of Run to execute, execution logs will be displayed in the Logs tab.

![](../../images/katalon-studio/docs/record-web-utility/Screen-Shot-2018-06-27-at-11.54.27.png)

> The steps above create and run a simple test case. For advanced features such as branching, looping or validation, refer to following articles: 
> 
> *   [Common Validation](https://www.katalon.com/tutorials/common-validation/) 
> *   [Control Statements](/display/KD/Control+Statements)
