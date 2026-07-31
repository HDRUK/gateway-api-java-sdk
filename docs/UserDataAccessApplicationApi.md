# UserDataAccessApplicationApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**countAllUserDarApplications**](UserDataAccessApplicationApi.md#countAllUserDarApplications) | **GET** /api/v1/users/{userId}/dar/applications/count | UserDataAccessApplicationController@allCounts |
| [**countUserDarApplicationsByField**](UserDataAccessApplicationApi.md#countUserDarApplicationsByField) | **GET** /api/v1/users/{userId}/dar/applications/count/{field} | UserDataAccessApplicationController@count |
| [**createUserDarApplicationAnswers**](UserDataAccessApplicationApi.md#createUserDarApplicationAnswers) | **PUT** /api/v1/users/{userId}/dar/applications/{id}/answers | UserDataAccessApplication@storeAnswers |
| [**fetchUserDarApplicationAnswers**](UserDataAccessApplicationApi.md#fetchUserDarApplicationAnswers) | **GET** /api/v1/users/{userId}/dar/applications/{id}/answers | UserDataAccessApplicationController@showAnswers |
| [**fetchUserDarApplicationDetails**](UserDataAccessApplicationApi.md#fetchUserDarApplicationDetails) | **GET** /api/v1/users/{userId}/dar/applications/{id} | UserDataAccessApplicationController@show |
| [**fetchUserDarApplicationHeader**](UserDataAccessApplicationApi.md#fetchUserDarApplicationHeader) | **GET** /api/v1/users/{userId}/dar/applications/{id}/showHeader | UserDataAccessApplicationController@showHeader |
| [**fetchUserDarApplications**](UserDataAccessApplicationApi.md#fetchUserDarApplications) | **GET** /api/v1/users/{userId}/dar/applications | UserDataAccessApplicationController@index |


<a id="countAllUserDarApplications"></a>
# **countAllUserDarApplications**
> CountUniqueFieldsCollections200Response countAllUserDarApplications(userId)

UserDataAccessApplicationController@allCounts

Get Counts for all status fields in the model

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.UserDataAccessApplicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    UserDataAccessApplicationApi apiInstance = new UserDataAccessApplicationApi(defaultClient);
    Integer userId = 1; // Integer | User id
    try {
      CountUniqueFieldsCollections200Response result = apiInstance.countAllUserDarApplications(userId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserDataAccessApplicationApi#countAllUserDarApplications");
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
| **userId** | **Integer**| User id | |

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

<a id="countUserDarApplicationsByField"></a>
# **countUserDarApplicationsByField**
> CountUniqueFieldsCollections200Response countUserDarApplicationsByField(userId, field)

UserDataAccessApplicationController@count

Get Counts for distinct entries of a field in the model

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.UserDataAccessApplicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    UserDataAccessApplicationApi apiInstance = new UserDataAccessApplicationApi(defaultClient);
    Integer userId = 1; // Integer | User id
    String field = "approval_status"; // String | name of the field to perform a count on
    try {
      CountUniqueFieldsCollections200Response result = apiInstance.countUserDarApplicationsByField(userId, field);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserDataAccessApplicationApi#countUserDarApplicationsByField");
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
| **userId** | **Integer**| User id | |
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

<a id="createUserDarApplicationAnswers"></a>
# **createUserDarApplicationAnswers**
> CreateCategories200Response createUserDarApplicationAnswers(userId, id, createUserDarApplicationAnswersRequest)

UserDataAccessApplication@storeAnswers

Add answers to the user&#39;s DAR application

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.UserDataAccessApplicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    UserDataAccessApplicationApi apiInstance = new UserDataAccessApplicationApi(defaultClient);
    Integer userId = 1; // Integer | User id
    Integer id = 1; // Integer | DAR application id
    CreateUserDarApplicationAnswersRequest createUserDarApplicationAnswersRequest = new CreateUserDarApplicationAnswersRequest(); // CreateUserDarApplicationAnswersRequest | UserDataAccessApplication definition
    try {
      CreateCategories200Response result = apiInstance.createUserDarApplicationAnswers(userId, id, createUserDarApplicationAnswersRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserDataAccessApplicationApi#createUserDarApplicationAnswers");
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
| **userId** | **Integer**| User id | |
| **id** | **Integer**| DAR application id | |
| **createUserDarApplicationAnswersRequest** | [**CreateUserDarApplicationAnswersRequest**](CreateUserDarApplicationAnswersRequest.md)| UserDataAccessApplication definition | |

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

<a id="fetchUserDarApplicationAnswers"></a>
# **fetchUserDarApplicationAnswers**
> FetchTeamDarApplicationAnswers200Response fetchUserDarApplicationAnswers(userId, id)

UserDataAccessApplicationController@showAnswers

Return answers from the user&#39;s DAR application

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.UserDataAccessApplicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    UserDataAccessApplicationApi apiInstance = new UserDataAccessApplicationApi(defaultClient);
    Integer userId = 1; // Integer | User id
    Integer id = 1; // Integer | DAR application id
    try {
      FetchTeamDarApplicationAnswers200Response result = apiInstance.fetchUserDarApplicationAnswers(userId, id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserDataAccessApplicationApi#fetchUserDarApplicationAnswers");
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
| **userId** | **Integer**| User id | |
| **id** | **Integer**| DAR application id | |

### Return type

[**FetchTeamDarApplicationAnswers200Response**](FetchTeamDarApplicationAnswers200Response.md)

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

<a id="fetchUserDarApplicationDetails"></a>
# **fetchUserDarApplicationDetails**
> FetchTeamDarApplication200Response fetchUserDarApplicationDetails(userId, id)

UserDataAccessApplicationController@show

Return a DAR application belonging to the user

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.UserDataAccessApplicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    UserDataAccessApplicationApi apiInstance = new UserDataAccessApplicationApi(defaultClient);
    Integer userId = 1; // Integer | User id
    Integer id = 1; // Integer | DAR application id
    try {
      FetchTeamDarApplication200Response result = apiInstance.fetchUserDarApplicationDetails(userId, id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserDataAccessApplicationApi#fetchUserDarApplicationDetails");
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
| **userId** | **Integer**| User id | |
| **id** | **Integer**| DAR application id | |

### Return type

[**FetchTeamDarApplication200Response**](FetchTeamDarApplication200Response.md)

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

<a id="fetchUserDarApplicationHeader"></a>
# **fetchUserDarApplicationHeader**
> FetchTeamDarApplication200Response fetchUserDarApplicationHeader(userId, id)

UserDataAccessApplicationController@showHeader

Get header information about a specific DAR

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.UserDataAccessApplicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    UserDataAccessApplicationApi apiInstance = new UserDataAccessApplicationApi(defaultClient);
    Integer userId = 1; // Integer | User id
    Integer id = 1; // Integer | DAR application id
    try {
      FetchTeamDarApplication200Response result = apiInstance.fetchUserDarApplicationHeader(userId, id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserDataAccessApplicationApi#fetchUserDarApplicationHeader");
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
| **userId** | **Integer**| User id | |
| **id** | **Integer**| DAR application id | |

### Return type

[**FetchTeamDarApplication200Response**](FetchTeamDarApplication200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="fetchUserDarApplications"></a>
# **fetchUserDarApplications**
> FetchTeamDarApplications200Response fetchUserDarApplications(userId)

UserDataAccessApplicationController@index

List of dar applications belonging to a user

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.UserDataAccessApplicationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    UserDataAccessApplicationApi apiInstance = new UserDataAccessApplicationApi(defaultClient);
    Integer userId = 1; // Integer | User id
    try {
      FetchTeamDarApplications200Response result = apiInstance.fetchUserDarApplications(userId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserDataAccessApplicationApi#fetchUserDarApplications");
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
| **userId** | **Integer**| User id | |

### Return type

[**FetchTeamDarApplications200Response**](FetchTeamDarApplications200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

