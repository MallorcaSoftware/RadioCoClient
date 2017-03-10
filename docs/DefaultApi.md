# DefaultApi

All URIs are relative to *http://public.radio.co/*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getStatus**](DefaultApi.md#getStatus) | **GET** /stations/{stationId}/status | 


<a name="getStatus"></a>
# **getStatus**
> StationStatusDto getStatus(stationId)



Gets Status of the given station 

### Example
```java
// Import classes:
//import com.mallorcasoftware.radiococlient.ApiException;
//import com.mallorcasoftware.radiococlient.api.DefaultApi;


DefaultApi apiInstance = new DefaultApi();
String stationId = "stationId_example"; // String | Given station id
try {
    StationStatusDto result = apiInstance.getStatus(stationId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DefaultApi#getStatus");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **stationId** | **String**| Given station id |

### Return type

[**StationStatusDto**](StationStatusDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

