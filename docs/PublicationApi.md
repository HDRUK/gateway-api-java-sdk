# PublicationApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**countUniqueFieldsPublications**](PublicationApi.md#countUniqueFieldsPublications) | **GET** /api/v1/publication/count/{field} | PublicationController@count |
| [**createPublications**](PublicationApi.md#createPublications) | **POST** /api/v1/publications | PublicationController@store |
| [**deletePublications**](PublicationApi.md#deletePublications) | **DELETE** /api/v1/publications/{id} | PublicationController@destroy |
| [**editPublications**](PublicationApi.md#editPublications) | **PATCH** /api/v1/publications/{id} | PublicationController@edit |
| [**fetchAllPublications**](PublicationApi.md#fetchAllPublications) | **GET** /api/v1/publications | PublicationController@index |
| [**fetchAllPublicationsV2**](PublicationApi.md#fetchAllPublicationsV2) | **GET** /api/v2/publications | PublicationController@indexActive |
| [**fetchPublications**](PublicationApi.md#fetchPublications) | **GET** /api/v1/publications/{id} | PublicationController@show |
| [**fetchPublicationsV2**](PublicationApi.md#fetchPublicationsV2) | **GET** /api/v2/publications/{id} | PublicationController@showActive |
| [**updatePublications**](PublicationApi.md#updatePublications) | **PUT** /api/v1/publications/{id} | PublicationController@update |


<a id="countUniqueFieldsPublications"></a>
# **countUniqueFieldsPublications**
> CountUniqueFieldsCollections200Response countUniqueFieldsPublications(field, ownerId, teamId)

PublicationController@count

Get Counts for distinct entries of a field in the model

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.PublicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PublicationApi apiInstance = new PublicationApi(defaultClient);
    String field = "status"; // String | name of the field to perform a count on
    Integer ownerId = 1; // Integer | owner id
    Integer teamId = 1; // Integer | 
    try {
      CountUniqueFieldsCollections200Response result = apiInstance.countUniqueFieldsPublications(field, ownerId, teamId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicationApi#countUniqueFieldsPublications");
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
| **ownerId** | **Integer**| owner id | |
| **teamId** | **Integer**|  | [optional] |

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

<a id="createPublications"></a>
# **createPublications**
> CreateDarIntegration201Response createPublications(createPublicationsRequest)

PublicationController@store

Create a new publication

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.PublicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PublicationApi apiInstance = new PublicationApi(defaultClient);
    CreatePublicationsRequest createPublicationsRequest = new CreatePublicationsRequest(); // CreatePublicationsRequest | Pass user credentials
    try {
      CreateDarIntegration201Response result = apiInstance.createPublications(createPublicationsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicationApi#createPublications");
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
| **createPublicationsRequest** | [**CreatePublicationsRequest**](CreatePublicationsRequest.md)| Pass user credentials | |

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

<a id="deletePublications"></a>
# **deletePublications**
> DeleteFederation200Response deletePublications(id)

PublicationController@destroy

Delete publication by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.PublicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PublicationApi apiInstance = new PublicationApi(defaultClient);
    Integer id = 1; // Integer | publication id
    try {
      DeleteFederation200Response result = apiInstance.deletePublications(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicationApi#deletePublications");
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
| **id** | **Integer**| publication id | |

### Return type

[**DeleteFederation200Response**](DeleteFederation200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **401** | Unauthorized |  -  |
| **404** | Error response |  -  |
| **500** | Error |  -  |

<a id="editPublications"></a>
# **editPublications**
> FetchPublications200Response editPublications(id, updatePublicationsRequest, unarchive)

PublicationController@edit

Edit publications

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.PublicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PublicationApi apiInstance = new PublicationApi(defaultClient);
    Integer id = 1; // Integer | publications id
    UpdatePublicationsRequest updatePublicationsRequest = new UpdatePublicationsRequest(); // UpdatePublicationsRequest | Pass user credentials
    String unarchive = "unarchive_example"; // String | Unarchive a publication
    try {
      FetchPublications200Response result = apiInstance.editPublications(id, updatePublicationsRequest, unarchive);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicationApi#editPublications");
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
| **id** | **Integer**| publications id | |
| **updatePublicationsRequest** | [**UpdatePublicationsRequest**](UpdatePublicationsRequest.md)| Pass user credentials | |
| **unarchive** | **String**| Unarchive a publication | [optional] |

### Return type

[**FetchPublications200Response**](FetchPublications200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **400** | Error |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

<a id="fetchAllPublications"></a>
# **fetchAllPublications**
> FetchAllPublications200Response fetchAllPublications(paperTitle, ownerId, teamId, status)

PublicationController@index

Get All Publications

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.PublicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PublicationApi apiInstance = new PublicationApi(defaultClient);
    String paperTitle = "paperTitle_example"; // String | Filter tools by paper title
    Integer ownerId = 56; // Integer | Filter tools by owner id
    Integer teamId = 56; // Integer | Filter tools by team id
    String status = "ACTIVE"; // String | Publication status to filter by ('ACTIVE', 'DRAFT', 'ARCHIVED')
    try {
      FetchAllPublications200Response result = apiInstance.fetchAllPublications(paperTitle, ownerId, teamId, status);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicationApi#fetchAllPublications");
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
| **paperTitle** | **String**| Filter tools by paper title | [optional] |
| **ownerId** | [**Integer**](.md)| Filter tools by owner id | [optional] |
| **teamId** | [**Integer**](.md)| Filter tools by team id | [optional] |
| **status** | **String**| Publication status to filter by (&#39;ACTIVE&#39;, &#39;DRAFT&#39;, &#39;ARCHIVED&#39;) | [optional] |

### Return type

[**FetchAllPublications200Response**](FetchAllPublications200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

<a id="fetchAllPublicationsV2"></a>
# **fetchAllPublicationsV2**
> FetchAllPublications200Response fetchAllPublicationsV2(paperTitle, withRelated, perPage)

PublicationController@indexActive

Get All Publications

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.PublicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PublicationApi apiInstance = new PublicationApi(defaultClient);
    String paperTitle = "paperTitle_example"; // String | Filter tools by paper title
    Boolean withRelated = true; // Boolean | Return related datasets
    Integer perPage = 1; // Integer | per page
    try {
      FetchAllPublications200Response result = apiInstance.fetchAllPublicationsV2(paperTitle, withRelated, perPage);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicationApi#fetchAllPublicationsV2");
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
| **paperTitle** | **String**| Filter tools by paper title | [optional] |
| **withRelated** | **Boolean**| Return related datasets | [optional] |
| **perPage** | **Integer**| per page | [optional] |

### Return type

[**FetchAllPublications200Response**](FetchAllPublications200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

<a id="fetchPublications"></a>
# **fetchPublications**
> FetchPublications200Response fetchPublications(id)

PublicationController@show

Get publication by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.PublicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PublicationApi apiInstance = new PublicationApi(defaultClient);
    Integer id = 1; // Integer | publication id
    try {
      FetchPublications200Response result = apiInstance.fetchPublications(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicationApi#fetchPublications");
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
| **id** | **Integer**| publication id | |

### Return type

[**FetchPublications200Response**](FetchPublications200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **401** | Unauthorized |  -  |
| **404** | Not found response |  -  |

<a id="fetchPublicationsV2"></a>
# **fetchPublicationsV2**
> FetchPublications200Response fetchPublicationsV2(id)

PublicationController@showActive

Get publication by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.PublicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PublicationApi apiInstance = new PublicationApi(defaultClient);
    Integer id = 1; // Integer | publication id
    try {
      FetchPublications200Response result = apiInstance.fetchPublicationsV2(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicationApi#fetchPublicationsV2");
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
| **id** | **Integer**| publication id | |

### Return type

[**FetchPublications200Response**](FetchPublications200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **401** | Unauthorized |  -  |
| **404** | Not found response |  -  |

<a id="updatePublications"></a>
# **updatePublications**
> FetchPublications200Response updatePublications(id, updatePublicationsRequest)

PublicationController@update

Update publications

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.PublicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PublicationApi apiInstance = new PublicationApi(defaultClient);
    Integer id = 1; // Integer | publication id
    UpdatePublicationsRequest updatePublicationsRequest = new UpdatePublicationsRequest(); // UpdatePublicationsRequest | Pass user credentials
    try {
      FetchPublications200Response result = apiInstance.updatePublications(id, updatePublicationsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicationApi#updatePublications");
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
| **id** | **Integer**| publication id | |
| **updatePublicationsRequest** | [**UpdatePublicationsRequest**](UpdatePublicationsRequest.md)| Pass user credentials | |

### Return type

[**FetchPublications200Response**](FetchPublications200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **400** | Error |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

