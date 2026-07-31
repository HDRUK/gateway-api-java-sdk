# AuthenticationApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**authentication**](AuthenticationApi.md#authentication) | **POST** /api/v1/auth | AuthController@checkAuthorization |
| [**login**](AuthenticationApi.md#login) | **POST** /api/v1/auth/login | AuthController@login |
| [**refreshToken**](AuthenticationApi.md#refreshToken) | **POST** /api/v1/refresh_token | AuthController@refreshToken |
| [**register**](AuthenticationApi.md#register) | **POST** /api/v1/auth/register | AuthController@register |


<a id="authentication"></a>
# **authentication**
> Authentication200Response authentication(authenticationRequest)

AuthController@checkAuthorization

Generate Jwt based on email and password

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.AuthenticationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    AuthenticationApi apiInstance = new AuthenticationApi(defaultClient);
    AuthenticationRequest authenticationRequest = new AuthenticationRequest(); // AuthenticationRequest | Pass user credentials
    try {
      Authentication200Response result = apiInstance.authentication(authenticationRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AuthenticationApi#authentication");
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
| **authenticationRequest** | [**AuthenticationRequest**](AuthenticationRequest.md)| Pass user credentials | |

### Return type

[**Authentication200Response**](Authentication200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **401** | Missing Property |  -  |

<a id="login"></a>
# **login**
> Register200Response login(loginRequest)

AuthController@login

Login with email and password

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.AuthenticationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    AuthenticationApi apiInstance = new AuthenticationApi(defaultClient);
    LoginRequest loginRequest = new LoginRequest(); // LoginRequest | Pass user credentials
    try {
      Register200Response result = apiInstance.login(loginRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AuthenticationApi#login");
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
| **loginRequest** | [**LoginRequest**](LoginRequest.md)| Pass user credentials | |

### Return type

[**Register200Response**](Register200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **400** | Validation error |  -  |
| **401** | Invalid credentials |  -  |

<a id="refreshToken"></a>
# **refreshToken**
> Authentication200Response refreshToken()

AuthController@refreshToken

Regenerate jwt token

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.AuthenticationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AuthenticationApi apiInstance = new AuthenticationApi(defaultClient);
    try {
      Authentication200Response result = apiInstance.refreshToken();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AuthenticationApi#refreshToken");
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

[**Authentication200Response**](Authentication200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **401** | Missing Property |  -  |

<a id="register"></a>
# **register**
> Register200Response register(registerRequest)

AuthController@register

Register a new user with email and password

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.AuthenticationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    AuthenticationApi apiInstance = new AuthenticationApi(defaultClient);
    RegisterRequest registerRequest = new RegisterRequest(); // RegisterRequest | Pass user registration data
    try {
      Register200Response result = apiInstance.register(registerRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AuthenticationApi#register");
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
| **registerRequest** | [**RegisterRequest**](RegisterRequest.md)| Pass user registration data | |

### Return type

[**Register200Response**](Register200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **400** | Validation error |  -  |
| **409** | Email already exists |  -  |

