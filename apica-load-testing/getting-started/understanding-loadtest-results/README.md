# Understanding Loadtest Results

The **Results** view is accessible for completed jobs and provides access to all information collected during a test run. It also allows you to compare different instances with each other:

<figure><img src="../../../.gitbook/assets/8ccb0643-3f2f-4bb8-b2f1-ac338914e0ef.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/50a8fe5d-ae75-47d8-9075-c5e29e480168.png" alt=""><figcaption></figcaption></figure>

## Result Details <a href="#understandingloadtestresults-resultdetails" id="understandingloadtestresults-resultdetails"></a>

The **Result Details** tab contains a number of charts which provide metrics related to the performance of the Load Test. It displays the metrics for a specific Test Result within the Test Instance you are viewing. It contains a header which displays the Concurrent Users which were specified when the test was configured. It also displays the start and end times of the Test. Select the Test Result to view by selecting a number of users from the “Users” dropdown; the metrics displayed on the charts are specific to the test run which was selected. The charts can be manipulated to show or hide additional data, printed, or expanded to provide a better view of the chart; see [Understanding Load Test Result Charts](broken-reference) for more details.

The following screenshot shows metrics for a Test Result which ran a .class file with 2 users (the .class file name has been obfuscated). Response times can be compared to the number of Active Users - virtual users who have started but not yet finished the Test.

<figure><img src="../../../.gitbook/assets/411c4f5f-1065-4146-b34c-1b38afd9ae26.png" alt=""><figcaption></figcaption></figure>

## Pages & URLs <a href="#understandingloadtestresults-pages-and-urls" id="understandingloadtestresults-pages-and-urls"></a>

The **Pages & URLs** tab shows detailed data about URL and page response times, and provides access to response time breakdowns.

<figure><img src="../../../.gitbook/assets/a61099e3-a7b3-4b5d-9195-211201b75dd0.png" alt=""><figcaption></figcaption></figure>

This page contains detailed results for each individual URL call in the test.&#x20;

### Instance <a href="#understandingloadtestresults-instance" id="understandingloadtestresults-instance"></a>

The **Instance** section shows basic information about the test.

<figure><img src="../../../.gitbook/assets/647cd425-cf58-4195-bc0e-e11a42ffc17e (1).png" alt=""><figcaption></figcaption></figure>

| Item                    | Description                                                                                                                                |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
|  Concurrent Users       | Number of [Users](https://apica-kb.atlassian.net/wiki/spaces/ASMDOCS/pages/4632035/Virtual+User).                                          |
|  Test Sequence Times    | Start and end for the test sequence run.                                                                                                   |
| Create Quick PDF Report | Button to [Quick Report](https://apica-kb.atlassian.net/wiki/pages/createpage.action?spaceKey=DMT\&title=Quick%20Report) form the results. |

### Results <a href="#understandingloadtestresults-results" id="understandingloadtestresults-results"></a>

In the **Results** section you can select which run to display in the charts and tables. Each run in the instance is indicated by a tab showing the number of users.

<figure><img src="../../../.gitbook/assets/10683edc-8bc1-4516-a315-74e2ed282f39.png" alt=""><figcaption></figcaption></figure>

By default, information about all runs is displayed:

<figure><img src="../../../.gitbook/assets/9c0065c1-08b7-45cf-a296-8ec209e7fb62.png" alt=""><figcaption></figcaption></figure>

To select a specific run, click the tab with the desired number of users:

<figure><img src="../../../.gitbook/assets/700bed82-a591-48e0-b43e-64edd81174ba (1).png" alt=""><figcaption></figcaption></figure>

The table corresponding to the run is shown in the [Pages & Urls](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5672450/Table) section.

## Errors <a href="#understandingloadtestresults-errors" id="understandingloadtestresults-errors"></a>

Errors show detailed information about any possible errors if any have occurred.

<figure><img src="../../../.gitbook/assets/dd643915-5d23-4020-acb0-628180a90952.png" alt=""><figcaption></figcaption></figure>

## Instance <a href="#understandingloadtestresults-instance.1" id="understandingloadtestresults-instance.1"></a>

The **Instance** section shows basic information about the test.

<figure><img src="../../../.gitbook/assets/2177466677.png" alt=""><figcaption></figcaption></figure>

| Item                    | Description                                                                                                                        |
| ----------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
|  Concurrent Users       | Number of [users](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5672993/Virtual+User).                                  |
|  Test Sequence Times    | Start and end for the test sequence run.                                                                                           |
| Create Quick PDF Report | Button to [create a PDF report](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5674012/QRQuick+Report) form the results. |

## Error Overview <a href="#understandingloadtestresults-erroroverview" id="understandingloadtestresults-erroroverview"></a>

The **Error Overview** table shows the number of errors per page and test.

<figure><img src="../../../.gitbook/assets/62c5dd83-7f1b-417e-a7da-4e8ed75d9b1a.png" alt=""><figcaption></figcaption></figure>

Each page is a row in the table, with a column for each test.

This view allows you to see which tests contain errors and select them for display in the details chart and table.

## Chart <a href="#understandingloadtestresults-chart" id="understandingloadtestresults-chart"></a>

The **Errors Over Time** chart shows error occurrences during the test for the selected location.

<figure><img src="../../../.gitbook/assets/9d103bb2-ba7a-40fe-9289-b28ded1ce018.png" alt=""><figcaption></figcaption></figure>

The chart shows the number of errors during the test for the selected test.

**Select Test**

To display the chart, you need to select the test in the dropdown menu.

<div align="left">

<figure><img src="../../../.gitbook/assets/af02d069-b16a-457c-b31b-368ec2f98f71 (2).png" alt=""><figcaption></figcaption></figure>

</div>

## Live Error Feed <a href="#understandingloadtestresults-liveerrorfeed" id="understandingloadtestresults-liveerrorfeed"></a>

The **Live Errors Feed** table shows information about the last recorded errors [chart](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5672165/Chart).

<figure><img src="../../../.gitbook/assets/af80bd3d-e311-4bc1-85d6-dddb19eea1e3.png" alt=""><figcaption></figcaption></figure>



| Column      | Description                                                                                                                                            |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Page        | Page order number and name in scenario.                                                                                                                |
| URL         | [HTTP Methods](https://apica-kb.atlassian.net/wiki/pages/createpage.action?spaceKey=GLOS\&title=HTTP%20Methods) and URL associated with the error.     |
| URL Index   | Error number relative to the URL.                                                                                                                      |
| Time Offset | Time when the error occured, relative to the start of test.                                                                                            |
| Error Type  | [HTTP Status Codes](https://apica-kb.atlassian.net/wiki/pages/createpage.action?spaceKey=GLOS\&title=HTTP%20Status%20Codes) and message for the error. |
| Actions     | Buttons for possible actions to perform on the error.                                                                                                  |

**Actions**

| Column | Action  | Description                                                                                        |
| ------ | ------- | -------------------------------------------------------------------------------------------------- |
|        | Details | Open the [Error Details](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5673614) dialog. |

## Error Details <a href="#understandingloadtestresults-errordetails" id="understandingloadtestresults-errordetails"></a>

The **Error Details** dialog provides access to a number of tabs containing detailed information relating to the error.

<figure><img src="../../../.gitbook/assets/af0b0dad-3fe5-4634-8171-07078bc66a70.png" alt=""><figcaption></figcaption></figure>

### Summary <a href="#understandingloadtestresults-summary" id="understandingloadtestresults-summary"></a>

The **Summary** section shows the received content of the response.

<figure><img src="../../../.gitbook/assets/b9d11eb4-b718-44b6-b116-1a9016c035ac.png" alt=""><figcaption></figcaption></figure>

| Row                           | Description                                                                                                                     |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| Page                          | Page order number and name in scenario.                                                                                         |
| Error Data                    | Time when error occured: Timestamp, time after start (number of seconds, and converted time).                                   |
| URL                           | [HTTP Method](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5672816/HTTP+Methods) and URL associated with the error. |
| URL Exec Step                 | Execution step when error occured.                                                                                              |
| Exec Agent Socket Create Time | Creation time for the execution agent connection.                                                                               |
| TCP Connection Reuse Count    | Number of reuses of the TCP connection.                                                                                         |
| TCP Local Address             | TCP local IP address.                                                                                                           |
| TCP Local Port                | Local port for TCP connection.                                                                                                  |
| Remote TCP Address            | TCP remote address.                                                                                                             |
| TCP Remote Port               | Remote port for TCP connection.                                                                                                 |
| SSL Session Id                | Session ID for [SSL](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5673458/Ssl) connection.                          |
| Error Log                     | Scrollable log view. Clicking the header opens the full log in a separate browser window.                                       |

### Log <a href="#understandingloadtestresults-log" id="understandingloadtestresults-log"></a>

The log in the [Summary](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5672038/Summary) section can be viewed in a separate browser tab.

<figure><img src="../../../.gitbook/assets/196b4a72-d0de-4a27-a5d2-a360b1a3432c.png" alt=""><figcaption></figcaption></figure>

### Request <a href="#understandingloadtestresults-request" id="understandingloadtestresults-request"></a>

In the **Request Headers** tab, information about the request preceding the error is displayed.

<figure><img src="../../../.gitbook/assets/47f76ae1-6e89-4c2b-aa21-382f0f6ecafd.png" alt=""><figcaption></figcaption></figure>

The table displays the [HTTP Methods](https://apica-kb.atlassian.net/wiki/pages/createpage.action?spaceKey=GLOS\&title=HTTP%20Methods) and URL associated with the error at the top. Following that is a table containing all headers sent with the request.

### Request Content <a href="#understandingloadtestresults-requestcontent" id="understandingloadtestresults-requestcontent"></a>

The **Request Content** tab shows the sent content of the request if any exists.

<figure><img src="../../../.gitbook/assets/b3e1b7dd-7e78-459a-b75e-b8f3080030b1.png" alt=""><figcaption></figcaption></figure>

### Response Headers <a href="#understandingloadtestresults-responseheaders" id="understandingloadtestresults-responseheaders"></a>

The **Response Headers** tab shows the received response headers.

<figure><img src="../../../.gitbook/assets/4b15566c-d9a5-4515-87af-9faf3a2ca2be.png" alt=""><figcaption></figcaption></figure>

The table displays the [HTTP Status Codes](https://apica-kb.atlassian.net/wiki/pages/createpage.action?spaceKey=GLOS\&title=HTTP%20Status%20Codes) and text error at the top.

Following that is a table containing all headers provided in the response.

### Response Content <a href="#understandingloadtestresults-responsecontent" id="understandingloadtestresults-responsecontent"></a>

The **Response Content** tab, shows the received content of the response, if any.

<figure><img src="../../../.gitbook/assets/e9f8602e-165e-47f3-98c6-ebc77ecd90f1.png" alt=""><figcaption></figcaption></figure>

To view the content in a browser, click “Preview Response Content”. Your default browser opens to display the content:

<figure><img src="../../../.gitbook/assets/380adb18-7b93-43bd-bc50-da8dee888c1a.png" alt=""><figcaption></figcaption></figure>

## Integrations <a href="#understandingloadtestresults-integrations" id="understandingloadtestresults-integrations"></a>

Depending on which integrations you have enabled, various integration tabs may be available as part of the results view.

## Transactions <a href="#understandingloadtestresults-transactions" id="understandingloadtestresults-transactions"></a>

The Transactions tab presents information about [User Defined Transactions](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5673126/User-Defined+Transactions).

<figure><img src="../../../.gitbook/assets/5e430a14-d4e6-4fd1-912e-e563b6a74410 (1) (1).png" alt=""><figcaption></figcaption></figure>

## Summary <a href="#understandingloadtestresults-summary.1" id="understandingloadtestresults-summary.1"></a>

The **Transactions Summary** table shows an overview of the transactions for a selected result.

<figure><img src="../../../.gitbook/assets/5c660827-d2a1-4698-a667-01685c597bc2.png" alt=""><figcaption></figcaption></figure>

With the **All Transaction Times Percentile** chart, you get a _statistical_ view of how the transaction times are distributed.

<div align="left">

<figure><img src="../../../.gitbook/assets/304aadca-21e5-4517-ab70-86938f655781.png" alt=""><figcaption></figcaption></figure>

</div>

The **All Transaction Times** chart shows the transaction _times_ for the selected transaction.

<div align="left">

<figure><img src="../../../.gitbook/assets/6006efa2-ab16-4e4f-97f3-63d64756d42f (2).png" alt=""><figcaption></figcaption></figure>

</div>

In the **Full Passed Transaction Times Percentile** chart, you get a statistical view of how the transaction times are distributed for the passed transactions.

<div align="left">

<figure><img src="../../../.gitbook/assets/d4778b08-e102-4753-83f5-d9d72fa8f16d (1).png" alt=""><figcaption></figcaption></figure>

</div>

## Settings Used <a href="#understandingloadtestresults-settingsused" id="understandingloadtestresults-settingsused"></a>

The **Settings Used** tab shows a summary of all settings used for a load test.

<figure><img src="../../../.gitbook/assets/3e5239b0-de51-455e-bb32-dfac77c8bb56 (1).png" alt=""><figcaption></figcaption></figure>

### Instance <a href="#understandingloadtestresults-instance.2" id="understandingloadtestresults-instance.2"></a>

The **Instance** section shows basic information about the test.



| Concurrent Users            | Number of [Users](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5672993/Virtual+User).                           |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| Test Sequence Times         | Start and end for the test sequence run.                                                                                    |
| **Create Quick PDF Report** | Button to the [Quick Report](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5674012/QRQuick+Report) form results. |

### Results <a href="#understandingloadtestresults-results.1" id="understandingloadtestresults-results.1"></a>

In the **Results** section, you can select which run to display.

To select a specific result set:

* Click the tab with the desired number of users

**The Settings Used tab shows a summary of all settings used for a load test.**

| **Item**                                     | **Description**                                                                                                                                                                                                |
| -------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Scenario**                                 |                                                                                                                                                                                                                |
| Scenario                                     | Scenario used in the job.                                                                                                                                                                                      |
| **Loadtest Options**                         |                                                                                                                                                                                                                |
| Number of Concurrent Users                   | Number of [virtual users](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5672993/Virtual+User) in the test.                                                                                          |
| Loadtest Duration                            | Total duration of the test.                                                                                                                                                                                    |
| Rampup Time                                  | Time to [ramp-up](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5673372/Ramp-Up).                                                                                                                   |
| Run Multiple Sequential Tests                | Used [execution mode](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5673008/Execution+Mode).                                                                                                        |
| **Location**                                 |                                                                                                                                                                                                                |
| Cluster                                      | Location [cluster(s) ](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5673283/C+Cluster)used to generate load.                                                                                       |
| **Scenario Options**                         |                                                                                                                                                                                                                |
| User input Text Files                        | Connected [input file(s)](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5672770/I+Input+Files).                                                                                                     |
| User Defined Vars                            | Variables defined in the scenario.                                                                                                                                                                             |
| **Advanced Options**                         |                                                                                                                                                                                                                |
| Max Loops Per User                           | Maximum number of [loops ](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5673133/Load+Testing+Loop)per [users](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5672993/Virtual+User).      |
| Request Timeout (sec)                        | Time to wait for responses.                                                                                                                                                                                    |
| Additional Options                           | Additional command line options provided as part of the job.                                                                                                                                                   |
| Distribute Load on All Available Datacenters | Enabled [load distribution](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5673136/Load+Distribution)                                                                                                |
| **Client Options**                           |                                                                                                                                                                                                                |
| User Agent                                   | Client [User-Agent](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5673101/User-Agent).                                                                                                              |
| **Network Bandwidth Downlink (Mbit/s):**     |                                                                                                                                                                                                                |
| Desktop                                      | Limit on downloaded desktop traffic.                                                                                                                                                                           |
| Mobile                                       | Limit on downloaded mobile traffic.                                                                                                                                                                            |
| **Network Bandwidth Uplink (Mbit/s):**       |                                                                                                                                                                                                                |
| Desktop                                      | Limit on uploaded desktop traffic.                                                                                                                                                                             |
| Mobile                                       | Limit on uploaded mobile traffic.                                                                                                                                                                              |
| Client Side Monitoring                       | Enabled [Client Side Monitoring](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5673298/Client+Side+Monitor).                                                                                        |
| **DNS**                                      |                                                                                                                                                                                                                |
| DNS Hosts file                               | Custom [hosts file](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5672827/HOSTS+File).                                                                                                              |
| DNS Server                                   | Custom [DNS server](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5673215/DNS+Server) used for lookups.                                                                                             |
| Resolve DNS for Each Executed Loop           | Whether [DNS ](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5673211/D+DNS)lookup is performed for each [loop](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5673133/Load+Testing+Loop). |
| DNS Translation file                         | Custom [DNS server](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5673215/DNS+Server) translation file used.                                                                                        |
| **Reporting**                                |                                                                                                                                                                                                                |
| Email Preliminary Report To                  | Address for test reports.                                                                                                                                                                                      |
| Reporting History                            | Limit on number of tests to include in test history.                                                                                                                                                           |
| **Execution**                                |                                                                                                                                                                                                                |
| Schedule                                     | Type of scheduling for the job.                                                                                                                                                                                |
| Schedule Date                                | Date for schedule.                                                                                                                                                                                             |
| **Test Information**                         |                                                                                                                                                                                                                |
| Attached to Project                          | Project the test belongs to.                                                                                                                                                                                   |
| Job Comment                                  | Comments added to the job settings.                                                                                                                                                                            |
| Tags                                         | Scenario Tags applied to the scenario.                                                                                                                                                                         |

&#x20;

## Client Side Monitoring <a href="#understandingloadtestresults-clientsidemonitoring" id="understandingloadtestresults-clientsidemonitoring"></a>

If the job uses **Client Side Monitoring**, this tab shows real browser rendering times corresponding to the behavior of a real user accessing the application during the load test.

<figure><img src="../../../.gitbook/assets/c7d84bd1-a8bd-4417-b73e-28874c627e8c (1).png" alt=""><figcaption></figcaption></figure>

You will be able to see the total Response Time measured from a real browser for each separate run on this page.

## Instance Results <a href="#understandingloadtestresults-instanceresults" id="understandingloadtestresults-instanceresults"></a>

The **Instance** section shows basic information about the test:

<figure><img src="../../../.gitbook/assets/ecba58d9-e65a-462f-8c6c-c85fe05262e8.png" alt=""><figcaption></figcaption></figure>

| **Item**                | **Description**                                                                                                                            |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
|  Concurrent Users       | Number of [Users](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5672993/Virtual+User).                                          |
|  Test Sequence Times    | Start and end for the test sequence run.                                                                                                   |
| Create Quick PDF Report | Button to the [Quick Report](https://apica-kb.atlassian.net/wiki/pages/createpage.action?spaceKey=DMT\&title=Quick%20Report) form results. |

## Results <a href="#understandingloadtestresults-results.2" id="understandingloadtestresults-results.2"></a>

In the **Results** section, you can select which run to display in the charts and tables.

<figure><img src="../../../.gitbook/assets/26611430-af24-4d41-b9ed-53a90b38efca (1).png" alt=""><figcaption></figcaption></figure>

To select a specific result set:

* Click the tab with the desired number of users

## Location Overview Chart <a href="#understandingloadtestresults-locationoverviewchart" id="understandingloadtestresults-locationoverviewchart"></a>

For each location, a **Location Overview** chart displays a graph containing the page response times and the number of URL errors for all runs.

Select the desired location, e.g. Los Angeles, from the dropdown menu to pick which location to show in the chart.

<div align="left">

<figure><img src="../../../.gitbook/assets/7f5b439f-ddb3-4fee-9a6b-ac66cae2f411.png" alt=""><figcaption></figcaption></figure>

</div>

<figure><img src="../../../.gitbook/assets/3442456b-10d9-4326-bfbc-01dc2ab2bc23.png" alt=""><figcaption></figcaption></figure>

The chart shows the page response times and the number of URL errors overall runs for the selected location.

## Run Details <a href="#understandingloadtestresults-rundetails" id="understandingloadtestresults-rundetails"></a>

The **Run Details** shows information about the run and provides access to related screenshots.

<figure><img src="../../../.gitbook/assets/1c7ecce5-6f16-4346-a4c8-38d3bd27f42b (1).png" alt=""><figcaption></figcaption></figure>

The run details contain a timestamp for when the test started (with offset showing time elapsed from the start of test in parentheses).

If screenshots are available, a link to open them for viewing is also shown.

#### Snapshot <a href="#understandingloadtestresults-snapshot" id="understandingloadtestresults-snapshot"></a>

To see the screenshots:

* Click the **View Screenshot** link.

The screenshots are displayed as an overlay on your browser:

<figure><img src="../../../.gitbook/assets/a485b80b-094e-4c50-b2dc-0f191bea3340.png" alt=""><figcaption></figcaption></figure>

The snapshots provide a browser view of the page at the time the URL occurred.

**Navigate**

When you hover the mouse over the left or right side of the snapshot, navigation buttons are shown, allowing you to browse through multiple snapshots, if available.

## Select Run <a href="#understandingloadtestresults-selectrun" id="understandingloadtestresults-selectrun"></a>

The **Select Run** dropdown menu allows you to pick which test run to show in the run [Run Details ](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5672721/Run+Details)and Pages sections

<div align="left">

<figure><img src="../../../.gitbook/assets/1d0dbd6b-b21c-43d9-b4b2-782d19ddf6ca.png" alt=""><figcaption></figcaption></figure>

</div>

## URL Errors <a href="#understandingloadtestresults-urlerrors" id="understandingloadtestresults-urlerrors"></a>

The **URL Errors** table shows any errors that have occurred for the page during the test.

<figure><img src="../../../.gitbook/assets/e79632c5-1445-4731-8c2c-6e886bb41d72.png" alt=""><figcaption></figcaption></figure>

Each URL is displayed as a row in the table.

| **Column** | **Description**                          |
| ---------- | ---------------------------------------- |
| #          | ID number.                               |
| Code       | Error code, if any.                      |
| URL        | URL associated with the error.           |
| Time       | Time elapsed from the start of the test. |
| Error      | Error message.                           |

## Pages <a href="#understandingloadtestresults-pages" id="understandingloadtestresults-pages"></a>

The **Pages** table(s) shows information about the page(s) in the test and the URLs called for each page during the test run.

<figure><img src="../../../.gitbook/assets/5c3fe39e-df17-4139-b832-67e0affe9953.png" alt=""><figcaption></figcaption></figure>



Each page is displayed in a table, with URLs displayed in rows:

| **Column**       | **Description**                                 | **Comment**                                                                                                                              |
| ---------------- | ----------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| URL              | Called URL.                                     |                                                                                                                                          |
| Time             | Time until received response.                   |                                                                                                                                          |
| Size             | Response size.                                  |                                                                                                                                          |
| More Information | Show more information about the URL.            | Click to see [more information](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5672502/V+More+Information) about the response. |
|  0s, 1s, 2s….    | Graphical representation of the response times. |  Click to see [timing details](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5672499/V+URL+Details).                          |

## The “More Information” Column <a href="#understandingloadtestresults-the-moreinformation-column" id="understandingloadtestresults-the-moreinformation-column"></a>

More information about the response is available for each URL. To see more information about a particular URL, click the “See More” link. A popup containing details about the URL is shown:

<div align="left">

<figure><img src="../../../.gitbook/assets/a3e824be-7f04-457e-8abc-20bf45bcf3ad.png" alt=""><figcaption></figcaption></figure>

</div>

| **Item**      | **Description**                                                                                                                       |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| Mime Type     | [MIME Type](https://apica-kb.atlassian.net/wiki/pages/createpage.action?spaceKey=GLOS\&title=MIME%20Type) for the response message.   |
| HTTP Response | Response [HTTP Status Codes](https://apica-kb.atlassian.net/wiki/pages/createpage.action?spaceKey=GLOS\&title=HTTP%20Status%20Codes). |
| Error Message | Returned error message (if the URL is associated with an error).                                                                      |

## View Details <a href="#understandingloadtestresults-viewdetails" id="understandingloadtestresults-viewdetails"></a>

To see the timing details about a particular URL:

* Click the **representation** for the desired URL

A popup containing details about the URL is shown:

<div align="left">

<figure><img src="../../../.gitbook/assets/b0c2b083-42ef-4505-8247-7356acd49f5e.png" alt=""><figcaption></figcaption></figure>

</div>

Information about the HTTP call is shown at the top.

| Item          | Description                                                                                                                           |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| HTTP Response | Response [HTTP Status Codes](https://apica-kb.atlassian.net/wiki/pages/createpage.action?spaceKey=GLOS\&title=HTTP%20Status%20Codes). |
| Error Message | Returned error message (if the URL is associated with an error).                                                                      |

The **Response Time Details** section shows a graphical representation of the flow and a legend with times.

| Item                                                                                                          | Description       |
| ------------------------------------------------------------------------------------------------------------- | ----------------- |
| <img src="../../../.gitbook/assets/5c480845-b98b-428a-8374-ebab436c6ce1 (1).png" alt="" data-size="original"> |  Blocked          |
| ![](<../../../.gitbook/assets/dc01a085-d8a2-49ca-b0d3-c146c6826a5c (1).png>)                                  |  Connect Duration |
| ![](../../../.gitbook/assets/e5ee070f-722a-45b0-b56d-99dfc81db5bc.png)                                        |  Send Duration    |
| <img src="../../../.gitbook/assets/bee82ae5-7fda-443b-9552-e87e5ed836a7.png" alt="" data-size="original">     |  Wait Duration    |
| ![](../../../.gitbook/assets/b90adfbf-11bf-40af-a8ed-daadb481ab1e.png)                                        |  Receive Duration |

The Total **Response Time** is displayed as a summary of the detailed view.
