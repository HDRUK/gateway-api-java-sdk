# CollectionsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**countUniqueFieldsCollections**](CollectionsApi.md#countUniqueFieldsCollections) | **GET** /api/v1/collections/count/{field} | CollectionController@count |
| [**countUniqueFieldsCollectionsV2**](CollectionsApi.md#countUniqueFieldsCollectionsV2) | **GET** /api/v2/collections/count/{field} | CollectionController@count |
| [**createCollections**](CollectionsApi.md#createCollections) | **POST** /api/v2/collections | CollectionController@store |
| [**deleteCollectionsV2**](CollectionsApi.md#deleteCollectionsV2) | **DELETE** /api/v2/collections/{id} | Delete a collection |
| [**editCollectionsV2**](CollectionsApi.md#editCollectionsV2) | **PATCH** /api/v2/collections/{id} | Edit a collection |
| [**fetchAllCollections**](CollectionsApi.md#fetchAllCollections) | **GET** /api/v1/collections | CollectionController@index |
| [**fetchAllCollectionsV2**](CollectionsApi.md#fetchAllCollectionsV2) | **GET** /api/v2/collections | CollectionController@index |
| [**fetchCollections**](CollectionsApi.md#fetchCollections) | **GET** /api/v1/collections/{id} | CollectionController@show |
| [**fetchCollectionsV2**](CollectionsApi.md#fetchCollectionsV2) | **GET** /api/v2/collections/{id} | CollectionController@show |
| [**updateCollectionsV2**](CollectionsApi.md#updateCollectionsV2) | **PUT** /api/v2/collections/{id} | Update a collection |


<a id="countUniqueFieldsCollections"></a>
# **countUniqueFieldsCollections**
> CountUniqueFieldsCollections200Response countUniqueFieldsCollections(field, teamId, userId)

CollectionController@count

Get Counts for distinct entries of a field in the model

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.CollectionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    CollectionsApi apiInstance = new CollectionsApi(defaultClient);
    String field = "status"; // String | name of the field to perform a count on
    Integer teamId = 1; // Integer | team id
    Integer userId = 1; // Integer | user id
    try {
      CountUniqueFieldsCollections200Response result = apiInstance.countUniqueFieldsCollections(field, teamId, userId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#countUniqueFieldsCollections");
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
| **field** | **String**| name of the field to perform a count on | |
| **teamId** | **Integer**| team id | |
| **userId** | **Integer**| user id | |

### Return type

[**CountUniqueFieldsCollections200Response**](CountUniqueFieldsCollections200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

<a id="countUniqueFieldsCollectionsV2"></a>
# **countUniqueFieldsCollectionsV2**
> CountUniqueFieldsCollections200Response countUniqueFieldsCollectionsV2(field)

CollectionController@count

Get Counts for distinct entries of a field in the model

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.CollectionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    CollectionsApi apiInstance = new CollectionsApi(defaultClient);
    String field = "status"; // String | name of the field to perform a count on
    try {
      CountUniqueFieldsCollections200Response result = apiInstance.countUniqueFieldsCollectionsV2(field);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#countUniqueFieldsCollectionsV2");
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
| **field** | **String**| name of the field to perform a count on | |

### Return type

[**CountUniqueFieldsCollections200Response**](CountUniqueFieldsCollections200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

<a id="createCollections"></a>
# **createCollections**
> CreateDarIntegration201Response createCollections(createCollectionsRequest)

CollectionController@store

Create a new collection owned by an individual

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.CollectionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    CollectionsApi apiInstance = new CollectionsApi(defaultClient);
    CreateCollectionsRequest createCollectionsRequest = new CreateCollectionsRequest(); // CreateCollectionsRequest | Pass user credentials
    try {
      CreateDarIntegration201Response result = apiInstance.createCollections(createCollectionsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#createCollections");
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
| **createCollectionsRequest** | [**CreateCollectionsRequest**](CreateCollectionsRequest.md)| Pass user credentials | |

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
| **201** | Created |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

<a id="deleteCollectionsV2"></a>
# **deleteCollectionsV2**
> DeleteApplications200Response deleteCollectionsV2(id)

Delete a collection

Delete a collection

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.CollectionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    CollectionsApi apiInstance = new CollectionsApi(defaultClient);
    Integer id = 1; // Integer | collection id
    try {
      DeleteApplications200Response result = apiInstance.deleteCollectionsV2(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#deleteCollectionsV2");
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
| **id** | **Integer**| collection id | |

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

<a id="editCollectionsV2"></a>
# **editCollectionsV2**
> FetchCollections200Response editCollectionsV2(id, editCollectionsV2Request, unarchive)

Edit a collection

Edit a collection

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.CollectionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    CollectionsApi apiInstance = new CollectionsApi(defaultClient);
    Integer id = 1; // Integer | collection id
    EditCollectionsV2Request editCollectionsV2Request = new EditCollectionsV2Request(); // EditCollectionsV2Request | Pass user credentials
    String unarchive = "unarchive_example"; // String | Unarchive a collection
    try {
      FetchCollections200Response result = apiInstance.editCollectionsV2(id, editCollectionsV2Request, unarchive);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#editCollectionsV2");
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
| **id** | **Integer**| collection id | |
| **editCollectionsV2Request** | [**EditCollectionsV2Request**](EditCollectionsV2Request.md)| Pass user credentials | |
| **unarchive** | **String**| Unarchive a collection | [optional] |

### Return type

[**FetchCollections200Response**](FetchCollections200Response.md)

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

<a id="fetchAllCollections"></a>
# **fetchAllCollections**
> FetchAllCollections200Response fetchAllCollections(name, teamId, userId, title, status, perPage)

CollectionController@index

Returns a list of collections

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.CollectionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    CollectionsApi apiInstance = new CollectionsApi(defaultClient);
    String name = "name_example"; // String | Filter collections by name
    Integer teamId = 56; // Integer | Filter collections by team ID
    Integer userId = 56; // Integer | Filter collections by user ID
    String title = "title_example"; // String | Filter collections by title
    String status = "status_example"; // String | Filter collections by status (DRAFT, ACTIVE, ARCHIVED)
    Integer perPage = 1; // Integer | per page
    try {
      FetchAllCollections200Response result = apiInstance.fetchAllCollections(name, teamId, userId, title, status, perPage);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#fetchAllCollections");
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
| **name** | **String**| Filter collections by name | [optional] |
| **teamId** | **Integer**| Filter collections by team ID | [optional] |
| **userId** | **Integer**| Filter collections by user ID | [optional] |
| **title** | **String**| Filter collections by title | [optional] |
| **status** | **String**| Filter collections by status (DRAFT, ACTIVE, ARCHIVED) | [optional] |
| **perPage** | **Integer**| per page | [optional] |

### Return type

[**FetchAllCollections200Response**](FetchAllCollections200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="fetchAllCollectionsV2"></a>
# **fetchAllCollectionsV2**
> FetchAllCollections200Response fetchAllCollectionsV2()

CollectionController@index

Returns a list of collections

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.CollectionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    CollectionsApi apiInstance = new CollectionsApi(defaultClient);
    try {
      FetchAllCollections200Response result = apiInstance.fetchAllCollectionsV2();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#fetchAllCollectionsV2");
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

[**FetchAllCollections200Response**](FetchAllCollections200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="fetchCollections"></a>
# **fetchCollections**
> FetchCollections200Response fetchCollections(id, viewType)

CollectionController@show

Get collection by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.CollectionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    CollectionsApi apiInstance = new CollectionsApi(defaultClient);
    Integer id = 1; // Integer | collection id
    String viewType = "full"; // String | Query flag to show full collection data or a trimmed version (defaults to full).
    try {
      FetchCollections200Response result = apiInstance.fetchCollections(id, viewType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#fetchCollections");
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
| **id** | **Integer**| collection id | |
| **viewType** | **String**| Query flag to show full collection data or a trimmed version (defaults to full). | [optional] [default to full] |

### Return type

[**FetchCollections200Response**](FetchCollections200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

<a id="fetchCollectionsV2"></a>
# **fetchCollectionsV2**
> FetchCollections200Response fetchCollectionsV2(id, viewType)

CollectionController@show

Get collection by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.CollectionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    CollectionsApi apiInstance = new CollectionsApi(defaultClient);
    Integer id = 1; // Integer | collection id
    String viewType = "full"; // String | Query flag to show full collection data or a trimmed version (defaults to full).
    try {
      FetchCollections200Response result = apiInstance.fetchCollectionsV2(id, viewType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#fetchCollectionsV2");
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
| **id** | **Integer**| collection id | |
| **viewType** | **String**| Query flag to show full collection data or a trimmed version (defaults to full). | [optional] [default to full] |

### Return type

[**FetchCollections200Response**](FetchCollections200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

<a id="updateCollectionsV2"></a>
# **updateCollectionsV2**
> FetchCollections200Response updateCollectionsV2(id, updateCollectionsV2Request)

Update a collection

Update a collection owned by an individual

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.CollectionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    CollectionsApi apiInstance = new CollectionsApi(defaultClient);
    Integer id = 1; // Integer | collection id
    UpdateCollectionsV2Request updateCollectionsV2Request = new UpdateCollectionsV2Request(); // UpdateCollectionsV2Request | Pass user credentials
    try {
      FetchCollections200Response result = apiInstance.updateCollectionsV2(id, updateCollectionsV2Request);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#updateCollectionsV2");
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
| **id** | **Integer**| collection id | |
| **updateCollectionsV2Request** | [**UpdateCollectionsV2Request**](UpdateCollectionsV2Request.md)| Pass user credentials | |

### Return type

[**FetchCollections200Response**](FetchCollections200Response.md)

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

