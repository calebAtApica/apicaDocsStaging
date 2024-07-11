# Performance Monitoring Agent (PMA) Installation

The Apica Monitoring Agent is a service that collects performance metrics at regular intervals. The collected data is sent to a controller server which stores the data in a database administered by Apica. Examples of metrics collected by the agent include CPU usage, memory usage, network, and disk utilization. The PMA agent communicates with its controller via TCP or HTTP. Utilize the following table to determine which hostname:port combination to whitelist in order to connect the agent to the controller server.

| **If you log into**                                                  | **whitelist hostname**                                                             | **protocol used** | **port/direction** |
| -------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ----------------- | ------------------ |
| [https://loadtest.apicasystem.com](https://loadtest.apicasystem.com) | [ltagcontroller.apicasystem.com](http://ltagcontroller.apicasystem.com)            | TCP               | 26300 outbound     |
|                                                                      |                                                                                    | HTTP              | 26301 outbound     |
| [https://alt-us1.apicasystems.com](https://alt-us1.apicasystems.com) | [pma-controller-us1.apicasystems.com](http://pma-controller-us1.apicasystems.com/) | TCP               | 26300 outbound     |
|                                                                      |                                                                                    | HTTP              | 26301 outbound     |

## Windows Performance Agent (PMA)

The client for Windows uses Windows Performance Objects to gather system statistics. The installation package is an MSI package that places the necessary files in a target location on the local system.

### Windows Agent Downloads

[Apica Agent Setup](https://apica-packages.s3.eu-central-1.amazonaws.com/stable/pma/ApicaAgentMsiSetup.msi)

[PMA Windows .NET 3.5](https://apica-packages.s3.eu-central-1.amazonaws.com/stable/pma/install/win/PMA-Windows-NET35\_v1.0.msi)

[PMA Windows .NET 4.5](https://apica-packages.s3.eu-central-1.amazonaws.com/stable/pma/install/win/PMA-Windows-NET45\_v1.0.msi)

[PMA Windows v.1.1](https://apica-packages.s3.eu-central-1.amazonaws.com/stable/pma/install/win/PMA-Windows\_v1.1.msi)

### Installation

* Run ApicaAgentSetup.msi
* Follow the installation instructions on the screen
* Open config.xml in the installation directory and enter your agent ticket. This will be provided to you by the Apica team.
* Start the agent by starting the ApicaAgent service.
* Stop the agent by stopping the ApicaAgent service.

### Windows Client

The client for Windows uses Windows Performance Objects to gather system statistics. The installation package is an MSI package that places the necessary files in a target location on the local system.

\[Coming Soon (ApicaAgentSetup\_external.msi)]

### Installation

* Run ApicaAgentSetup.msi
* Follow the installation instructions on the screen
* Open config.xml in the installation directory and enter your agent ticket. This will be provided to you by the Apica team.
* Start the agent by starting the ApicaAgent service.
* Stop the agent by stopping the ApicaAgent service.

**Configuration**

| **Item**  | **Description**                                                                                                                      |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| host      | Do not change! The hostname or IP address of the agent controller. This will be provided by the Apica team.                          |
| ticket    | Unique identifier for this agent. This will be provided by the Apica team.                                                           |
| pmcConfig | The filename of the pmcConfig file, located in the installation directory of the agent. Default value = pmcconfig.xml.               |
| protocol  | The protocol used by the agent to communicate with the agent controller. Accepted values are TCP or HTTP. The default value is TCP.  |
| protocol  |  The protocol used by the agent to communicate with the agent controller. Accepted values are TCP or HTTP. The default value is TCP. |

#### Configure performance counters

The pmcConfig file describes the performance counters that will be collected by the agent.

In this example we instruct the agent to collect the performance counter % Processor Time in performance object Processor, and we want to collect statistics for all processors so we set the instance to \_Total.

```
<performanceCounter>
  <pmc name="cid">1</pmc>
  <pmc name="CategoryName">Processor</pmc>
  <pmc name="CounterName">% Processor Time</pmc>
  <pmc name="InstanceName">_Total</pmc>
</performanceCounter>
```

The easiest way to find additional Performance Counters is to open perfmon.exe on the local machine and add a new counter.

You will be presented with a list of Categories like Processor or Processor Information and within these categories, you will find different performance counters like % User Time or % Processor Time.

Once you have added the counter to perfmon, the selected counters will be displayed at the bottom of the window. The list of selected counters contains the information that needs to be supplied to the agent in the pmcConfig file.

```
Object = CategoryName, Counter = CounterName, Instance = InstanceName
```

You can find a complete list of pre-defined counters as well as instructions for creating your own counters in the following article: [https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/878182402](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/878182402)

You can find several templates which include sets of pre-defined counters tailored to different environments (SQL server, for example) in this article: [https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5672726](https://apica-kb.atlassian.net/wiki/spaces/ALTDOCS/pages/5672726)

## Troubleshooting Windows Agents

Troubleshooting the agent installation or operation can be done by referencing the error messages in logs.

**Examples**

Logs: The agent logs are sent to the application event log in windows.

Connectivity issues

If the agent is configured to use plain TCP it must be able to connect to ltagcontroller.apicasystem.com on TCP port 26300.

If the agent is configured to use HTTP is must be able to connect to ltagcontroller.apicasystem.com on TCP port 26301.

Misconfigured Performance Counters

The error message below occurs when the agent is unable to fetch a performance counter from the underlying operating system. Please check your pmcConfig file and correct any errors, also make sure that you are able to find all of the configured performance counters using perfmon.exe on the local machine.

#### Linux

| **Counter ID** | **Name**                        | **Unit** |
| -------------- | ------------------------------- | -------- |
| 1              | CPU Usage                       | %        |
| 2              | Physical Memory Used            | MB       |
| 3              | Network Receive (RX)            | Mbit/s   |
| 4              | Network Transmit (TX)           | Mbit/s   |
| 5              | Disk Read                       | MB/s     |
| 6              | Disk Write                      | MB/s     |
| 15             | Load Avg (1 Min)                | Count    |
| 16             | Load Avg (5 Min)                | Count    |
| 17             | Load Avg (15 Min)               | Count    |
| 18             | Pages swapped into memory/sec   | Count    |
| 19             | Pages swapped out of memory/sec | Count    |
| 20             | IO Wait                         | %        |
| 21             | Memory Cache Used               | MB       |
| 22             | Running Processes               | Count    |
| 23             | Physical Memory Available       | MB       |

#### Windows

| **Counter ID** | **Name**                              | **Unit** |
| -------------- | ------------------------------------- | -------- |
| 1              | CPU Usage                             | %        |
| 23             | Physical Memory Available             | MB       |
| 3              | Network Receive (RX)                  | Mbit/s   |
| 4              | Network Transmit (TX)                 | Mbit/s   |
| 5              | Disk Read                             | MB/s     |
| 6              | Disk Write                            | MB/s     |
| 24             | Physical Disk: Avg. Disk Queue Length | Count    |
| 25             | System: Threads                       | Count    |
| 26             | System: Processor Queue Length        | Count    |
| 27             | Memory: Pages/sec                     | Count    |
| 28             | Physical Disk: % Disk Time            | %        |

## Linux Agent

The client for Linux utilizes the libstatgrab library to collect system statistics. The installation package is a tar archive containing an installation script that places the necessary files in default locations on the local system.

**⏬ Linux Agent Downloads**

[PMA Linux v.1.1](https://apica-packages.s3.eu-central-1.amazonaws.com/stable/pma/install/lin/PMA-Linux-v1.1.tar.gz)

[PMA Linux v1.2](https://apica-packages.s3.eu-central-1.amazonaws.com/stable/pma/install/lin/PMA-Linux-v1.2.tar.gz)

[PMA FreeBSD8 v1.0](https://apica-packages.s3.eu-central-1.amazonaws.com/stable/pma/install/lin/PMA-FreeBSD8-v1.0.zip)

[Free BSDx64 10.1](https://apica-packages.s3.eu-central-1.amazonaws.com/stable/pma/custom/apica\_agent-freebsd-x64-10.1.sh)

[PMA Controller](https://apica-packages.s3.eu-central-1.amazonaws.com/stable/pma/install/PMA-Controller.tar.gz)

**Default locations**

The binary file is located at /usr/bin/apicaagent,

configuration files are stored in /etc/apica

and a startup script is placed in /etc/init.d/.

**Installation**

Before you install the agent make sure that the local machine is able to connect to ltagcontroller.apicasystem.com on TCP port 26300 or 26301.

* Extract the files from install\_apicaagent.tar.gz.
* Enter the directory install\_apicaagent and run install\_apicaagent.sh
* Open /etc/apica/client.conf and enter your agent ticket.
* Start the agent by running /etc/init.d/apicaagent start
* Stop the agent by running /etc/init.d/apicaagent stop

**Configuration**

| **Item** | **Description**                                                                                                                     |
| -------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| host     | Do not change! The hostname or IP address of the agent controller.                                                                  |
| ticket   | Unique identifier for this agent.                                                                                                   |
| protocol | The protocol used by the agent to communicate with the agent controller. Accepted values are TCP or HTTP. The default value is TCP. |

## Linux Troubleshooting

Troubleshooting the agent installation or operation can be done by referencing the error messages in logs.

### Examples

Logs: The agent logs are sent to the application event log in windows.

**Connectivity issues**

Connectivity issues: If the agent is configured to use plain TCP it must be able to connect to ltagcontroller.apicasystem.com on TCP port 26300. If the agent is configured to use HTTP is must be able to connect to ltagcontroller.apicasystem.com on TCP port 26301.

**Note:** If you are using an internal agent controller, please make sure that the agent is able to connect to the internal host name or IP address on either 26300 (TCP) or 26301 (HTTP).

**Custom metrics**

The Linux client supports custom metrics gathered from an external script. The script must send output to standard output in the following format (one JSON object per value):

{ \`counter\_id\` : { \`id\` : counter\_id, \`timestamp\` : unix\_timestamp, \`value\` : sample\_value }, \`counter\_id\` : { \`id\` : counter\_id, \`timestamp\` : unix\_timestamp, \`value\` : sample\_value } }

| Item            | Description                                         |
| --------------- | --------------------------------------------------- |
| counter\_id     | Counter identifier, configured in agent controller. |
| unix\_timestamp | Unix timestamp (seconds since 1970-01-01)           |
| sample\_value   | Numeric (Integer) value                             |

In the configuration file you need to uncomment and edit the following settings (The example below uses a python script but you may use any kind of script that prints to stdout):

script\_enabled = true

script = python path/to/your/python/script

**Example: Established connections**

\#!/usr/bin/python import os import time cons = os.popen("netstat -nt | grep ESTABLISHED | wc -l").read(); print { "28" : { "id" : 28, "timestamp" : int(time.time()), "value" : int(cons.replace('\n',''))} };

**Example: Threads**

\#!/usr/bin/python import os import time threads = os.popen("ps -eLF | wc -l").read(); print { "42" : { "id" : 42, "timestamp" : int(time.time()), "value" : int(threads.replace('\n','')

**Misconfigured Performance Counters**

The error message below occurs when the agent is unable to fetch a performance counter from the underlying operating system. Please check your pmcConfig file and correct any errors, also make sure that you are able to find all of the configured performance counters using perfmon.exe on the local machine.

**Counters**

| Counter ID | Name                            | Unit   |
| ---------- | ------------------------------- | ------ |
| 1          | CPU Usage                       | %      |
| 2          | Physical Memory Used            | MB     |
| 3          | Network Receive (RX)            | Mbit/s |
| 4          | Network Transmit (TX)           | Mbit/s |
| 5          | Disk Read                       | MB/s   |
| 6          | Disk Write                      | MB/s   |
| 15         | Load Avg (1 Min)                | Count  |
| 16         | Load Avg (5 Min)                | Count  |
| 17         | Load Avg (15 Min)               | Count  |
| 18         | Pages swapped into memory/sec   | Count  |
| 19         | Pages swapped out of memory/sec | Count  |
| 20         | IO Wait                         | %      |
| 21         | Memory Cache Used               | MB     |
| 22         | Running Processes               | Count  |
| 23         | Physical Memory Available       | MB     |
