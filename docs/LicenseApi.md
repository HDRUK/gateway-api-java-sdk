# LicenseApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createLicenses**](LicenseApi.md#createLicenses) | **POST** /api/v1/licenses | License@store |
| [**deleteLicenses**](LicenseApi.md#deleteLicenses) | **DELETE** /api/v1/licenses/{id} | License@destroy |
| [**editLicenses**](LicenseApi.md#editLicenses) | **PATCH** /api/v1/licenses/{id} | License@edit |
| [**fetchAllLicenses**](LicenseApi.md#fetchAllLicenses) | **GET** /api/v1/licenses | License@index |
| [**fetchLicenses**](LicenseApi.md#fetchLicenses) | **GET** /api/v1/licenses/{id} | License@show |
| [**updateLicenses**](LicenseApi.md#updateLicenses) | **PUT** /api/v1/licenses/{id} | License@update |


<a id="createLicenses"></a>
# **createLicenses**
> CreateDarIntegration201Response createLicenses(createLicensesRequest)

License@store

Creates a new license

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.LicenseApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    LicenseApi apiInstance = new LicenseApi(defaultClient);
    CreateLicensesRequest createLicensesRequest = new CreateLicensesRequest(); // CreateLicensesRequest | License definition
    try {
      CreateDarIntegration201Response result = apiInstance.createLicenses(createLicensesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LicenseApi#createLicenses");
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
| **createLicensesRequest** | [**CreateLicensesRequest**](CreateLicensesRequest.md)| License definition | |

### Return type

[**CreateDarIntegration201Response**](CreateDarIntegration201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **500** | Error |  -  |

<a id="deleteLicenses"></a>
# **deleteLicenses**
> DeleteApplications200Response deleteLicenses(id)

License@destroy

Delete a License

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.LicenseApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    LicenseApi apiInstance = new LicenseApi(defaultClient);
    Integer id = 1; // Integer | License id
    try {
      DeleteApplications200Response result = apiInstance.deleteLicenses(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LicenseApi#deleteLicenses");
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
| **id** | **Integer**| License id | |

### Return type

[**DeleteApplications200Response**](DeleteApplications200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **404** | Not found response |  -  |
| **200** | Success |  -  |
| **500** | Error |  -  |

<a id="editLicenses"></a>
# **editLicenses**
> UpdateLicenses200Response editLicenses(id, createLicensesRequest)

License@edit

Edit a tool license

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.LicenseApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    LicenseApi apiInstance = new LicenseApi(defaultClient);
    Integer id = 1; // Integer | license id
    CreateLicensesRequest createLicensesRequest = new CreateLicensesRequest(); // CreateLicensesRequest | Category definition
    try {
      UpdateLicenses200Response result = apiInstance.editLicenses(id, createLicensesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LicenseApi#editLicenses");
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
| **id** | **Integer**| license id | |
| **createLicensesRequest** | [**CreateLicensesRequest**](CreateLicensesRequest.md)| Category definition | |

### Return type

[**UpdateLicenses200Response**](UpdateLicenses200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **404** | Not found response |  -  |
| **200** | Success |  -  |
| **500** | Error |  -  |

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

<a id="updateLicenses"></a>
# **updateLicenses**
> UpdateLicenses200Response updateLicenses(id, createLicensesRequest)

License@update

Update a tool license

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.LicenseApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    LicenseApi apiInstance = new LicenseApi(defaultClient);
    Integer id = 1; // Integer | license id
    CreateLicensesRequest createLicensesRequest = new CreateLicensesRequest(); // CreateLicensesRequest | Category definition
    try {
      UpdateLicenses200Response result = apiInstance.updateLicenses(id, createLicensesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LicenseApi#updateLicenses");
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
| **id** | **Integer**| license id | |
| **createLicensesRequest** | [**CreateLicensesRequest**](CreateLicensesRequest.md)| Category definition | |

### Return type

[**UpdateLicenses200Response**](UpdateLicenses200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **404** | Not found response |  -  |
| **200** | Success |  -  |
| **500** | Error |  -  |

