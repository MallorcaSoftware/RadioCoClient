# radiococlient

## Requirements

Building the API client library requires [Maven](https://maven.apache.org/) to be installed.

## Installation

To install the API client library to your local Maven repository, simply execute:

```shell
mvn install
```

To deploy it to a remote Maven repository instead, configure the settings of the repository and execute:

```shell
mvn deploy
```

Refer to the [official documentation](https://maven.apache.org/plugins/maven-deploy-plugin/usage.html) for more information.

### Maven users

Add this dependency to your project's POM:

```xml
<dependency>
    <groupId>com.mallorcasoftware</groupId>
    <artifactId>radiococlient</artifactId>
    <version>1.0.0</version>
    <scope>compile</scope>
</dependency>
```

### Gradle users

Add this dependency to your project's build file:

```groovy
compile "com.mallorcasoftware:radiococlient:1.0.0"
```

### Others

At first generate the JAR by executing:

    mvn package

Then manually install the following JARs:

* target/radiococlient-1.0.0.jar
* target/lib/*.jar

## Getting Started

Please follow the [installation](#installation) instruction and execute the following Java code:

```java

import com.mallorcasoftware.radiococlient.*;
import com.mallorcasoftware.radiococlient.auth.*;
import com.mallorcasoftware.radiococlient.model.*;
import com.mallorcasoftware.radiococlient.api.DefaultApi;

import java.io.File;
import java.util.*;

public class DefaultApiExample {

    public static void main(String[] args) {
        
        DefaultApi apiInstance = new DefaultApi();
        String stationId = "stationId_example"; // String | Given station id
        try {
            StationStatusDto result = apiInstance.getStatus(stationId);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling DefaultApi#getStatus");
            e.printStackTrace();
        }
    }
}

```

## Documentation for API Endpoints

All URIs are relative to *http://public.radio.co/*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DefaultApi* | [**getStatus**](docs/DefaultApi.md#getStatus) | **GET** /stations/{stationId}/status | 


## Documentation for Models

 - [CurrentTrackDto](docs/CurrentTrackDto.md)
 - [HistoryTrackDto](docs/HistoryTrackDto.md)
 - [StationStatusDto](docs/StationStatusDto.md)


## Documentation for Authorization

All endpoints do not require authorization.
Authentication schemes defined for the API:

## Recommendation

It's recommended to create an instance of `ApiClient` per thread in a multithreaded environment to avoid any potential issue.

## Author

MallorcaSoftware

http://www.mallorca-software.com