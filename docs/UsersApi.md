# UsersApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createUsers**](UsersApi.md#createUsers) | **POST** /api/v1/users | UserController@store |
| [**deleteUsers**](UsersApi.md#deleteUsers) | **DELETE** /api/v1/users/{id} | UserController@destroy |
| [**editUsers**](UsersApi.md#editUsers) | **PATCH** /api/v1/users/{id} | UserController@edit |
| [**fetchAllUsers**](UsersApi.md#fetchAllUsers) | **GET** /api/v1/users | UserController@index |
| [**fetchUsers**](UsersApi.md#fetchUsers) | **GET** /api/v1/users/{id} | UserController@show |
| [**resendSecondaryVerificationEmail**](UsersApi.md#resendSecondaryVerificationEmail) | **POST** /api/v1/users/{id}/resend-secondary-verification | Resend secondary email verification |
| [**updateUsers**](UsersApi.md#updateUsers) | **PUT** /api/v1/users/{id} | UserController@update |
| [**verifySecondaryEmail**](UsersApi.md#verifySecondaryEmail) | **GET** /api/v1/users/verify-secondary-email/{uuid} | Verify user&#39;s secondary email using a UUID |


<a id="createUsers"></a>
# **createUsers**
> CreateCategories200Response createUsers(createUsersRequest)

UserController@store

Create a new user

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.UsersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    UsersApi apiInstance = new UsersApi(defaultClient);
    CreateUsersRequest createUsersRequest = new CreateUsersRequest(); // CreateUsersRequest | Pass user credentials
    try {
      CreateCategories200Response result = apiInstance.createUsers(createUsersRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UsersApi#createUsers");
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
| **createUsersRequest** | [**CreateUsersRequest**](CreateUsersRequest.md)| Pass user credentials | |

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

<a id="deleteUsers"></a>
# **deleteUsers**
> DeleteFederation200Response deleteUsers(id)

UserController@destroy

Delete User based in id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.UsersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    UsersApi apiInstance = new UsersApi(defaultClient);
    Integer id = 1; // Integer | user id
    try {
      DeleteFederation200Response result = apiInstance.deleteUsers(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UsersApi#deleteUsers");
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
| **id** | **Integer**| user id | |

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

<a id="editUsers"></a>
# **editUsers**
> FetchUsers200Response editUsers(id, updateUsersRequest)

UserController@edit

Edit user

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.UsersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    UsersApi apiInstance = new UsersApi(defaultClient);
    Integer id = 1; // Integer | user id
    UpdateUsersRequest updateUsersRequest = new UpdateUsersRequest(); // UpdateUsersRequest | Pass user credentials
    try {
      FetchUsers200Response result = apiInstance.editUsers(id, updateUsersRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UsersApi#editUsers");
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
| **id** | **Integer**| user id | |
| **updateUsersRequest** | [**UpdateUsersRequest**](UpdateUsersRequest.md)| Pass user credentials | |

### Return type

[**FetchUsers200Response**](FetchUsers200Response.md)

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
| **404** | Error response |  -  |
| **500** | Error |  -  |

<a id="fetchAllUsers"></a>
# **fetchAllUsers**
> FetchAllUsers200Response fetchAllUsers(filterNames)

UserController@index

Get All Users

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.UsersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    UsersApi apiInstance = new UsersApi(defaultClient);
    String filterNames = "abc"; // String | Three or more characters to filter users names by
    try {
      FetchAllUsers200Response result = apiInstance.fetchAllUsers(filterNames);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UsersApi#fetchAllUsers");
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
| **filterNames** | **String**| Three or more characters to filter users names by | [optional] |

### Return type

[**FetchAllUsers200Response**](FetchAllUsers200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

<a id="fetchUsers"></a>
# **fetchUsers**
> FetchUsers200Response fetchUsers(id)

UserController@show

Get users by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.UsersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    UsersApi apiInstance = new UsersApi(defaultClient);
    Integer id = 1; // Integer | user id
    try {
      FetchUsers200Response result = apiInstance.fetchUsers(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UsersApi#fetchUsers");
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
| **id** | **Integer**| user id | |

### Return type

[**FetchUsers200Response**](FetchUsers200Response.md)

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

<a id="resendSecondaryVerificationEmail"></a>
# **resendSecondaryVerificationEmail**
> ResendSecondaryVerificationEmail200Response resendSecondaryVerificationEmail(id)

Resend secondary email verification

Resends the verification email for the secondary email address. Old tokens are expired.

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.UsersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    UsersApi apiInstance = new UsersApi(defaultClient);
    Integer id = 123; // Integer | User ID
    try {
      ResendSecondaryVerificationEmail200Response result = apiInstance.resendSecondaryVerificationEmail(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UsersApi#resendSecondaryVerificationEmail");
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
| **id** | **Integer**| User ID | |

### Return type

[**ResendSecondaryVerificationEmail200Response**](ResendSecondaryVerificationEmail200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Verification email resent |  -  |
| **404** | User or secondary email not found |  -  |

<a id="updateUsers"></a>
# **updateUsers**
> FetchUsers200Response updateUsers(id, updateUsersRequest)

UserController@update

Update user

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.UsersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    UsersApi apiInstance = new UsersApi(defaultClient);
    Integer id = 1; // Integer | user id
    UpdateUsersRequest updateUsersRequest = new UpdateUsersRequest(); // UpdateUsersRequest | Pass user credentials
    try {
      FetchUsers200Response result = apiInstance.updateUsers(id, updateUsersRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UsersApi#updateUsers");
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
| **id** | **Integer**| user id | |
| **updateUsersRequest** | [**UpdateUsersRequest**](UpdateUsersRequest.md)| Pass user credentials | |

### Return type

[**FetchUsers200Response**](FetchUsers200Response.md)

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
| **404** | Error response |  -  |
| **500** | Error |  -  |

<a id="verifySecondaryEmail"></a>
# **verifySecondaryEmail**
> VerifySecondaryEmail200Response verifySecondaryEmail(uuid)

Verify user&#39;s secondary email using a UUID

This endpoint verifies the secondary email for a user if the UUID is valid and not expired.

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.UsersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    UsersApi apiInstance = new UsersApi(defaultClient);
    String uuid = "03af1f5e-5cd2-4c41-ae23-56dd2c9efc67"; // String | Verification UUID
    try {
      VerifySecondaryEmail200Response result = apiInstance.verifySecondaryEmail(uuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UsersApi#verifySecondaryEmail");
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
| **uuid** | **String**| Verification UUID | |

### Return type

[**VerifySecondaryEmail200Response**](VerifySecondaryEmail200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Email verified successfully |  -  |
| **400** | Invalid or expired token |  -  |
| **404** | UUID not found |  -  |

