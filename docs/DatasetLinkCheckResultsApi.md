# DatasetLinkCheckResultsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**fetchDatasetLinkCheckResultsV2**](DatasetLinkCheckResultsApi.md#fetchDatasetLinkCheckResultsV2) | **GET** /api/v2/dataset_link_check_results | DatasetLinkCheckResultController@index |


<a id="fetchDatasetLinkCheckResultsV2"></a>
# **fetchDatasetLinkCheckResultsV2**
> FetchDatasetLinkCheckResultsV2200Response fetchDatasetLinkCheckResultsV2()

DatasetLinkCheckResultController@index

Get the confirmed dead links (HTTP 404, verified across multiple checks) found in active dataset metadata by the nightly link check

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DatasetLinkCheckResultsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    DatasetLinkCheckResultsApi apiInstance = new DatasetLinkCheckResultsApi(defaultClient);
    try {
      FetchDatasetLinkCheckResultsV2200Response result = apiInstance.fetchDatasetLinkCheckResultsV2();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatasetLinkCheckResultsApi#fetchDatasetLinkCheckResultsV2");
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

