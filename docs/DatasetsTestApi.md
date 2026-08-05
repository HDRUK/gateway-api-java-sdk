# DatasetsTestApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**datasetsTest**](DatasetsTestApi.md#datasetsTest) | **POST** /api/v1/datasets/test | DatasetController@datasetTest |


<a id="datasetsTest"></a>
# **datasetsTest**
> CreateDarIntegration201Response datasetsTest(datasetsTestRequest)

DatasetController@datasetTest

Datasets test

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DatasetsTestApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    DatasetsTestApi apiInstance = new DatasetsTestApi(defaultClient);
    DatasetsTestRequest datasetsTestRequest = new DatasetsTestRequest(); // DatasetsTestRequest | Pass datasets payload
    try {
      CreateDarIntegration201Response result = apiInstance.datasetsTest(datasetsTestRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatasetsTestApi#datasetsTest");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **datasetsTestRequest** | [**DatasetsTestRequest**](DatasetsTestRequest.md)| Pass datasets payload | |

### Return type

[**CreateDarIntegration201Response**](CreateDarIntegration201Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

