# SearchSimilarDatasetsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**searchSimilarDatasets**](SearchSimilarDatasetsApi.md#searchSimilarDatasets) | **POST** /api/v1/search/similar/datasets | Search@similarDatasets |


<a id="searchSimilarDatasets"></a>
# **searchSimilarDatasets**
> SearchSimilarDatasets200Response searchSimilarDatasets(searchSimilarDatasetsRequest)

Search@similarDatasets

Returns top three gateway datasets most similar to the provided dataset

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.SearchSimilarDatasetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    SearchSimilarDatasetsApi apiInstance = new SearchSimilarDatasetsApi(defaultClient);
    SearchSimilarDatasetsRequest searchSimilarDatasetsRequest = new SearchSimilarDatasetsRequest(); // SearchSimilarDatasetsRequest | Submit dataset id
    try {
      SearchSimilarDatasets200Response result = apiInstance.searchSimilarDatasets(searchSimilarDatasetsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SearchSimilarDatasetsApi#searchSimilarDatasets");
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
| **searchSimilarDatasetsRequest** | [**SearchSimilarDatasetsRequest**](SearchSimilarDatasetsRequest.md)| Submit dataset id | |

### Return type

[**SearchSimilarDatasets200Response**](SearchSimilarDatasets200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

