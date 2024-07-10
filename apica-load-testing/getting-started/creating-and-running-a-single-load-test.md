# Creating and Running a Single Load Test

A test script accesses the Load Test target and performs a number of actions that you will measure. There are several ways to add these to ALT. In this chapter, we take a look at creating LoadTests in LoadTest Portal. The following video provides a visual overview of the load test creation process.

{% embed url="https://media-cdn.atlassian.com/us-west-1/v1/cdn/file/6104a499-cb14-454e-8c22-10c9a4e16082/artifact/video_1280.mp4/binary?Key-Pair-Id=K3CEQBLVYJW0FT&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9tZWRpYS1jZG4uYXRsYXNzaWFuLmNvbS91cy13ZXN0LTEvdjEvY2RuL2ZpbGUvNjEwNGE0OTktY2IxNC00NTRlLThjMjItMTBjOWE0ZTE2MDgyL2FydGlmYWN0LyovYmluYXJ5PypjbGllbnQ9OTgyNTQ4NTQtNzdhYy00MDU3LWIzZWQtNjM0M2Q1YzE3MjQzKiIsIkNvbmRpdGlvbiI6eyJEYXRlTGVzc1RoYW4iOnsiQVdTOkVwb2NoVGltZSI6MTcyMDY0NzY1MX19fV19&Signature=UoU1sE2P0TYcq8wqAVEySYSFGFlS9-QBwcm4iO9Fo3QurydXYGvnJTkejMJfvHnLnF3NwtYsvpN-Qdan1gRPMriqdierxPObV8PzEVt~Mbh71p87fhFVt5wb9Z4oJZnxsqJCLoWRt4NVX8oFPzQs0rWK7quNx06gCqyrThWTjp0MD0VWz7hrDZ4RCve67ZAmhPGIFYokHbneV5VBjatIC7k6WFfKsgavihJ~s75tXnF7vhFqgq7KVS0a-To5UJMcshNj-355nhomSwrBbS1I3KOXJYJhP-AYa8~P2CNC8ZEyjfcBB3rgmL1V4suEbOw-EvRZTjvs3p~1HBE2QadXjA__&client=98254854-77ac-4057-b3ed-6343d5c17243&collection=contentId-5537844&max-age=2592000&token=eyJhbGciOiJSUzI1NiIsImtpZCI6ImdlbmVyaWMta2V5cGFpci9kdC1hcGktZmlsZXN0b3JlL2Nkbi1hdXRoLS1xcWwzczd2dTYyaWZxNG9iIn0.eyJzdWIiOiI5ODI1NDg1NC03N2FjLTQwNTctYjNlZC02MzQzZDVjMTcyNDMiLCJleHRJZCI6IjM4OGU5ODg4LWIxNTctNDg5MC1iNDkwLTdlMTdmODA2MjExZSIsImludElkIjoiMzg4ZTk4ODgtYjE1Ny00ODkwLWI0OTAtN2UxN2Y4MDYyMTFlIiwiaXNvbGF0ZWQiOmZhbHNlLCJyZXNvdXJjZVR5cGUiOjMsImlzcyI6ImdlbmVyaWMta2V5cGFpci9kdC1hcGktZmlsZXN0b3JlIiwiYXVkIjoibWVkaWEiLCJpYXQiOjE3MjA2NDQ3NzIsIm5iZiI6MTcyMDY0NDc3MiwiZXhwIjoxNzIwNjQ3NjUxLCJqdGkiOiJiMTJlZGM5ZGE2MDhkNjFmMTlkY2YxMjJlOTEyMzY1MjVhOWE0ZDU2In0.yt3_G1TkepgA_eNdYNHQhB3IK1l-ZCYqI34fgTBeew_W7GWSFlIi3lu1u_2RCQRfSQFG5lPmpp4mK6oN0UCNqpcja9dzmAxEvwtsC55b75bHEcLUFK5Vi6q3DlgE0wmbRy5E8EUUeTVSswVwyYcJyJn3J0ljVnekyVzUvYOTTuic_9SDFPHLhr9yYd1DXcw-ChwF9fQ_BytCnxUmofPOHr4Nys0VLSoNteqf5Hdp135vXdX_nWukUjh3itPQdnPYn4Ke5LuGqbYPJ79E7loZv-DUl7xfvWYrZo2ZthdGbBUK_UyaWAdisOrUixPuekgbPGl9UktqqrSrxonuPEIcjg" %}

{% hint style="info" %}
The above video and following process describe the process of creating a single script [Load Test](broken-reference). To run multiple scripts concurrently as a [Scenario](broken-reference), refer to [Running Multiple Tests Concurrently With Scenarios](broken-reference).
{% endhint %}

## Creating and Running a Load Test <a href="#creatingandrunningasingleloadtest-creatingandrunningaloadtest" id="creatingandrunningasingleloadtest-creatingandrunningaloadtest"></a>

To begin the process of creating a load test, navigate to the “Loadtest > New Test” page from the top menu bar within the ALT portal:

<div align="left">

<figure><img src="../../.gitbook/assets/91224f4d-2b2d-4f87-bb5c-d37c053b3b5f.png" alt=""><figcaption></figcaption></figure>

</div>

When the “Create New Loadtest” page appears, a list of links will appear on the right side of the page. Click on any of the links to jump to that step in the scenario process.

<div align="left">

<figure><img src="../../.gitbook/assets/54e60e3d-c704-460e-a885-6a0a2c851669.png" alt=""><figcaption></figcaption></figure>

</div>

### Step 1: Select Subscription <a href="#creatingandrunningasingleloadtest-step1-selectsubscription" id="creatingandrunningasingleloadtest-step1-selectsubscription"></a>

Select a subscript to begin the load test creation process.

<figure><img src="../../.gitbook/assets/b5117631-d346-41bd-be13-22d8fc1aebd1.png" alt=""><figcaption></figcaption></figure>

Every load test must be run using a valid subscription. A subscription is purchased when a customer pays for service. As the above screenshot shows, different subscriptions can be used for different purposes, although many customers will only have one subscription. The most common reason for multiple subscriptions is to allow for a subscription which accounts for “day to day” load tests with a smaller number of users, as well as a subscription with “burst days” which lasts for a much shorter period of time (e.g. two weeks) but allows for a much higher number of max users and/or a higher test duration. Each subscription displays the maximum number of users who are allowed to run a load test, the maximum duration of each load test which is run, the maximum number of tests which can be performed at one time, and the start and end time of the subscription.

{% hint style="info" %}
The specific terms of a subscription are determined when the customer contract is signed. Most subscriptions allow for an unlimited maximum number of tests.
{% endhint %}

### Step 2: Select Script <a href="#creatingandrunningasingleloadtest-step2-selectscript" id="creatingandrunningasingleloadtest-step2-selectscript"></a>

When a subscription has been selected, select a script from which to build the Load Test:

<figure><img src="../../.gitbook/assets/b87bf1e3-7152-4f59-83f3-0d1b54cadeb7.png" alt=""><figcaption></figcaption></figure>

#### Use Existing Loadtest Script <a href="#creatingandrunningasingleloadtest-useexistingloadtestscript" id="creatingandrunningasingleloadtest-useexistingloadtestscript"></a>

Users have the option to select from a list of previously uploaded .class or .zip files when creating a load test.

#### Create New Loadtest Script <a href="#creatingandrunningasingleloadtest-createnewloadtestscript" id="creatingandrunningasingleloadtest-createnewloadtestscript"></a>

**Create a New URL Script**

<div align="left">

<figure><img src="../../.gitbook/assets/3822fea6-eb45-4c26-8429-c112cbe3235a.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

The URL Script is a series of directly entered URL calls with some optional steps.

<div align="left">

<figure><img src="../../.gitbook/assets/796858c1-1587-45cb-9cac-831994c1cacd.png" alt="" width="563"><figcaption></figcaption></figure>

</div>

When the **Next** button is pressed, the entered URLs will be executed/validated and the option to proceed and generate the Loadtest script will be provided.

<figure><img src="../../.gitbook/assets/04a82725-fbe2-40ab-9f9f-47177a2983c6.png" alt=""><figcaption></figcaption></figure>

After that script is generated, it will appear as an existing .class file.

<div align="left">

<figure><img src="../../.gitbook/assets/9197ca2b-e0ec-41d5-8885-2c278efae834.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

**Create a New Loadtest Selenium Script**

<div align="left">

<figure><img src="../../.gitbook/assets/aeaca17e-f2fa-4ba3-9d29-307c667dbd96.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

It is possible to utilize an HTML-formatted Selenium IDE recorded session as the Load Test script. In the below screenshot, the file has already been uploaded and the user must click the Actions icon and wait until that HTML file has been run.

<div align="left">

<figure><img src="../../.gitbook/assets/1f7b731a-f7f0-4465-a08e-8931f8ea6453.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

A Step 2 Page will appear for you to select any step options:

<div align="left">

<figure><img src="../../.gitbook/assets/f4b70f2c-692c-4716-8633-ea34ce1d6314.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

When the user selects **Next**, the Selenium script will be executed/validated and the option to proceed and generate the script will be provided. The results of the URL calls will be shown. It is possible to remove certain file extensions or domains which are unnecessary by entering a comma-separated list of extensions/domains and clicking the “Remove” button. For example, a user may wish to remove 3rd party URLs from their load test script or run the script without .png or .jpg images. Alternatively, it is possible to only keep certain domains within the script and remove all other domains by entering a comma-separated list of domains and clicking the “Keep” button.

<figure><img src="../../.gitbook/assets/03b602db-2f31-473a-ae95-3a230721dffc.png" alt=""><figcaption></figcaption></figure>

When a user clicks the “Remove” or “Keep” buttons, the list of URLs in the table will update to reflect the extensions or domains which have been kept or removed.

**Upload a New ZebraTester Script**

To upload a new ZebraTester file, click the “ZebraTester” file icon:

<div align="left">

<figure><img src="../../.gitbook/assets/61734fe1-7443-42ef-bb4a-41e3e008596f.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

The **Upload Zebra File** dialog opens.

<div align="left">

<figure><img src="../../.gitbook/assets/6674597b-b3c3-453f-9166-db8d6f6ec975.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

Upload a compatible .class or .zip file. Select an existing Project to assign the file to using the file dropdown, or select “Add Project” to create an entirely new Project. Select a script group or leave the script ungrouped. Add an optional file description and click the Save button.

### Step 3: Presets <a href="#creatingandrunningasingleloadtest-step3-presets" id="creatingandrunningasingleloadtest-step3-presets"></a>

If a user within your customer account has configured a Load Test, a Preset may already be defined with a number of users, a test duration, a defined location, etc. Configuration of the Loadtest Options, Location, and Test Information sections are mandatory; other configuration options are optional.

<div align="left">

<figure><img src="../../.gitbook/assets/5bdbea84-aa40-4070-be4f-8c63d40506b9.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

#### Loadtest Options <a href="#creatingandrunningasingleloadtest-loadtestoptions" id="creatingandrunningasingleloadtest-loadtestoptions"></a>

The following graph provides a visual explanation of the Loadtest Duration, Ramp Up Time, and Users within a test:

<div align="left">

<figure><img src="../../.gitbook/assets/54270977-7a5c-4764-b573-bd0ecea135e4.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

It is possible to run several tests in sequential order (as opposed to running in parallel) by selecting “Run Multiple Sequential Tests”.

### Step 4: Location <a href="#creatingandrunningasingleloadtest-step4-location" id="creatingandrunningasingleloadtest-step4-location"></a>

Select the location from which to run the load test. A Cluster is a saved collection of one or more locations which a user can reuse when running load tests. A cluster must be defined when starting a load test, rather than one individual location, although a cluster can consist of only one test.

<div align="left">

<figure><img src="../../.gitbook/assets/41716955-fb34-4a0c-a4cd-773623de3542.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

### Step 5: Scenario Options <a href="#creatingandrunningasingleloadtest-step5-scenariooptions" id="creatingandrunningasingleloadtest-step5-scenariooptions"></a>

Optional custom response time percentiles can be used to set specific percentiles for each page response time. The settings will be used when creating the test results and will be available on the test result page.

### Step 6: Advanced Options <a href="#creatingandrunningasingleloadtest-step6-advancedoptions" id="creatingandrunningasingleloadtest-step6-advancedoptions"></a>

<div align="left">

<figure><img src="../../.gitbook/assets/9694d506-4016-4892-93a7-2f00332059c3.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

The **Max Loops per User** field limits the number of web surfing session repetitions (loops) per simulated user. The load test stops if the limit has reached for each simulated user. This parameter can be combined with the parameter 'Load Test Duration'; the limitation which first occurs will stop the load test.

**Script pacing** is used to control the pace of script iterations (loops) over time. When the script reaches the end of an iteration (loop) the virtual user is inactive until the pacing time is reached. The result is a static flow of script iterations over time as long as the pacing time is set to a longer time than the script iteration time. The function is commonly used to control the requests per time ratio independent of response times. For example, a 30 second pacing gives one script iteration (loop) every 30 seconds.

The **Additional Options** field passes command line options to the load testing engine. If additional options are specified within a ZebraTester script which is being tested, do not reproduce those additional options here; otherwise duplicate fields may arise. The following\
\
`-multihomed` Initiates all Exec Agents to use multiple local IP addresses when executing a load test. This option allows users to simulate traffic from more than one IP address per Exec Agent. This option is only considered if the Exec Agent supports a multihomed network configuration (that is, several IP addresses are assigned to the same host). The first step in using this option is to configure multiple IP addresses for the same host on the level of the Windows or Unix operating system. The second step is to assign these IP addresses to the Exec Agent configuration. For the local host, where the Web Admin GUI is running, the second step can be performed by calling the Setup menu inside the Project Navigator (the “gear-wheel” icon at the top of the navigation). For remote Exec Agents, edit the file javaSetup.dat which is located inside the ZebraTester installation directory by modifying the value of the entry javaVirtualIpAddresses: enter all IP addresses of the host on the same line and separate them by comma characters. The effect of this option is that each concurrent user uses its own client IP address during the load test. If fewer IP addresses are available than concurrent users, the IP addresses are averaged across the users.\
\
`-sslcache <seconds>` Alters the timeout of the user-related SSL cache. The default value is 300 seconds. A value of 0 (zero) has the effect that the SSL cache is disabled.\
\
`-sslcreset` Reset the user-related SSL session cache per loop (default: no reset per loop).\
\
`-sslcmode` Apply SSL/HTTPS compatibility workarounds for deficient SSL servers. You may try this option if you get constantly the error type 'Network Connection aborted by Server' for all URL calls.\
\
`-tz <timezone>` Sets an alternative time zone which is used by the load test program. The default time zone is equal to the selection which has been made when installing ZebraTester, or - if modified subsequently - which has been set in the Personal Settings menu. Possible time zone values are described in chapter 6 of the Application Reference Manual.\


`-ssl <parameter>`

* All - Automatic detection of the SSL protocol version. ZebraTester prefers the TLS 1.2 protocol, but if this is not supported by the Web server, TLS 1.1, TLS 1.0 or SSL v3 is used. This is the normal behavior which is implemented in many Web browser products.
* v3 - Fixes the SSL protocol version to SSL v3.
* TLS - Fixes the SSL protocol version to TLS 1.0.
* TLS11 - Fixes the SSL protocol version to TLS 1.1.
* TLS12 - Fixes the SSL protocol version to TLS 1.2.

### Step 7: Client Options <a href="#creatingandrunningasingleloadtest-step7-clientoptions" id="creatingandrunningasingleloadtest-step7-clientoptions"></a>

Define a custom user agent and custom bandwidth speeds.

<div align="center">

<figure><img src="../../.gitbook/assets/3239bd58-1370-47d3-97cd-a1f7f9a7d462 (1).png" alt=""><figcaption></figcaption></figure>

</div>

Configuration of [Client Side Monitoring](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5673024) is optional.

### Step 8: DNS Options <a href="#creatingandrunningasingleloadtest-step8-dnsoptions" id="creatingandrunningasingleloadtest-step8-dnsoptions"></a>

Specifying a **DNS Hosts file** will allow the load test job to utilize its own DNS hosts file in order to resolve hostnames. If a Hosts file is used, the hosts file of the underlying operating system will be ignored. A DNS Hosts file must be zipped along with all other scenario input files. Specifying a **DNS Server** will allow a load test job to use one or more specific DNS server(s) in order to resolve hostnames. If a custom DNS server is specified, the DNS library of the underlying agent operating system will be ignored. Multiple values can be entered and separated by a comma.

Only IP addresses will be accepted in the DNS server field! DNS names are invalid.

Specifying a **DNS Translation file** will allow for a manual DNS remapping so an internal/non-production hostname can be mapped to a public hostname.

<div align="left">

<figure><img src="../../.gitbook/assets/b6ba2f4c-8b78-4bf0-a37c-57455c43696d.png" alt="" width="563"><figcaption></figcaption></figure>

</div>

### Step 9: Reporting <a href="#creatingandrunningasingleloadtest-step9-reporting" id="creatingandrunningasingleloadtest-step9-reporting"></a>

Reporting is an optional feature. Reporting History defines a number of prior tests to compare the current report to. For example, a Reporting History of 10 will attempt to find a maximum of 10 load test jobs similar to the one being configured, and present a comparison of the configured job and the previous jobs in a report. The similarity is based on the script being run as well as the number of parallel users which is defined.

<div align="left">

<figure><img src="../../.gitbook/assets/878410eb-a56d-4791-b9c4-88d7c38d24bc (1).png" alt="" width="375"><figcaption></figcaption></figure>

</div>

### Step 10: Test Information <a href="#creatingandrunningasingleloadtest-step10-testinformation" id="creatingandrunningasingleloadtest-step10-testinformation"></a>

Add the created script into a Project. Take the Test Instance and attach it to a new or existing Instance. Add comments and tags for more context and organization.

<div align="left">

<figure><img src="../../.gitbook/assets/a4c0fd7d-8a2b-41f5-a7bd-7282ef4cf37b.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

### Step 11: Monitoring Agents <a href="#creatingandrunningasingleloadtest-step11-monitoringagents" id="creatingandrunningasingleloadtest-step11-monitoringagents"></a>

If the **AppDynamics** integration has been configured within a user’s customer account, the user can select an AppDynamics server in this section which will gather additional Test metrics. There is a specific tab within the load test Results which displays AppDynamics data that is gathered using the integration. In the **Performance Monitoring Agents** section, a user can include a configured Performance Monitoring Agent as part of the test. The agents need to have been created and configured within the [Monitoring Agents](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5672405/Monitoring+Agents) page before they can be added to a test.

<div align="left">

<figure><img src="../../.gitbook/assets/cfdc6622-2a11-4e4e-8ed5-8d0ce246152f.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

A user can select single agents or an entire group with all agents at once.

### Steps 12 and 13: Execution and Start Loadtest <a href="#creatingandrunningasingleloadtest-steps12and13-executionandstartloadtest" id="creatingandrunningasingleloadtest-steps12and13-executionandstartloadtest"></a>

It is possible to specify a runtime and to save the current settings as a preset in the final steps. Click “Initiate Loadtest” to begin the test.
