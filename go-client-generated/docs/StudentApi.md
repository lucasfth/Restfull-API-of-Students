# {{classname}}

All URIs are relative to *https://petstore3.swagger.io/api/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AddStudent**](StudentApi.md#AddStudent) | **Post** /student | Add a new student to uni
[**DeleteStudent**](StudentApi.md#DeleteStudent) | **Delete** /student/{studentId} | Deletes a student
[**FindStudentsByStatus**](StudentApi.md#FindStudentsByStatus) | **Get** /student/findByStatus | Finds students by status
[**FindStudentsByTags**](StudentApi.md#FindStudentsByTags) | **Get** /student/findByTags | Finds Students by tags
[**GetStudentById**](StudentApi.md#GetStudentById) | **Get** /student/{studentId} | Find student by ID
[**UpdateStudent**](StudentApi.md#UpdateStudent) | **Put** /student | Update an existing student
[**UpdateStudentWithForm**](StudentApi.md#UpdateStudentWithForm) | **Post** /student/{studentId} | Updates a student in uni with form data
[**UploadFile**](StudentApi.md#UploadFile) | **Post** /student/{studentId}/uploadImage | uploads an image

# **AddStudent**
> Student AddStudent(ctx, body, id, name, category, photoUrls, tags, status)
Add a new student to uni

Add a new student to uni

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **body** | [**Student**](Student.md)| Create a new student in uni | 
  **id** | **int64**|  | 
  **name** | **string**|  | 
  **category** | [**Category**](.md)|  | 
  **photoUrls** | [**[]string**](string.md)|  | 
  **tags** | [**[]Tag**](Tag.md)|  | 
  **status** | **string**|  | 

### Return type

[**Student**](Student.md)

### Authorization

[studentuni_auth](../README.md#studentuni_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/xml, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **DeleteStudent**
> DeleteStudent(ctx, studentId, optional)
Deletes a student

delete a student

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **studentId** | **int64**| Student id to delete | 
 **optional** | ***StudentApiDeleteStudentOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a StudentApiDeleteStudentOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **apiKey** | **optional.String**|  | 

### Return type

 (empty response body)

### Authorization

[studentuni_auth](../README.md#studentuni_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **FindStudentsByStatus**
> []Student FindStudentsByStatus(ctx, optional)
Finds students by status

Multiple status values can be provided with comma separated strings

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***StudentApiFindStudentsByStatusOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a StudentApiFindStudentsByStatusOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **status** | **optional.String**| Status values that need to be considered for filter | [default to active]

### Return type

[**[]Student**](Student.md)

### Authorization

[studentuni_auth](../README.md#studentuni_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **FindStudentsByTags**
> []Student FindStudentsByTags(ctx, optional)
Finds Students by tags

Multiple tags can be provided with comma separated strings. Use tag1, tag2, tag3 for testing.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***StudentApiFindStudentsByTagsOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a StudentApiFindStudentsByTagsOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tags** | [**optional.Interface of []string**](string.md)| Tags to filter by | 

### Return type

[**[]Student**](Student.md)

### Authorization

[studentuni_auth](../README.md#studentuni_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetStudentById**
> Student GetStudentById(ctx, studentId)
Find student by ID

Returns a single student

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **studentId** | **int64**| ID of student to return | 

### Return type

[**Student**](Student.md)

### Authorization

[api_key](../README.md#api_key), [studentuni_auth](../README.md#studentuni_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **UpdateStudent**
> Student UpdateStudent(ctx, body, id, name, category, photoUrls, tags, status)
Update an existing student

Update an existing student by Id

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **body** | [**Student**](Student.md)| Update an existent student in uni | 
  **id** | **int64**|  | 
  **name** | **string**|  | 
  **category** | [**Category**](.md)|  | 
  **photoUrls** | [**[]string**](string.md)|  | 
  **tags** | [**[]Tag**](Tag.md)|  | 
  **status** | **string**|  | 

### Return type

[**Student**](Student.md)

### Authorization

[studentuni_auth](../README.md#studentuni_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/xml, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **UpdateStudentWithForm**
> UpdateStudentWithForm(ctx, studentId, optional)
Updates a student in uni with form data

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **studentId** | **int64**| ID of student that needs to be updated | 
 **optional** | ***StudentApiUpdateStudentWithFormOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a StudentApiUpdateStudentWithFormOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **name** | **optional.String**| Name of student that needs to be updated | 
 **status** | **optional.String**| Status of student that needs to be updated | 

### Return type

 (empty response body)

### Authorization

[studentuni_auth](../README.md#studentuni_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **UploadFile**
> ModelApiResponse UploadFile(ctx, studentId, optional)
uploads an image

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **studentId** | **int64**| ID of student to update | 
 **optional** | ***StudentApiUploadFileOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a StudentApiUploadFileOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **body** | [**optional.Interface of Object**](Object.md)|  | 
 **additionalMetadata** | **optional.**| Additional Metadata | 

### Return type

[**ModelApiResponse**](ApiResponse.md)

### Authorization

[studentuni_auth](../README.md#studentuni_auth)

### HTTP request headers

 - **Content-Type**: application/octet-stream
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

