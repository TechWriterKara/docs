---
title: "View Execution Log" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/view-execution-log.html 
description: 
---
Once your test cases/test suites finish execution, you can review the results on the **Log Viewer** views.

![](../../images/katalon-studio/docs/view-execution-log/image2017-6-30 21_25_13.png)

Using the filter options, you can specify what type of logs to be displayed:

<table class="wrapped confluenceTable"><colgroup><col><col></colgroup><tbody><tr><th class="confluenceTh"><p><strong>Filter</strong></p></th><th class="confluenceTh"><p><strong>Description</strong></p></th></tr><tr><td class="confluenceTd"><p>All</p></td><td class="confluenceTd"><p>Show all the log messages.</p></td></tr><tr><td class="confluenceTd"><p>Info</p></td><td class="confluenceTd"><p>Show only the log messages for information/reference.</p></td></tr><tr><td class="confluenceTd"><p>Passed</p></td><td class="confluenceTd"><p>Show only the log messages indicating that a step is successfully executed.</p></td></tr><tr><td class="confluenceTd"><p>Failed</p></td><td class="confluenceTd"><p>Show only the log messages indicating that a test step is failed to execute.</p></td></tr><tr><td class="confluenceTd"><p>Error</p></td><td class="confluenceTd"><p>Show only the log messages indicating that some error has occurred at a given step.</p></td></tr><tr><td colspan="1" class="confluenceTd">Warning</td><td colspan="1" class="confluenceTd">Show only the log messages indicating that a test step is failed but accepted as warning.</td></tr><tr><td colspan="1" class="confluenceTd">Not Run</td><td colspan="1" class="confluenceTd">Show only the log messages indicating that a test step is skipped.</td></tr></tbody></table>

Standard view vs. Tree View
---------------------------

The **Log Viewer** can be viewed in different modes: **standard** view and **tree** view. You can switch to tree view by selecting the **Tree View** toggle as illustrated below:

![](../../images/katalon-studio/docs/view-execution-log/image2017-6-30 21_26_35.png)

The **Tree View** display logs in a structural way that relates to how the test case/test suite organized. Additionally, users can now navigate to the respective step by selecting from the context menu as showed below:

![](../../images/katalon-studio/docs/view-execution-log/image2017-6-23 15_55_57.png)

Scroll Lock
-----------

While the test is being executed, the **Log Viewer** will be updated with real-time log messages, where the most recent log message is shown at the bottom of the view. Therefore, the **Log Viewer** is kept scrolling down during the test execution. However, users may want to keep the **Log Viewer** standing still so that they can verify certain log message. In order to stop this scrolling behavior, you can select **Scroll Lock**.

![](../../images/katalon-studio/docs/view-execution-log/image2017-6-30 21_27_35.png)