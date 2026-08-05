# LicenseApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**fetchAllLicenses**](LicenseApi.md#fetchAllLicenses) | **GET** /api/v1/licenses | License@index |
| [**fetchLicenses**](LicenseApi.md#fetchLicenses) | **GET** /api/v1/licenses/{id} | License@show |


<a id="fetchAllLicenses"></a>
# **fetchAllLicenses**
> FetchAllLicenses200Response fetchAllLicenses()

License@index

Returns a list of licenses available

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.LicenseApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    LicenseApi apiInstance = new LicenseApi(defaultClient);
    try {
      FetchAllLicenses200Response result = apiInstance.fetchAllLicenses();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LicenseApi#fetchAllLicenses");
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

[**FetchAllLicenses200Response**](FetchAllLicenses200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="fetchLicenses"></a>
# **fetchLicenses**
> FetchLicenses200Response fetchLicenses(id)

License@show

Return a single license

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.LicenseApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    LicenseApi apiInstance = new LicenseApi(defaultClient);
    Integer id = 1; // Integer | License ID
    try {
      FetchLicenses200Response result = apiInstance.fetchLicenses(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LicenseApi#fetchLicenses");
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
| **id** | **Integer**| License ID | |

### Return type

[**FetchLicenses200Response**](FetchLicenses200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **404** | Not found response |  -  |

