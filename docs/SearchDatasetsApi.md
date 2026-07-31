# SearchDatasetsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**searchDatasets**](SearchDatasetsApi.md#searchDatasets) | **POST** /api/v1/search/datasets | Search@datasets |


<a id="searchDatasets"></a>
# **searchDatasets**
> SearchDatasets200Response searchDatasets(searchDatasetsRequest)

Search@datasets

Returns gateway datasets related to the provided query term(s)

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.SearchDatasetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    SearchDatasetsApi apiInstance = new SearchDatasetsApi(defaultClient);
    SearchDatasetsRequest searchDatasetsRequest = new SearchDatasetsRequest(); // SearchDatasetsRequest | Submit search query
    try {
      SearchDatasets200Response result = apiInstance.searchDatasets(searchDatasetsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SearchDatasetsApi#searchDatasets");
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
| **searchDatasetsRequest** | [**SearchDatasetsRequest**](SearchDatasetsRequest.md)| Submit search query | |

### Return type

[**SearchDatasets200Response**](SearchDatasets200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

