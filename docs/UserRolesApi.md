# UserRolesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createUserHasRoles**](UserRolesApi.md#createUserHasRoles) | **POST** /api/v1/users/{userId}/roles | UserRoleController@store |
| [**deleteUserHasRoles**](UserRolesApi.md#deleteUserHasRoles) | **DELETE** /api/v1/users/{userId}/roles | UserRoleController@destroy |
| [**updateUserHasRoles**](UserRolesApi.md#updateUserHasRoles) | **PATCH** /api/v1/users/{userId}/roles | UserRoleController@edit |


<a id="createUserHasRoles"></a>
# **createUserHasRoles**
> DeleteAliases200Response createUserHasRoles(userId, createUserHasRolesRequest)

UserRoleController@store

Create user has roles

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.UserRolesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    UserRolesApi apiInstance = new UserRolesApi(defaultClient);
    Integer userId = 1; // Integer | user id
    CreateUserHasRolesRequest createUserHasRolesRequest = new CreateUserHasRolesRequest(); // CreateUserHasRolesRequest | Pass user credentials
    try {
      DeleteAliases200Response result = apiInstance.createUserHasRoles(userId, createUserHasRolesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserRolesApi#createUserHasRoles");
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
| **createUserHasRolesRequest** | [**CreateUserHasRolesRequest**](CreateUserHasRolesRequest.md)| Pass user credentials | |

### Return type

[**DeleteAliases200Response**](DeleteAliases200Response.md)

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

<a id="deleteUserHasRoles"></a>
# **deleteUserHasRoles**
> DeleteFederation200Response deleteUserHasRoles(userId)

UserRoleController@destroy

Delete user - roles

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.UserRolesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    UserRolesApi apiInstance = new UserRolesApi(defaultClient);
    Integer userId = 1; // Integer | user id
    try {
      DeleteFederation200Response result = apiInstance.deleteUserHasRoles(userId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserRolesApi#deleteUserHasRoles");
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
| **404** | Error response |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

<a id="updateUserHasRoles"></a>
# **updateUserHasRoles**
> DeleteAliases200Response updateUserHasRoles(userId, updateUserHasRolesRequest)

UserRoleController@edit

Update user has roles

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.UserRolesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    UserRolesApi apiInstance = new UserRolesApi(defaultClient);
    Integer userId = 1; // Integer | user id
    UpdateUserHasRolesRequest updateUserHasRolesRequest = new UpdateUserHasRolesRequest(); // UpdateUserHasRolesRequest | Pass user credentials
    try {
      DeleteAliases200Response result = apiInstance.updateUserHasRoles(userId, updateUserHasRolesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserRolesApi#updateUserHasRoles");
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
| **updateUserHasRolesRequest** | [**UpdateUserHasRolesRequest**](UpdateUserHasRolesRequest.md)| Pass user credentials | |

### Return type

[**DeleteAliases200Response**](DeleteAliases200Response.md)

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

