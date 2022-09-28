# {{classname}}

All URIs are relative to *https://petstore3.swagger.io/api/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateUser**](UserApi.md#CreateUser) | **Post** /user | Create user
[**CreateUsersWithListInput**](UserApi.md#CreateUsersWithListInput) | **Post** /user/createWithList | Creates list of users with given input array
[**DeleteUser**](UserApi.md#DeleteUser) | **Delete** /user/{username} | Delete user
[**GetUserByName**](UserApi.md#GetUserByName) | **Get** /user/{username} | Get user by user name
[**LoginUser**](UserApi.md#LoginUser) | **Get** /user/login | Logs user into the system
[**LogoutUser**](UserApi.md#LogoutUser) | **Get** /user/logout | Logs out current logged in user session
[**UpdateUser**](UserApi.md#UpdateUser) | **Put** /user/{username} | Update user

# **CreateUser**
> User CreateUser(ctx, optional)
Create user

This can only be done by the logged in user.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***UserApiCreateUserOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a UserApiCreateUserOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**optional.Interface of User**](User.md)| Created user object | 
 **id** | **optional.**|  | 
 **username** | **optional.**|  | 
 **firstName** | **optional.**|  | 
 **lastName** | **optional.**|  | 
 **email** | **optional.**|  | 
 **password** | **optional.**|  | 
 **phone** | **optional.**|  | 
 **userStatus** | **optional.**|  | 

### Return type

[**User**](User.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json, application/xml, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CreateUsersWithListInput**
> User CreateUsersWithListInput(ctx, optional)
Creates list of users with given input array

Creates list of users with given input array

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***UserApiCreateUsersWithListInputOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a UserApiCreateUsersWithListInputOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**optional.Interface of []User**](User.md)|  | 

### Return type

[**User**](User.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **DeleteUser**
> DeleteUser(ctx, username)
Delete user

This can only be done by the logged in user.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| The name that needs to be deleted | 

### Return type

 (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetUserByName**
> User GetUserByName(ctx, username)
Get user by user name

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| The name that needs to be fetched. Use user1 for testing.  | 

### Return type

[**User**](User.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **LoginUser**
> string LoginUser(ctx, optional)
Logs user into the system

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***UserApiLoginUserOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a UserApiLoginUserOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **optional.String**| The user name for login | 
 **password** | **optional.String**| The password for login in clear text | 

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **LogoutUser**
> LogoutUser(ctx, )
Logs out current logged in user session

### Required Parameters
This endpoint does not need any parameter.

### Return type

 (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **UpdateUser**
> UpdateUser(ctx, username, optional)
Update user

This can only be done by the logged in user.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| name that need to be deleted | 
 **optional** | ***UserApiUpdateUserOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a UserApiUpdateUserOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **body** | [**optional.Interface of User**](User.md)| Update an existent user in the store | 
 **id** | **optional.**|  | 
 **username** | **optional.**|  | 
 **firstName** | **optional.**|  | 
 **lastName** | **optional.**|  | 
 **email** | **optional.**|  | 
 **password** | **optional.**|  | 
 **phone** | **optional.**|  | 
 **userStatus** | **optional.**|  | 

### Return type

 (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json, application/xml, application/x-www-form-urlencoded
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

