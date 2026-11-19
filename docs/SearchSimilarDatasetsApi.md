# SearchSimilarDatasetsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**searchSimilarDatasets**](SearchSimilarDatasetsApi.md#searchSimilarDatasets) | **POST** /api/v1/search/similar/datasets | Search for similar datasets (deprecated) |
| [**searchSimilarDatasetsV2**](SearchSimilarDatasetsApi.md#searchSimilarDatasetsV2) | **POST** /api/v2/search/similar/datasets | Search for similar datasets |


<a id="searchSimilarDatasets"></a>
# **searchSimilarDatasets**
> searchSimilarDatasets(searchSimilarDatasetsV2Request)

Search for similar datasets (deprecated)

Deprecated: use /api/v2/search/similar/datasets, which this endpoint now serves. Responses carry Deprecation, Sunset and Link headers; it stops working after the Sunset date (17 May 2027).

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
    SearchSimilarDatasetsV2Request searchSimilarDatasetsV2Request = new SearchSimilarDatasetsV2Request(); // SearchSimilarDatasetsV2Request | 
    try {
      apiInstance.searchSimilarDatasets(searchSimilarDatasetsV2Request);
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
| **searchSimilarDatasetsV2Request** | [**SearchSimilarDatasetsV2Request**](SearchSimilarDatasetsV2Request.md)|  | |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Same as /api/v2/search/similar/datasets |  -  |
| **400** | Missing or invalid dataset id |  -  |

<a id="searchSimilarDatasetsV2"></a>
# **searchSimilarDatasetsV2**
> SearchSimilarDatasetsV2200Response searchSimilarDatasetsV2(searchSimilarDatasetsV2Request)

Search for similar datasets

Returns up to three gateway datasets sharing the most terms with the provided dataset&#39;s keywords and title. The provided dataset is never included.

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
    SearchSimilarDatasetsV2Request searchSimilarDatasetsV2Request = new SearchSimilarDatasetsV2Request(); // SearchSimilarDatasetsV2Request | 
    try {
      SearchSimilarDatasetsV2200Response result = apiInstance.searchSimilarDatasetsV2(searchSimilarDatasetsV2Request);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SearchSimilarDatasetsApi#searchSimilarDatasetsV2");
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
| **searchSimilarDatasetsV2Request** | [**SearchSimilarDatasetsV2Request**](SearchSimilarDatasetsV2Request.md)|  | |

### Return type

[**SearchSimilarDatasetsV2200Response**](SearchSimilarDatasetsV2200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success; empty data when the dataset is not indexed |  -  |
| **400** | Missing or invalid dataset id |  -  |

