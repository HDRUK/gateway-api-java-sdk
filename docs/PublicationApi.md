# PublicationApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**countTeamUniqueFieldsPublicationV2**](PublicationApi.md#countTeamUniqueFieldsPublicationV2) | **GET** /api/v2/teams/{teamId}/publications/count/{field} | TeamPublicationController@count |
| [**countUniqueFieldsPublications**](PublicationApi.md#countUniqueFieldsPublications) | **GET** /api/v1/publication/count/{field} | PublicationController@count |
| [**countUserUniqueFieldsPublicationV2**](PublicationApi.md#countUserUniqueFieldsPublicationV2) | **GET** /api/v2/users/{userId}/publications/count/{field} | UserPublicationController@count |
| [**createPublications**](PublicationApi.md#createPublications) | **POST** /api/v1/publications | PublicationController@store |
| [**createPublicationsV2ByTeamId**](PublicationApi.md#createPublicationsV2ByTeamId) | **POST** /api/v2/teams/{teamId}/publications | TeamPublicationController@store |
| [**createPublicationsV2ByUserId**](PublicationApi.md#createPublicationsV2ByUserId) | **POST** /api/v2/users/{userId}/publications | UserPublicationController@store |
| [**deletePublications**](PublicationApi.md#deletePublications) | **DELETE** /api/v1/publications/{id} | PublicationController@destroy |
| [**deletePublicationsV2ByTeamId**](PublicationApi.md#deletePublicationsV2ByTeamId) | **DELETE** /api/v2/teams/{teamId}/publications/{id} | TeamPublicationController@destroy |
| [**deletePublicationsV2ByUserId**](PublicationApi.md#deletePublicationsV2ByUserId) | **DELETE** /api/v2/users/{userId}/publications/{id} | UserPublicationController@destroy |
| [**editPublications**](PublicationApi.md#editPublications) | **PATCH** /api/v1/publications/{id} | PublicationController@edit |
| [**editPublicationsV2ByTeamId**](PublicationApi.md#editPublicationsV2ByTeamId) | **PATCH** /api/v2/teams/{teamId}/publications/{id} | TeamPublicationController@edit |
| [**editPublicationsV2ByUserId**](PublicationApi.md#editPublicationsV2ByUserId) | **PATCH** /api/v2/users/{userId}/publications/{id} | UserPublicationController@edit |
| [**fetchAllPublications**](PublicationApi.md#fetchAllPublications) | **GET** /api/v1/publications | PublicationController@index |
| [**fetchAllPublicationsByTeamAndStatusV2**](PublicationApi.md#fetchAllPublicationsByTeamAndStatusV2) | **GET** /api/v2/teams/{teamId}/publications/status/{status} | TeamPublicationController@indexStatus |
| [**fetchAllPublicationsByUserAndStatusV2**](PublicationApi.md#fetchAllPublicationsByUserAndStatusV2) | **GET** /api/v2/users/{userId}/publications/{status} | UserPublicationController@indexStatus |
| [**fetchAllPublicationsV2**](PublicationApi.md#fetchAllPublicationsV2) | **GET** /api/v2/publications | PublicationController@indexActive |
| [**fetchPublications**](PublicationApi.md#fetchPublications) | **GET** /api/v1/publications/{id} | PublicationController@show |
| [**fetchPublicationsByTeamAndByIdV2**](PublicationApi.md#fetchPublicationsByTeamAndByIdV2) | **GET** /api/v2/teams/{teamId}/publications/{id} | TeamPublicationController@show |
| [**fetchPublicationsByUserAndByIdV2**](PublicationApi.md#fetchPublicationsByUserAndByIdV2) | **GET** /api/v2/users/{userId}/publications/{id} | UserPublicationController@show |
| [**fetchPublicationsV2**](PublicationApi.md#fetchPublicationsV2) | **GET** /api/v2/publications/{id} | PublicationController@showActive |
| [**updatePublications**](PublicationApi.md#updatePublications) | **PUT** /api/v1/publications/{id} | PublicationController@update |
| [**updatePublicationsV2ByTeamId**](PublicationApi.md#updatePublicationsV2ByTeamId) | **PUT** /api/v2/teams/{teamId}/publications/{id} | TeamPublicationController@update |
| [**updatePublicationsV2ByUserId**](PublicationApi.md#updatePublicationsV2ByUserId) | **PUT** /api/v2/users/{userId}/publications/{id} | UserPublicationController@update |


<a id="countTeamUniqueFieldsPublicationV2"></a>
# **countTeamUniqueFieldsPublicationV2**
> CountUniqueFieldsCollections200Response countTeamUniqueFieldsPublicationV2(teamId, field)

TeamPublicationController@count

Get team counts for distinct entries of a field in the model

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
    Integer teamId = 1; // Integer | team id
    String field = "status"; // String | name of the field to perform a count on
    try {
      CountUniqueFieldsCollections200Response result = apiInstance.countTeamUniqueFieldsPublicationV2(teamId, field);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicationApi#countTeamUniqueFieldsPublicationV2");
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
| **teamId** | **Integer**| team id | |
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

<a id="countUserUniqueFieldsPublicationV2"></a>
# **countUserUniqueFieldsPublicationV2**
> CountUniqueFieldsCollections200Response countUserUniqueFieldsPublicationV2(userId, field)

UserPublicationController@count

Get user counts for distinct entries of a field in the model

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
    Integer userId = 1; // Integer | user id
    String field = "status"; // String | name of the field to perform a count on
    try {
      CountUniqueFieldsCollections200Response result = apiInstance.countUserUniqueFieldsPublicationV2(userId, field);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicationApi#countUserUniqueFieldsPublicationV2");
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
| **userId** | **Integer**| user id | |
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

<a id="createPublications"></a>
# **createPublications**
> CreateCategories200Response createPublications(createPublicationsRequest)

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
      CreateCategories200Response result = apiInstance.createPublications(createPublicationsRequest);
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

[**CreateCategories200Response**](CreateCategories200Response.md)

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

<a id="createPublicationsV2ByTeamId"></a>
# **createPublicationsV2ByTeamId**
> CreateCategories200Response createPublicationsV2ByTeamId(teamId, createPublicationsRequest)

TeamPublicationController@store

Create a new publication by team id

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
    Integer teamId = 1; // Integer | team id
    CreatePublicationsRequest createPublicationsRequest = new CreatePublicationsRequest(); // CreatePublicationsRequest | Pass user credentials
    try {
      CreateCategories200Response result = apiInstance.createPublicationsV2ByTeamId(teamId, createPublicationsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicationApi#createPublicationsV2ByTeamId");
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
| **teamId** | **Integer**| team id | |
| **createPublicationsRequest** | [**CreatePublicationsRequest**](CreatePublicationsRequest.md)| Pass user credentials | |

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
| **201** | Created |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

<a id="createPublicationsV2ByUserId"></a>
# **createPublicationsV2ByUserId**
> CreateCategories200Response createPublicationsV2ByUserId(userId, createPublicationsRequest)

UserPublicationController@store

Create a new publication by user id

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
    Long userId = 56L; // Long | ID of the user
    CreatePublicationsRequest createPublicationsRequest = new CreatePublicationsRequest(); // CreatePublicationsRequest | Pass user credentials
    try {
      CreateCategories200Response result = apiInstance.createPublicationsV2ByUserId(userId, createPublicationsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicationApi#createPublicationsV2ByUserId");
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
| **userId** | **Long**| ID of the user | |
| **createPublicationsRequest** | [**CreatePublicationsRequest**](CreatePublicationsRequest.md)| Pass user credentials | |

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

<a id="deletePublicationsV2ByTeamId"></a>
# **deletePublicationsV2ByTeamId**
> DeleteFederation200Response deletePublicationsV2ByTeamId(teamId, id)

TeamPublicationController@destroy

Delete publication by team id and id

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
    Integer teamId = 1; // Integer | team id
    Integer id = 1; // Integer | publication id
    try {
      DeleteFederation200Response result = apiInstance.deletePublicationsV2ByTeamId(teamId, id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicationApi#deletePublicationsV2ByTeamId");
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
| **teamId** | **Integer**| team id | |
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

<a id="deletePublicationsV2ByUserId"></a>
# **deletePublicationsV2ByUserId**
> DeleteFederation200Response deletePublicationsV2ByUserId(userId, id)

UserPublicationController@destroy

Delete publication by user id and id

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
    Long userId = 56L; // Long | ID of the user
    Integer id = 1; // Integer | publication id
    try {
      DeleteFederation200Response result = apiInstance.deletePublicationsV2ByUserId(userId, id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicationApi#deletePublicationsV2ByUserId");
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
| **userId** | **Long**| ID of the user | |
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

<a id="editPublicationsV2ByTeamId"></a>
# **editPublicationsV2ByTeamId**
> FetchPublications200Response editPublicationsV2ByTeamId(teamId, id, updatePublicationsRequest)

TeamPublicationController@edit

Edit publications by team id

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
    Integer teamId = 1; // Integer | team id
    Integer id = 1; // Integer | publications id
    UpdatePublicationsRequest updatePublicationsRequest = new UpdatePublicationsRequest(); // UpdatePublicationsRequest | Pass user credentials
    try {
      FetchPublications200Response result = apiInstance.editPublicationsV2ByTeamId(teamId, id, updatePublicationsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicationApi#editPublicationsV2ByTeamId");
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
| **teamId** | **Integer**| team id | |
| **id** | **Integer**| publications id | |
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

<a id="editPublicationsV2ByUserId"></a>
# **editPublicationsV2ByUserId**
> FetchPublications200Response editPublicationsV2ByUserId(userId, id, updatePublicationsRequest)

UserPublicationController@edit

Edit publications by user id

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
    Long userId = 56L; // Long | ID of the user
    Integer id = 1; // Integer | publications id
    UpdatePublicationsRequest updatePublicationsRequest = new UpdatePublicationsRequest(); // UpdatePublicationsRequest | Pass user credentials
    try {
      FetchPublications200Response result = apiInstance.editPublicationsV2ByUserId(userId, id, updatePublicationsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicationApi#editPublicationsV2ByUserId");
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
| **userId** | **Long**| ID of the user | |
| **id** | **Integer**| publications id | |
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

<a id="fetchAllPublicationsByTeamAndStatusV2"></a>
# **fetchAllPublicationsByTeamAndStatusV2**
> FetchAllPublications200Response fetchAllPublicationsByTeamAndStatusV2(teamId, status, paperTitle)

TeamPublicationController@indexStatus

Returns a list of a teams publications

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.PublicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    PublicationApi apiInstance = new PublicationApi(defaultClient);
    Long teamId = 56L; // Long | ID of the team
    String status = "active"; // String | Status of the team (active, draft, or archived). Defaults to active if not provided.
    String paperTitle = "paperTitle_example"; // String | Filter Publication by title
    try {
      FetchAllPublications200Response result = apiInstance.fetchAllPublicationsByTeamAndStatusV2(teamId, status, paperTitle);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicationApi#fetchAllPublicationsByTeamAndStatusV2");
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
| **teamId** | **Long**| ID of the team | |
| **status** | **String**| Status of the team (active, draft, or archived). Defaults to active if not provided. | [default to active] [enum: active, draft, archived] |
| **paperTitle** | **String**| Filter Publication by title | [optional] |

### Return type

[**FetchAllPublications200Response**](FetchAllPublications200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **404** | Not Found |  -  |

<a id="fetchAllPublicationsByUserAndStatusV2"></a>
# **fetchAllPublicationsByUserAndStatusV2**
> FetchAllPublications200Response fetchAllPublicationsByUserAndStatusV2(userId, status, paperTitle)

UserPublicationController@indexStatus

Returns a list of a users publications

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.PublicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    PublicationApi apiInstance = new PublicationApi(defaultClient);
    Long userId = 56L; // Long | ID of the user
    String status = "active"; // String | Status of the team (active, draft, or archived). Defaults to active if not provided.
    String paperTitle = "paperTitle_example"; // String | Filter Publication by title
    try {
      FetchAllPublications200Response result = apiInstance.fetchAllPublicationsByUserAndStatusV2(userId, status, paperTitle);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicationApi#fetchAllPublicationsByUserAndStatusV2");
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
| **userId** | **Long**| ID of the user | |
| **status** | **String**| Status of the team (active, draft, or archived). Defaults to active if not provided. | [default to active] [enum: active, draft, archived] |
| **paperTitle** | **String**| Filter Publication by title | [optional] |

### Return type

[**FetchAllPublications200Response**](FetchAllPublications200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **404** | Not Found |  -  |

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

<a id="fetchPublicationsByTeamAndByIdV2"></a>
# **fetchPublicationsByTeamAndByIdV2**
> FetchPublications200Response fetchPublicationsByTeamAndByIdV2(teamId, id)

TeamPublicationController@show

Get publication by team id and by id

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
    Integer teamId = 1; // Integer | team id
    Integer id = 1; // Integer | publication id
    try {
      FetchPublications200Response result = apiInstance.fetchPublicationsByTeamAndByIdV2(teamId, id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicationApi#fetchPublicationsByTeamAndByIdV2");
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
| **teamId** | **Integer**| team id | |
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

<a id="fetchPublicationsByUserAndByIdV2"></a>
# **fetchPublicationsByUserAndByIdV2**
> FetchPublications200Response fetchPublicationsByUserAndByIdV2(userId, id)

UserPublicationController@show

Get publication by user id and by id

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
    Long userId = 56L; // Long | ID of the user
    Integer id = 1; // Integer | publication id
    try {
      FetchPublications200Response result = apiInstance.fetchPublicationsByUserAndByIdV2(userId, id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicationApi#fetchPublicationsByUserAndByIdV2");
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
| **userId** | **Long**| ID of the user | |
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

<a id="updatePublicationsV2ByTeamId"></a>
# **updatePublicationsV2ByTeamId**
> FetchPublications200Response updatePublicationsV2ByTeamId(teamId, id, updatePublicationsRequest)

TeamPublicationController@update

Update publications by team id

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
    Integer teamId = 1; // Integer | team id
    Integer id = 1; // Integer | publication id
    UpdatePublicationsRequest updatePublicationsRequest = new UpdatePublicationsRequest(); // UpdatePublicationsRequest | Pass user credentials
    try {
      FetchPublications200Response result = apiInstance.updatePublicationsV2ByTeamId(teamId, id, updatePublicationsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicationApi#updatePublicationsV2ByTeamId");
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
| **teamId** | **Integer**| team id | |
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

<a id="updatePublicationsV2ByUserId"></a>
# **updatePublicationsV2ByUserId**
> FetchPublications200Response updatePublicationsV2ByUserId(userId, id, updatePublicationsRequest)

UserPublicationController@update

Update publications by user id

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
    Long userId = 56L; // Long | ID of the user
    Integer id = 1; // Integer | publication id
    UpdatePublicationsRequest updatePublicationsRequest = new UpdatePublicationsRequest(); // UpdatePublicationsRequest | Pass user credentials
    try {
      FetchPublications200Response result = apiInstance.updatePublicationsV2ByUserId(userId, id, updatePublicationsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PublicationApi#updatePublicationsV2ByUserId");
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
| **userId** | **Long**| ID of the user | |
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

