# Report Generator Utility

**Report Generator Utility** uses ALT Restful API to generate a report on scenario summary and transaction/page metrics in MS Excel format.

The report contains: Sheet **Transaction/Page Summary Details**:

This is a table where you can find a summary of a run scenario and information about every page/transaction in the scenario.

#### Prerequisites <a href="#reportgeneratorutility-prerequisites" id="reportgeneratorutility-prerequisites"></a>

The report generator uses Java 11 . It can be downloaded at [AdoptOpenJDK](https://adoptopenjdk.net/?variant=openjdk11\&jvmVariant=hotspot)

To check Java version that is installed on your machine, run `java -version`

For example, on Window 10 and AdoptOpenJDK the output should be like this

```
PS C:\temp\e> java -version
openjdk version "11.0.7" 2020-04-14
OpenJDK Runtime Environment AdoptOpenJDK (build 11.0.7+10)
OpenJDK 64-Bit Server VM AdoptOpenJDK (build 11.0.7+10, mixed mode)
```

#### Download Links <a href="#reportgeneratorutility-downloadlinks" id="reportgeneratorutility-downloadlinks"></a>

[https://alt-report-generator.s3.amazonaws.com/1.0.11/ReportGenerator.jar](https://alt-report-generator.s3.amazonaws.com/1.0.11/ReportGenerator.jar) and [https://alt-report-generator.s3.amazonaws.com/1.0.11/java8/ReportGenerator.jar](https://alt-report-generator.s3.amazonaws.com/1.0.11/java8/ReportGenerator.jar) (Java 8 version)

#### Usage <a href="#reportgeneratorutility-usage" id="reportgeneratorutility-usage"></a>

`java -jar ./ReportGenerator.jar 123` where _123_ is **Run ID** of a completed job. On ALT Portal Navigate to **Loadtest → Jobs** and scroll down to **Completed Jobs** to find the Run ID.

**Property file** holds _api.endpoint_ and _api.token_ that is used for making requests to ALT Restful API.

It should be placed in the same directory with _ReportGenerator.jar_, be named **reportgenerator.properties** and have content like this:

```
api.endpoint=https://api-alt-us1.apicasystems.com/v1
api.token=98585B7D-1562-4FBC-9870-41F591C1XXXX
```

To get **Token** and **Endpoint** Navigate to **API** tab on ALT Portal

**NOTE** If the report generator is not able to find the property file it will suggest creating one:

```
PS C:\apica\alt-custom-report-generator\target> java -jar .\ReportGenerator.jar 123
Property file not found. Would you like to create a default property file? [Y/n] Y
Property file has been generated. Please set proper api.endpoint and api.token
```

#### Different Options Available <a href="#reportgeneratorutility-differentoptionsavailable" id="reportgeneratorutility-differentoptionsavailable"></a>

`-p` or `--properties` - custom property file, example

_java -jar ./ReportGenerator.jar -p /path/to/property/file/filename.properties 123_

`-o` or `--output` - custom output report file, example

_java -jar ./ReportGenerator.jar -o /path/to/output/file/filename.xlsx 123_

`-e` or `--api-endpoint`, `-t` or `--api-token` - ALT Restful API endpoint and access token, example

_java -jar ./ReportGenerator.jar -t 98585B7D-1562-4FBC-9870-41F591C1XXXX -e_ [_https://api-alt-us1.apicasystems.com/v1_](https://api-alt-us1.apicasystems.com/v1) _123_

`-S` or `--inseconds` - All the times will be in seconds

_java -jar ./ReportGenerator.jar -t 98585B7D-1562-4FBC-9870-41F591C1XXXX -e_ [_https://api-alt-us1.apicasystems.com/v1_](https://api-alt-us1.apicasystems.com/v1) _123 -S_

`-P` or `--pagemetrics` - Report based on Page Metrics

_java -jar ./ReportGenerator.jar -t 98585B7D-1562-4FBC-9870-41F591C1XXXX -e_ [_https://api-alt-us1.apicasystems.com/v1_](https://api-alt-us1.apicasystems.com/v1) _123 -S_ -P

NOTE if both endpoint and token are provided as parameters the property file is not needed. If only token or endpoint is provided the other will be got from the property file.

#### Troubleshooting <a href="#reportgeneratorutility-troubleshooting" id="reportgeneratorutility-troubleshooting"></a>

If you get:

```
Error: Could not create the Java Virtual Machine.
Error: A fatal exception has occurred. Program will exit.
```

Please check that cmd line is valid (see examples above), you have enough permissions to run the tool and Java is installed properly.

#### Verbose mode <a href="#reportgeneratorutility-verbosemode" id="reportgeneratorutility-verbosemode"></a>

Usually, the report generator gives clear error messages so you can fix it easily, but sometime you might need to get detailed log. To run the report generator in verbose mode, pass a system parameter `-Dverbose=true` before `-jar`, example

```
java -Dverbose=true -jar ./ReportGenerator.jar 123
```
