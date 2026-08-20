# NightlyDatasetTestsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**fetchNightlyDatasetTestsV2**](NightlyDatasetTestsApi.md#fetchNightlyDatasetTestsV2) | **GET** /api/v2/nightly_dataset_tests | NightlyDatasetTestController@index |


<a id="fetchNightlyDatasetTestsV2"></a>
# **fetchNightlyDatasetTestsV2**
> FetchDatasetLinkCheckResultsV2200Response fetchNightlyDatasetTestsV2()

NightlyDatasetTestController@index

Get the results of the nightly dataset reachability check, with a summary and a list of failures

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.NightlyDatasetTestsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    NightlyDatasetTestsApi apiInstance = new NightlyDatasetTestsApi(defaultClient);
    try {
      FetchDatasetLinkCheckResultsV2200Response result = apiInstance.fetchNightlyDatasetTestsV2();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NightlyDatasetTestsApi#fetchNightlyDatasetTestsV2");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**FetchDatasetLinkCheckResultsV2200Response**](FetchDatasetLinkCheckResultsV2200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

