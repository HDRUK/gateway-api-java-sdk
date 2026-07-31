# AdminSearchApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createAdminSearchReindex**](AdminSearchApi.md#createAdminSearchReindex) | **POST** /api/v1/admin/search/reindex | Queue a drop+recreate+import of a search entity&#39;s Typesense collection |
| [**fetchAdminSearchStatus**](AdminSearchApi.md#fetchAdminSearchStatus) | **GET** /api/v1/admin/search/status | Get Typesense collection status for every onboarded search entity |
| [**updateAdminSearchFeature**](AdminSearchApi.md#updateAdminSearchFeature) | **POST** /api/v1/admin/search/feature | Activate or deactivate a search-related Pennant feature flag |


<a id="createAdminSearchReindex"></a>
# **createAdminSearchReindex**
> createAdminSearchReindex(createAdminSearchReindexRequest)

Queue a drop+recreate+import of a search entity&#39;s Typesense collection

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.AdminSearchApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    AdminSearchApi apiInstance = new AdminSearchApi(defaultClient);
    CreateAdminSearchReindexRequest createAdminSearchReindexRequest = new CreateAdminSearchReindexRequest(); // CreateAdminSearchReindexRequest | 
    try {
      apiInstance.createAdminSearchReindex(createAdminSearchReindexRequest);
    } catch (ApiException e) {
      System.err.println("Exception when calling AdminSearchApi#createAdminSearchReindex");
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
| **createAdminSearchReindexRequest** | [**CreateAdminSearchReindexRequest**](CreateAdminSearchReindexRequest.md)|  | |

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
| **202** | Reindex queued |  -  |
| **422** | Unknown entity |  -  |

<a id="fetchAdminSearchStatus"></a>
# **fetchAdminSearchStatus**
> fetchAdminSearchStatus()

Get Typesense collection status for every onboarded search entity

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.AdminSearchApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    AdminSearchApi apiInstance = new AdminSearchApi(defaultClient);
    try {
      apiInstance.fetchAdminSearchStatus();
    } catch (ApiException e) {
      System.err.println("Exception when calling AdminSearchApi#fetchAdminSearchStatus");
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

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="updateAdminSearchFeature"></a>
# **updateAdminSearchFeature**
> updateAdminSearchFeature(updateAdminSearchFeatureRequest)

Activate or deactivate a search-related Pennant feature flag

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.AdminSearchApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    AdminSearchApi apiInstance = new AdminSearchApi(defaultClient);
    UpdateAdminSearchFeatureRequest updateAdminSearchFeatureRequest = new UpdateAdminSearchFeatureRequest(); // UpdateAdminSearchFeatureRequest | 
    try {
      apiInstance.updateAdminSearchFeature(updateAdminSearchFeatureRequest);
    } catch (ApiException e) {
      System.err.println("Exception when calling AdminSearchApi#updateAdminSearchFeature");
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
| **updateAdminSearchFeatureRequest** | [**UpdateAdminSearchFeatureRequest**](UpdateAdminSearchFeatureRequest.md)|  | |

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
| **200** | Success |  -  |
| **422** | Unknown feature |  -  |

