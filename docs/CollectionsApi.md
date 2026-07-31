# CollectionsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**countTeamUniqueFieldsCollectionV2**](CollectionsApi.md#countTeamUniqueFieldsCollectionV2) | **GET** /api/v2/teams/{teamId}/collections/count/{field} | TeamCollectionController@count |
| [**countUniqueFieldsCollections**](CollectionsApi.md#countUniqueFieldsCollections) | **GET** /api/v1/collections/count/{field} | CollectionController@count |
| [**countUniqueFieldsCollectionsV2**](CollectionsApi.md#countUniqueFieldsCollectionsV2) | **GET** /api/v2/collections/count/{field} | CollectionController@count |
| [**countUserUniqueFieldsCollectionV2**](CollectionsApi.md#countUserUniqueFieldsCollectionV2) | **GET** /api/v2/users/{userId}/collections/count/{field} | UserCollectionController@count |
| [**createCollections**](CollectionsApi.md#createCollections) | **POST** /api/v2/collections | CollectionController@store |
| [**createTeamCollections**](CollectionsApi.md#createTeamCollections) | **POST** /api/v1/teams/{teamId}/collections | CollectionController@store |
| [**createTeamCollectionsV2**](CollectionsApi.md#createTeamCollectionsV2) | **POST** /api/v2/teams/{teamId}/collections | TeamCollectionController@store |
| [**createUserCollections**](CollectionsApi.md#createUserCollections) | **POST** /api/v2/users/collections | UserCollectionController@store |
| [**deleteCollectionsV2**](CollectionsApi.md#deleteCollectionsV2) | **DELETE** /api/v2/collections/{id} | Delete a collection |
| [**deleteTeamCollections**](CollectionsApi.md#deleteTeamCollections) | **DELETE** /api/v1/teams/{teamId}/collections/{id} | Delete a collection |
| [**deleteTeamCollectionsV2**](CollectionsApi.md#deleteTeamCollectionsV2) | **DELETE** /api/v2/teams/{teamId}/collections/{id} | Delete a collection |
| [**deleteUserCollectionsV2**](CollectionsApi.md#deleteUserCollectionsV2) | **DELETE** /api/v2/users/{userId}/collections/{id} | Delete a collection |
| [**editCollectionsV2**](CollectionsApi.md#editCollectionsV2) | **PATCH** /api/v2/collections/{id} | Edit a collection |
| [**editTeamCollections**](CollectionsApi.md#editTeamCollections) | **PATCH** /api/v1/teams/{teamId}/collections/{id} | Edit a collection |
| [**editTeamCollectionsV2**](CollectionsApi.md#editTeamCollectionsV2) | **PATCH** /api/v2/teams/{teamId}/collections/{id} | Edit a collection |
| [**editUserCollectionsV2**](CollectionsApi.md#editUserCollectionsV2) | **PATCH** /api/v2/users/{userId}/collections/{id} | Edit a collection |
| [**fetchAllCollections**](CollectionsApi.md#fetchAllCollections) | **GET** /api/v1/collections | CollectionController@index |
| [**fetchAllCollectionsV2**](CollectionsApi.md#fetchAllCollectionsV2) | **GET** /api/v2/collections | CollectionController@index |
| [**fetchCollections**](CollectionsApi.md#fetchCollections) | **GET** /api/v1/collections/{id} | CollectionController@show |
| [**fetchCollectionsV2**](CollectionsApi.md#fetchCollectionsV2) | **GET** /api/v2/collections/{id} | CollectionController@show |
| [**fetchTeamActiveCollectionsV2**](CollectionsApi.md#fetchTeamActiveCollectionsV2) | **GET** /api/v2/teams/{teamId}/collections/status/active | TeamCollectionController@indexActive |
| [**fetchTeamArchivedCollectionsV2**](CollectionsApi.md#fetchTeamArchivedCollectionsV2) | **GET** /api/v2/teams/{teamId}/collections/status/archived | TeamCollectionController@indexArchived |
| [**fetchTeamCollectionV2**](CollectionsApi.md#fetchTeamCollectionV2) | **GET** /api/v2/teams/{teamId}/collections/{id} | TeamCollectionController@show |
| [**fetchTeamDraftCollectionsV2**](CollectionsApi.md#fetchTeamDraftCollectionsV2) | **GET** /api/v2/teams/{teamId}/collections/status/draft | TeamCollectionController@indexDraft |
| [**fetchUserArchivedCollectionsV2**](CollectionsApi.md#fetchUserArchivedCollectionsV2) | **GET** /api/v2/users/{userId}/collections/status/archived | UserCollectionController@indexArchived |
| [**fetchUserCollectionV2**](CollectionsApi.md#fetchUserCollectionV2) | **GET** /api/v2/users/{userId}/collections/{id} | CollectionController@show |
| [**fetchUserCollectionsV2**](CollectionsApi.md#fetchUserCollectionsV2) | **GET** /api/v2/users/{userId}/collections/status/active | UserCollectionController@indexActive |
| [**fetchUserDraftCollectionsV2**](CollectionsApi.md#fetchUserDraftCollectionsV2) | **GET** /api/v2/users/{userId}/collections/status/draft | UserCollectionController@indexDraft |
| [**updateCollectionsV2**](CollectionsApi.md#updateCollectionsV2) | **PUT** /api/v2/collections/{id} | Update a collection |
| [**updateTeamCollections**](CollectionsApi.md#updateTeamCollections) | **PUT** /api/v1/teams/{teamId}/collections/{id} | Update a collection |
| [**updateTeamCollectionsV2**](CollectionsApi.md#updateTeamCollectionsV2) | **PUT** /api/v2/teams/{teamId}/collections/{id} | Update a collection |
| [**updateUserCollectionsV2**](CollectionsApi.md#updateUserCollectionsV2) | **PUT** /api/v2/users/{userId}/collections/{id} | Update a collection |


<a id="countTeamUniqueFieldsCollectionV2"></a>
# **countTeamUniqueFieldsCollectionV2**
> CountUniqueFieldsCollections200Response countTeamUniqueFieldsCollectionV2(teamId, field)

TeamCollectionController@count

Get user counts for distinct entries of a field in the model

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
    Integer teamId = 1; // Integer | team id
    String field = "status"; // String | name of the field to perform a count on
    try {
      CountUniqueFieldsCollections200Response result = apiInstance.countTeamUniqueFieldsCollectionV2(teamId, field);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#countTeamUniqueFieldsCollectionV2");
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

<a id="countUserUniqueFieldsCollectionV2"></a>
# **countUserUniqueFieldsCollectionV2**
> CountUniqueFieldsCollections200Response countUserUniqueFieldsCollectionV2(userId, field)

UserCollectionController@count

Get user counts for distinct entries of a field in the model

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
    Integer userId = 1; // Integer | user id
    String field = "status"; // String | name of the field to perform a count on
    try {
      CountUniqueFieldsCollections200Response result = apiInstance.countUserUniqueFieldsCollectionV2(userId, field);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#countUserUniqueFieldsCollectionV2");
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

<a id="createCollections"></a>
# **createCollections**
> CreateCategories200Response createCollections(createCollectionsRequest)

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
      CreateCategories200Response result = apiInstance.createCollections(createCollectionsRequest);
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

<a id="createTeamCollections"></a>
# **createTeamCollections**
> CreateCategories200Response createTeamCollections(teamId, createTeamCollectionsRequest)

CollectionController@store

Create a new collection for a team

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
    Integer teamId = 1; // Integer | team id
    CreateTeamCollectionsRequest createTeamCollectionsRequest = new CreateTeamCollectionsRequest(); // CreateTeamCollectionsRequest | Pass user credentials
    try {
      CreateCategories200Response result = apiInstance.createTeamCollections(teamId, createTeamCollectionsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#createTeamCollections");
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
| **createTeamCollectionsRequest** | [**CreateTeamCollectionsRequest**](CreateTeamCollectionsRequest.md)| Pass user credentials | |

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

<a id="createTeamCollectionsV2"></a>
# **createTeamCollectionsV2**
> CreateCategories200Response createTeamCollectionsV2(teamId, createTeamCollectionsRequest)

TeamCollectionController@store

Create a new collection for a team

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
    Integer teamId = 1; // Integer | team id
    CreateTeamCollectionsRequest createTeamCollectionsRequest = new CreateTeamCollectionsRequest(); // CreateTeamCollectionsRequest | Pass user credentials
    try {
      CreateCategories200Response result = apiInstance.createTeamCollectionsV2(teamId, createTeamCollectionsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#createTeamCollectionsV2");
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
| **createTeamCollectionsRequest** | [**CreateTeamCollectionsRequest**](CreateTeamCollectionsRequest.md)| Pass user credentials | |

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

<a id="createUserCollections"></a>
# **createUserCollections**
> CreateCategories200Response createUserCollections(createCollectionsRequest)

UserCollectionController@store

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
      CreateCategories200Response result = apiInstance.createUserCollections(createCollectionsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#createUserCollections");
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

<a id="deleteCollectionsV2"></a>
# **deleteCollectionsV2**
> DeleteAliases200Response deleteCollectionsV2(id)

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
      DeleteAliases200Response result = apiInstance.deleteCollectionsV2(id);
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

<a id="deleteTeamCollections"></a>
# **deleteTeamCollections**
> DeleteAliases200Response deleteTeamCollections(teamId, id)

Delete a collection

Delete a collection owned by a team

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
    Integer teamId = 1; // Integer | team id
    Integer id = 1; // Integer | collection id
    try {
      DeleteAliases200Response result = apiInstance.deleteTeamCollections(teamId, id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#deleteTeamCollections");
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
| **id** | **Integer**| collection id | |

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

<a id="deleteTeamCollectionsV2"></a>
# **deleteTeamCollectionsV2**
> DeleteAliases200Response deleteTeamCollectionsV2(teamId, id)

Delete a collection

Delete a collection owned by a team

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
    Integer teamId = 1; // Integer | team id
    Integer id = 1; // Integer | collection id
    try {
      DeleteAliases200Response result = apiInstance.deleteTeamCollectionsV2(teamId, id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#deleteTeamCollectionsV2");
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
| **id** | **Integer**| collection id | |

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

<a id="deleteUserCollectionsV2"></a>
# **deleteUserCollectionsV2**
> DeleteAliases200Response deleteUserCollectionsV2(userId, id)

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
    Integer userId = 1; // Integer | user id
    Integer id = 1; // Integer | collection id
    try {
      DeleteAliases200Response result = apiInstance.deleteUserCollectionsV2(userId, id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#deleteUserCollectionsV2");
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
| **id** | **Integer**| collection id | |

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

<a id="editTeamCollections"></a>
# **editTeamCollections**
> FetchCollections200Response editTeamCollections(teamId, id, editTeamCollectionsRequest, unarchive)

Edit a collection

Edit a collection owned by a team

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
    Integer teamId = 1; // Integer | team id
    Integer id = 1; // Integer | collection id
    EditTeamCollectionsRequest editTeamCollectionsRequest = new EditTeamCollectionsRequest(); // EditTeamCollectionsRequest | Pass user credentials
    String unarchive = "unarchive_example"; // String | Unarchive a collection
    try {
      FetchCollections200Response result = apiInstance.editTeamCollections(teamId, id, editTeamCollectionsRequest, unarchive);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#editTeamCollections");
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
| **id** | **Integer**| collection id | |
| **editTeamCollectionsRequest** | [**EditTeamCollectionsRequest**](EditTeamCollectionsRequest.md)| Pass user credentials | |
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

<a id="editTeamCollectionsV2"></a>
# **editTeamCollectionsV2**
> FetchCollections200Response editTeamCollectionsV2(teamId, id, editTeamCollectionsRequest)

Edit a collection

Edit a collection owned by a team

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
    Integer teamId = 1; // Integer | team id
    Integer id = 1; // Integer | collection id
    EditTeamCollectionsRequest editTeamCollectionsRequest = new EditTeamCollectionsRequest(); // EditTeamCollectionsRequest | Pass user credentials
    try {
      FetchCollections200Response result = apiInstance.editTeamCollectionsV2(teamId, id, editTeamCollectionsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#editTeamCollectionsV2");
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
| **id** | **Integer**| collection id | |
| **editTeamCollectionsRequest** | [**EditTeamCollectionsRequest**](EditTeamCollectionsRequest.md)| Pass user credentials | |

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

<a id="editUserCollectionsV2"></a>
# **editUserCollectionsV2**
> FetchCollections200Response editUserCollectionsV2(userId, id, editCollectionsV2Request)

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
    Integer userId = 1; // Integer | user id
    Integer id = 1; // Integer | collection id
    EditCollectionsV2Request editCollectionsV2Request = new EditCollectionsV2Request(); // EditCollectionsV2Request | Pass user credentials
    try {
      FetchCollections200Response result = apiInstance.editUserCollectionsV2(userId, id, editCollectionsV2Request);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#editUserCollectionsV2");
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
| **id** | **Integer**| collection id | |
| **editCollectionsV2Request** | [**EditCollectionsV2Request**](EditCollectionsV2Request.md)| Pass user credentials | |

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

<a id="fetchTeamActiveCollectionsV2"></a>
# **fetchTeamActiveCollectionsV2**
> FetchAllCollections200Response fetchTeamActiveCollectionsV2(teamId)

TeamCollectionController@indexActive

Returns a list of a teams collections

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
    Integer teamId = 1; // Integer | team id
    try {
      FetchAllCollections200Response result = apiInstance.fetchTeamActiveCollectionsV2(teamId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#fetchTeamActiveCollectionsV2");
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

<a id="fetchTeamArchivedCollectionsV2"></a>
# **fetchTeamArchivedCollectionsV2**
> FetchAllCollections200Response fetchTeamArchivedCollectionsV2(teamId)

TeamCollectionController@indexArchived

Returns a list of a teams archived collections

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
    Integer teamId = 1; // Integer | team id
    try {
      FetchAllCollections200Response result = apiInstance.fetchTeamArchivedCollectionsV2(teamId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#fetchTeamArchivedCollectionsV2");
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

<a id="fetchTeamCollectionV2"></a>
# **fetchTeamCollectionV2**
> FetchCollections200Response fetchTeamCollectionV2(teamId, id)

TeamCollectionController@show

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
    Integer teamId = 1; // Integer | team id
    Integer id = 1; // Integer | collection id
    try {
      FetchCollections200Response result = apiInstance.fetchTeamCollectionV2(teamId, id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#fetchTeamCollectionV2");
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
| **id** | **Integer**| collection id | |

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

<a id="fetchTeamDraftCollectionsV2"></a>
# **fetchTeamDraftCollectionsV2**
> FetchAllCollections200Response fetchTeamDraftCollectionsV2(teamId)

TeamCollectionController@indexDraft

Returns a list of a teams draft collections

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
    Integer teamId = 1; // Integer | team id
    try {
      FetchAllCollections200Response result = apiInstance.fetchTeamDraftCollectionsV2(teamId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#fetchTeamDraftCollectionsV2");
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

<a id="fetchUserArchivedCollectionsV2"></a>
# **fetchUserArchivedCollectionsV2**
> FetchAllCollections200Response fetchUserArchivedCollectionsV2(userId)

UserCollectionController@indexArchived

Returns a list of a users archived collections

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
    Integer userId = 1; // Integer | user id
    try {
      FetchAllCollections200Response result = apiInstance.fetchUserArchivedCollectionsV2(userId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#fetchUserArchivedCollectionsV2");
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

<a id="fetchUserCollectionV2"></a>
# **fetchUserCollectionV2**
> FetchCollections200Response fetchUserCollectionV2(userId, id)

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
    Integer userId = 1; // Integer | user id
    Integer id = 1; // Integer | collection id
    try {
      FetchCollections200Response result = apiInstance.fetchUserCollectionV2(userId, id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#fetchUserCollectionV2");
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
| **id** | **Integer**| collection id | |

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

<a id="fetchUserCollectionsV2"></a>
# **fetchUserCollectionsV2**
> FetchAllCollections200Response fetchUserCollectionsV2(userId)

UserCollectionController@indexActive

Returns a list of a users collections

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
    Integer userId = 1; // Integer | user id
    try {
      FetchAllCollections200Response result = apiInstance.fetchUserCollectionsV2(userId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#fetchUserCollectionsV2");
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

<a id="fetchUserDraftCollectionsV2"></a>
# **fetchUserDraftCollectionsV2**
> FetchAllCollections200Response fetchUserDraftCollectionsV2(userId)

UserCollectionController@indexDraft

Returns a list of a users draft collections

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
    Integer userId = 1; // Integer | user id
    try {
      FetchAllCollections200Response result = apiInstance.fetchUserDraftCollectionsV2(userId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#fetchUserDraftCollectionsV2");
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

<a id="updateTeamCollections"></a>
# **updateTeamCollections**
> FetchCollections200Response updateTeamCollections(teamId, id, updateTeamCollectionsRequest)

Update a collection

Update a collection owned by a team

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
    Integer teamId = 1; // Integer | team id
    Integer id = 1; // Integer | collection id
    UpdateTeamCollectionsRequest updateTeamCollectionsRequest = new UpdateTeamCollectionsRequest(); // UpdateTeamCollectionsRequest | Pass user credentials
    try {
      FetchCollections200Response result = apiInstance.updateTeamCollections(teamId, id, updateTeamCollectionsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#updateTeamCollections");
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
| **id** | **Integer**| collection id | |
| **updateTeamCollectionsRequest** | [**UpdateTeamCollectionsRequest**](UpdateTeamCollectionsRequest.md)| Pass user credentials | |

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

<a id="updateTeamCollectionsV2"></a>
# **updateTeamCollectionsV2**
> FetchCollections200Response updateTeamCollectionsV2(teamId, id, updateTeamCollectionsRequest)

Update a collection

Update a collection owned by a team

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
    Integer teamId = 1; // Integer | team id
    Integer id = 1; // Integer | collection id
    UpdateTeamCollectionsRequest updateTeamCollectionsRequest = new UpdateTeamCollectionsRequest(); // UpdateTeamCollectionsRequest | Pass user credentials
    try {
      FetchCollections200Response result = apiInstance.updateTeamCollectionsV2(teamId, id, updateTeamCollectionsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#updateTeamCollectionsV2");
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
| **id** | **Integer**| collection id | |
| **updateTeamCollectionsRequest** | [**UpdateTeamCollectionsRequest**](UpdateTeamCollectionsRequest.md)| Pass user credentials | |

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

<a id="updateUserCollectionsV2"></a>
# **updateUserCollectionsV2**
> FetchCollections200Response updateUserCollectionsV2(userId, id, updateCollectionsV2Request)

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
    Integer userId = 1; // Integer | user id
    Integer id = 1; // Integer | collection id
    UpdateCollectionsV2Request updateCollectionsV2Request = new UpdateCollectionsV2Request(); // UpdateCollectionsV2Request | Pass user credentials
    try {
      FetchCollections200Response result = apiInstance.updateUserCollectionsV2(userId, id, updateCollectionsV2Request);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CollectionsApi#updateUserCollectionsV2");
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

