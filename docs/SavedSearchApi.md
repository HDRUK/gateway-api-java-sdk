# SavedSearchApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createSavedSearches**](SavedSearchApi.md#createSavedSearches) | **POST** /api/v1/saved_searches | SavedSearch@store |
| [**deleteSavedSearches**](SavedSearchApi.md#deleteSavedSearches) | **DELETE** /api/v1/saved_searches/{id} | SavedSearch@destroy |
| [**editSavedSearches**](SavedSearchApi.md#editSavedSearches) | **PATCH** /api/v1/saved_searches/{id} | SavedSearch@update |
| [**fetchAllSavedSearches**](SavedSearchApi.md#fetchAllSavedSearches) | **GET** /api/v1/saved_searches | SavedSearch@index |
| [**fetchSavedSearches**](SavedSearchApi.md#fetchSavedSearches) | **GET** /api/v1/saved_searches/{id} | SavedSearch@show |
| [**updateSavedSearches**](SavedSearchApi.md#updateSavedSearches) | **PUT** /api/v1/saved_searches/{id} | SavedSearch@update |


<a id="createSavedSearches"></a>
# **createSavedSearches**
> CreateCategories200Response createSavedSearches(createSavedSearchesRequest)

SavedSearch@store

Creates a new saved search

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.SavedSearchApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    SavedSearchApi apiInstance = new SavedSearchApi(defaultClient);
    CreateSavedSearchesRequest createSavedSearchesRequest = new CreateSavedSearchesRequest(); // CreateSavedSearchesRequest | Saved search definition
    try {
      CreateCategories200Response result = apiInstance.createSavedSearches(createSavedSearchesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SavedSearchApi#createSavedSearches");
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
| **createSavedSearchesRequest** | [**CreateSavedSearchesRequest**](CreateSavedSearchesRequest.md)| Saved search definition | |

### Return type

[**CreateCategories200Response**](CreateCategories200Response.md)

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

<a id="deleteSavedSearches"></a>
# **deleteSavedSearches**
> DeleteAliases200Response deleteSavedSearches(id)

SavedSearch@destroy

Delete a saved search

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.SavedSearchApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    SavedSearchApi apiInstance = new SavedSearchApi(defaultClient);
    Integer id = 1; // Integer | saved search id
    try {
      DeleteAliases200Response result = apiInstance.deleteSavedSearches(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SavedSearchApi#deleteSavedSearches");
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
| **id** | **Integer**| saved search id | |

### Return type

[**DeleteAliases200Response**](DeleteAliases200Response.md)

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

<a id="editSavedSearches"></a>
# **editSavedSearches**
> UpdateSavedSearches200Response editSavedSearches(id, editSavedSearchesRequest)

SavedSearch@update

Edit a saved search

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.SavedSearchApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    SavedSearchApi apiInstance = new SavedSearchApi(defaultClient);
    Integer id = 1; // Integer | saved search id
    EditSavedSearchesRequest editSavedSearchesRequest = new EditSavedSearchesRequest(); // EditSavedSearchesRequest | Saved search definition
    try {
      UpdateSavedSearches200Response result = apiInstance.editSavedSearches(id, editSavedSearchesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SavedSearchApi#editSavedSearches");
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
| **id** | **Integer**| saved search id | |
| **editSavedSearchesRequest** | [**EditSavedSearchesRequest**](EditSavedSearchesRequest.md)| Saved search definition | |

### Return type

[**UpdateSavedSearches200Response**](UpdateSavedSearches200Response.md)

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

<a id="fetchAllSavedSearches"></a>
# **fetchAllSavedSearches**
> FetchAllSavedSearches200Response fetchAllSavedSearches(perPage)

SavedSearch@index

Returns a list of saved searches enabled on the system

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.SavedSearchApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    SavedSearchApi apiInstance = new SavedSearchApi(defaultClient);
    Integer perPage = 56; // Integer | Specify number of results per page
    try {
      FetchAllSavedSearches200Response result = apiInstance.fetchAllSavedSearches(perPage);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SavedSearchApi#fetchAllSavedSearches");
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
| **perPage** | **Integer**| Specify number of results per page | [optional] |

### Return type

[**FetchAllSavedSearches200Response**](FetchAllSavedSearches200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="fetchSavedSearches"></a>
# **fetchSavedSearches**
> FetchAllSavedSearches200Response fetchSavedSearches(id)

SavedSearch@show

Return a single saved search

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.SavedSearchApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    SavedSearchApi apiInstance = new SavedSearchApi(defaultClient);
    Integer id = 1; // Integer | saved search id
    try {
      FetchAllSavedSearches200Response result = apiInstance.fetchSavedSearches(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SavedSearchApi#fetchSavedSearches");
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
| **id** | **Integer**| saved search id | |

### Return type

[**FetchAllSavedSearches200Response**](FetchAllSavedSearches200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **404** | Not found response |  -  |

<a id="updateSavedSearches"></a>
# **updateSavedSearches**
> UpdateSavedSearches200Response updateSavedSearches(id, updateSavedSearchesRequest)

SavedSearch@update

Update a saved search

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.SavedSearchApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    SavedSearchApi apiInstance = new SavedSearchApi(defaultClient);
    Integer id = 1; // Integer | saved search id
    UpdateSavedSearchesRequest updateSavedSearchesRequest = new UpdateSavedSearchesRequest(); // UpdateSavedSearchesRequest | Saved search definition
    try {
      UpdateSavedSearches200Response result = apiInstance.updateSavedSearches(id, updateSavedSearchesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SavedSearchApi#updateSavedSearches");
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
| **id** | **Integer**| saved search id | |
| **updateSavedSearchesRequest** | [**UpdateSavedSearchesRequest**](UpdateSavedSearchesRequest.md)| Saved search definition | |

### Return type

[**UpdateSavedSearches200Response**](UpdateSavedSearches200Response.md)

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

