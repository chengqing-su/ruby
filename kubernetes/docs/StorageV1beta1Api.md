# Kubernetes::StorageV1beta1Api

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_storage_class**](StorageV1beta1Api.md#create_storage_class) | **POST** /apis/storage.k8s.io/v1beta1/storageclasses | 
[**create_volume_attachment**](StorageV1beta1Api.md#create_volume_attachment) | **POST** /apis/storage.k8s.io/v1beta1/volumeattachments | 
[**delete_collection_storage_class**](StorageV1beta1Api.md#delete_collection_storage_class) | **DELETE** /apis/storage.k8s.io/v1beta1/storageclasses | 
[**delete_collection_volume_attachment**](StorageV1beta1Api.md#delete_collection_volume_attachment) | **DELETE** /apis/storage.k8s.io/v1beta1/volumeattachments | 
[**delete_storage_class**](StorageV1beta1Api.md#delete_storage_class) | **DELETE** /apis/storage.k8s.io/v1beta1/storageclasses/{name} | 
[**delete_volume_attachment**](StorageV1beta1Api.md#delete_volume_attachment) | **DELETE** /apis/storage.k8s.io/v1beta1/volumeattachments/{name} | 
[**get_api_resources**](StorageV1beta1Api.md#get_api_resources) | **GET** /apis/storage.k8s.io/v1beta1/ | 
[**list_storage_class**](StorageV1beta1Api.md#list_storage_class) | **GET** /apis/storage.k8s.io/v1beta1/storageclasses | 
[**list_volume_attachment**](StorageV1beta1Api.md#list_volume_attachment) | **GET** /apis/storage.k8s.io/v1beta1/volumeattachments | 
[**patch_storage_class**](StorageV1beta1Api.md#patch_storage_class) | **PATCH** /apis/storage.k8s.io/v1beta1/storageclasses/{name} | 
[**patch_volume_attachment**](StorageV1beta1Api.md#patch_volume_attachment) | **PATCH** /apis/storage.k8s.io/v1beta1/volumeattachments/{name} | 
[**read_storage_class**](StorageV1beta1Api.md#read_storage_class) | **GET** /apis/storage.k8s.io/v1beta1/storageclasses/{name} | 
[**read_volume_attachment**](StorageV1beta1Api.md#read_volume_attachment) | **GET** /apis/storage.k8s.io/v1beta1/volumeattachments/{name} | 
[**replace_storage_class**](StorageV1beta1Api.md#replace_storage_class) | **PUT** /apis/storage.k8s.io/v1beta1/storageclasses/{name} | 
[**replace_volume_attachment**](StorageV1beta1Api.md#replace_volume_attachment) | **PUT** /apis/storage.k8s.io/v1beta1/volumeattachments/{name} | 


# **create_storage_class**
> V1beta1StorageClass create_storage_class(body, opts)



create a StorageClass

### Example
```ruby
# load the gem
require 'kubernetes'
# setup authorization
Kubernetes.configure do |config|
  # Configure API key authorization: BearerToken
  config.api_key['authorization'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['authorization'] = 'Bearer'
end

api_instance = Kubernetes::StorageV1beta1Api.new

body = Kubernetes::V1beta1StorageClass.new # V1beta1StorageClass | 

opts = { 
  include_uninitialized: true, # BOOLEAN | If true, partially initialized resources are included in the response.
  pretty: "pretty_example", # String | If 'true', then the output is pretty printed.
  dry_run: "dry_run_example" # String | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
}

begin
  result = api_instance.create_storage_class(body, opts)
  p result
rescue Kubernetes::ApiError => e
  puts "Exception when calling StorageV1beta1Api->create_storage_class: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**V1beta1StorageClass**](V1beta1StorageClass.md)|  | 
 **include_uninitialized** | **BOOLEAN**| If true, partially initialized resources are included in the response. | [optional] 
 **pretty** | **String**| If &#39;true&#39;, then the output is pretty printed. | [optional] 
 **dry_run** | **String**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] 

### Return type

[**V1beta1StorageClass**](V1beta1StorageClass.md)

### Authorization

[BearerToken](../README.md#BearerToken)

### HTTP request headers

 - **Content-Type**: */*
 - **Accept**: application/json, application/yaml, application/vnd.kubernetes.protobuf



# **create_volume_attachment**
> V1beta1VolumeAttachment create_volume_attachment(body, opts)



create a VolumeAttachment

### Example
```ruby
# load the gem
require 'kubernetes'
# setup authorization
Kubernetes.configure do |config|
  # Configure API key authorization: BearerToken
  config.api_key['authorization'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['authorization'] = 'Bearer'
end

api_instance = Kubernetes::StorageV1beta1Api.new

body = Kubernetes::V1beta1VolumeAttachment.new # V1beta1VolumeAttachment | 

opts = { 
  include_uninitialized: true, # BOOLEAN | If true, partially initialized resources are included in the response.
  pretty: "pretty_example", # String | If 'true', then the output is pretty printed.
  dry_run: "dry_run_example" # String | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
}

begin
  result = api_instance.create_volume_attachment(body, opts)
  p result
rescue Kubernetes::ApiError => e
  puts "Exception when calling StorageV1beta1Api->create_volume_attachment: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**V1beta1VolumeAttachment**](V1beta1VolumeAttachment.md)|  | 
 **include_uninitialized** | **BOOLEAN**| If true, partially initialized resources are included in the response. | [optional] 
 **pretty** | **String**| If &#39;true&#39;, then the output is pretty printed. | [optional] 
 **dry_run** | **String**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] 

### Return type

[**V1beta1VolumeAttachment**](V1beta1VolumeAttachment.md)

### Authorization

[BearerToken](../README.md#BearerToken)

### HTTP request headers

 - **Content-Type**: */*
 - **Accept**: application/json, application/yaml, application/vnd.kubernetes.protobuf



# **delete_collection_storage_class**
> V1Status delete_collection_storage_class(opts)



delete collection of StorageClass

### Example
```ruby
# load the gem
require 'kubernetes'
# setup authorization
Kubernetes.configure do |config|
  # Configure API key authorization: BearerToken
  config.api_key['authorization'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['authorization'] = 'Bearer'
end

api_instance = Kubernetes::StorageV1beta1Api.new

opts = { 
  include_uninitialized: true, # BOOLEAN | If true, partially initialized resources are included in the response.
  pretty: "pretty_example", # String | If 'true', then the output is pretty printed.
  continue: "continue_example", # String | The continue option should be set when retrieving more results from the server. Since this value is server defined, clients may only use the continue value from a previous query result with identical query parameters (except for the value of continue) and the server may reject a continue value it does not recognize. If the specified continue value is no longer valid whether due to expiration (generally five to fifteen minutes) or a configuration change on the server, the server will respond with a 410 ResourceExpired error together with a continue token. If the client needs a consistent list, it must restart their list without the continue field. Otherwise, the client may send another list request with the token received with the 410 error, the server will respond with a list starting from the next key, but from the latest snapshot, which is inconsistent from the previous list results - objects that are created, modified, or deleted after the first list request will be included in the response, as long as their keys are after the \"next key\".  This field is not supported when watch is true. Clients may start a watch from the last resourceVersion value returned by the server and not miss any modifications.
  field_selector: "field_selector_example", # String | A selector to restrict the list of returned objects by their fields. Defaults to everything.
  label_selector: "label_selector_example", # String | A selector to restrict the list of returned objects by their labels. Defaults to everything.
  limit: 56, # Integer | limit is a maximum number of responses to return for a list call. If more items exist, the server will set the `continue` field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true.  The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned.
  resource_version: "resource_version_example", # String | When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. When specified for list: - if unset, then the result is returned from remote storage based on quorum-read flag; - if it's 0, then we simply return what we currently have in cache, no guarantee; - if set to non zero, then the result is at least as fresh as given rv.
  timeout_seconds: 56, # Integer | Timeout for the list/watch call. This limits the duration of the call, regardless of any activity or inactivity.
  watch: true # BOOLEAN | Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion.
}

begin
  result = api_instance.delete_collection_storage_class(opts)
  p result
rescue Kubernetes::ApiError => e
  puts "Exception when calling StorageV1beta1Api->delete_collection_storage_class: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **include_uninitialized** | **BOOLEAN**| If true, partially initialized resources are included in the response. | [optional] 
 **pretty** | **String**| If &#39;true&#39;, then the output is pretty printed. | [optional] 
 **continue** | **String**| The continue option should be set when retrieving more results from the server. Since this value is server defined, clients may only use the continue value from a previous query result with identical query parameters (except for the value of continue) and the server may reject a continue value it does not recognize. If the specified continue value is no longer valid whether due to expiration (generally five to fifteen minutes) or a configuration change on the server, the server will respond with a 410 ResourceExpired error together with a continue token. If the client needs a consistent list, it must restart their list without the continue field. Otherwise, the client may send another list request with the token received with the 410 error, the server will respond with a list starting from the next key, but from the latest snapshot, which is inconsistent from the previous list results - objects that are created, modified, or deleted after the first list request will be included in the response, as long as their keys are after the \&quot;next key\&quot;.  This field is not supported when watch is true. Clients may start a watch from the last resourceVersion value returned by the server and not miss any modifications. | [optional] 
 **field_selector** | **String**| A selector to restrict the list of returned objects by their fields. Defaults to everything. | [optional] 
 **label_selector** | **String**| A selector to restrict the list of returned objects by their labels. Defaults to everything. | [optional] 
 **limit** | **Integer**| limit is a maximum number of responses to return for a list call. If more items exist, the server will set the &#x60;continue&#x60; field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true.  The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned. | [optional] 
 **resource_version** | **String**| When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. When specified for list: - if unset, then the result is returned from remote storage based on quorum-read flag; - if it&#39;s 0, then we simply return what we currently have in cache, no guarantee; - if set to non zero, then the result is at least as fresh as given rv. | [optional] 
 **timeout_seconds** | **Integer**| Timeout for the list/watch call. This limits the duration of the call, regardless of any activity or inactivity. | [optional] 
 **watch** | **BOOLEAN**| Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion. | [optional] 

### Return type

[**V1Status**](V1Status.md)

### Authorization

[BearerToken](../README.md#BearerToken)

### HTTP request headers

 - **Content-Type**: */*
 - **Accept**: application/json, application/yaml, application/vnd.kubernetes.protobuf



# **delete_collection_volume_attachment**
> V1Status delete_collection_volume_attachment(opts)



delete collection of VolumeAttachment

### Example
```ruby
# load the gem
require 'kubernetes'
# setup authorization
Kubernetes.configure do |config|
  # Configure API key authorization: BearerToken
  config.api_key['authorization'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['authorization'] = 'Bearer'
end

api_instance = Kubernetes::StorageV1beta1Api.new

opts = { 
  include_uninitialized: true, # BOOLEAN | If true, partially initialized resources are included in the response.
  pretty: "pretty_example", # String | If 'true', then the output is pretty printed.
  continue: "continue_example", # String | The continue option should be set when retrieving more results from the server. Since this value is server defined, clients may only use the continue value from a previous query result with identical query parameters (except for the value of continue) and the server may reject a continue value it does not recognize. If the specified continue value is no longer valid whether due to expiration (generally five to fifteen minutes) or a configuration change on the server, the server will respond with a 410 ResourceExpired error together with a continue token. If the client needs a consistent list, it must restart their list without the continue field. Otherwise, the client may send another list request with the token received with the 410 error, the server will respond with a list starting from the next key, but from the latest snapshot, which is inconsistent from the previous list results - objects that are created, modified, or deleted after the first list request will be included in the response, as long as their keys are after the \"next key\".  This field is not supported when watch is true. Clients may start a watch from the last resourceVersion value returned by the server and not miss any modifications.
  field_selector: "field_selector_example", # String | A selector to restrict the list of returned objects by their fields. Defaults to everything.
  label_selector: "label_selector_example", # String | A selector to restrict the list of returned objects by their labels. Defaults to everything.
  limit: 56, # Integer | limit is a maximum number of responses to return for a list call. If more items exist, the server will set the `continue` field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true.  The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned.
  resource_version: "resource_version_example", # String | When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. When specified for list: - if unset, then the result is returned from remote storage based on quorum-read flag; - if it's 0, then we simply return what we currently have in cache, no guarantee; - if set to non zero, then the result is at least as fresh as given rv.
  timeout_seconds: 56, # Integer | Timeout for the list/watch call. This limits the duration of the call, regardless of any activity or inactivity.
  watch: true # BOOLEAN | Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion.
}

begin
  result = api_instance.delete_collection_volume_attachment(opts)
  p result
rescue Kubernetes::ApiError => e
  puts "Exception when calling StorageV1beta1Api->delete_collection_volume_attachment: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **include_uninitialized** | **BOOLEAN**| If true, partially initialized resources are included in the response. | [optional] 
 **pretty** | **String**| If &#39;true&#39;, then the output is pretty printed. | [optional] 
 **continue** | **String**| The continue option should be set when retrieving more results from the server. Since this value is server defined, clients may only use the continue value from a previous query result with identical query parameters (except for the value of continue) and the server may reject a continue value it does not recognize. If the specified continue value is no longer valid whether due to expiration (generally five to fifteen minutes) or a configuration change on the server, the server will respond with a 410 ResourceExpired error together with a continue token. If the client needs a consistent list, it must restart their list without the continue field. Otherwise, the client may send another list request with the token received with the 410 error, the server will respond with a list starting from the next key, but from the latest snapshot, which is inconsistent from the previous list results - objects that are created, modified, or deleted after the first list request will be included in the response, as long as their keys are after the \&quot;next key\&quot;.  This field is not supported when watch is true. Clients may start a watch from the last resourceVersion value returned by the server and not miss any modifications. | [optional] 
 **field_selector** | **String**| A selector to restrict the list of returned objects by their fields. Defaults to everything. | [optional] 
 **label_selector** | **String**| A selector to restrict the list of returned objects by their labels. Defaults to everything. | [optional] 
 **limit** | **Integer**| limit is a maximum number of responses to return for a list call. If more items exist, the server will set the &#x60;continue&#x60; field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true.  The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned. | [optional] 
 **resource_version** | **String**| When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. When specified for list: - if unset, then the result is returned from remote storage based on quorum-read flag; - if it&#39;s 0, then we simply return what we currently have in cache, no guarantee; - if set to non zero, then the result is at least as fresh as given rv. | [optional] 
 **timeout_seconds** | **Integer**| Timeout for the list/watch call. This limits the duration of the call, regardless of any activity or inactivity. | [optional] 
 **watch** | **BOOLEAN**| Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion. | [optional] 

### Return type

[**V1Status**](V1Status.md)

### Authorization

[BearerToken](../README.md#BearerToken)

### HTTP request headers

 - **Content-Type**: */*
 - **Accept**: application/json, application/yaml, application/vnd.kubernetes.protobuf



# **delete_storage_class**
> V1Status delete_storage_class(name, , opts)



delete a StorageClass

### Example
```ruby
# load the gem
require 'kubernetes'
# setup authorization
Kubernetes.configure do |config|
  # Configure API key authorization: BearerToken
  config.api_key['authorization'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['authorization'] = 'Bearer'
end

api_instance = Kubernetes::StorageV1beta1Api.new

name = "name_example" # String | name of the StorageClass

opts = { 
  pretty: "pretty_example", # String | If 'true', then the output is pretty printed.
  body: Kubernetes::V1DeleteOptions.new, # V1DeleteOptions | 
  dry_run: "dry_run_example", # String | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
  grace_period_seconds: 56, # Integer | The duration in seconds before the object should be deleted. Value must be non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately.
  orphan_dependents: true, # BOOLEAN | Deprecated: please use the PropagationPolicy, this field will be deprecated in 1.7. Should the dependent objects be orphaned. If true/false, the \"orphan\" finalizer will be added to/removed from the object's finalizers list. Either this field or PropagationPolicy may be set, but not both.
  propagation_policy: "propagation_policy_example" # String | Whether and how garbage collection will be performed. Either this field or OrphanDependents may be set, but not both. The default policy is decided by the existing finalizer set in the metadata.finalizers and the resource-specific default policy. Acceptable values are: 'Orphan' - orphan the dependents; 'Background' - allow the garbage collector to delete the dependents in the background; 'Foreground' - a cascading policy that deletes all dependents in the foreground.
}

begin
  result = api_instance.delete_storage_class(name, , opts)
  p result
rescue Kubernetes::ApiError => e
  puts "Exception when calling StorageV1beta1Api->delete_storage_class: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **String**| name of the StorageClass | 
 **pretty** | **String**| If &#39;true&#39;, then the output is pretty printed. | [optional] 
 **body** | [**V1DeleteOptions**](V1DeleteOptions.md)|  | [optional] 
 **dry_run** | **String**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] 
 **grace_period_seconds** | **Integer**| The duration in seconds before the object should be deleted. Value must be non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately. | [optional] 
 **orphan_dependents** | **BOOLEAN**| Deprecated: please use the PropagationPolicy, this field will be deprecated in 1.7. Should the dependent objects be orphaned. If true/false, the \&quot;orphan\&quot; finalizer will be added to/removed from the object&#39;s finalizers list. Either this field or PropagationPolicy may be set, but not both. | [optional] 
 **propagation_policy** | **String**| Whether and how garbage collection will be performed. Either this field or OrphanDependents may be set, but not both. The default policy is decided by the existing finalizer set in the metadata.finalizers and the resource-specific default policy. Acceptable values are: &#39;Orphan&#39; - orphan the dependents; &#39;Background&#39; - allow the garbage collector to delete the dependents in the background; &#39;Foreground&#39; - a cascading policy that deletes all dependents in the foreground. | [optional] 

### Return type

[**V1Status**](V1Status.md)

### Authorization

[BearerToken](../README.md#BearerToken)

### HTTP request headers

 - **Content-Type**: */*
 - **Accept**: application/json, application/yaml, application/vnd.kubernetes.protobuf



# **delete_volume_attachment**
> V1Status delete_volume_attachment(name, , opts)



delete a VolumeAttachment

### Example
```ruby
# load the gem
require 'kubernetes'
# setup authorization
Kubernetes.configure do |config|
  # Configure API key authorization: BearerToken
  config.api_key['authorization'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['authorization'] = 'Bearer'
end

api_instance = Kubernetes::StorageV1beta1Api.new

name = "name_example" # String | name of the VolumeAttachment

opts = { 
  pretty: "pretty_example", # String | If 'true', then the output is pretty printed.
  body: Kubernetes::V1DeleteOptions.new, # V1DeleteOptions | 
  dry_run: "dry_run_example", # String | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
  grace_period_seconds: 56, # Integer | The duration in seconds before the object should be deleted. Value must be non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately.
  orphan_dependents: true, # BOOLEAN | Deprecated: please use the PropagationPolicy, this field will be deprecated in 1.7. Should the dependent objects be orphaned. If true/false, the \"orphan\" finalizer will be added to/removed from the object's finalizers list. Either this field or PropagationPolicy may be set, but not both.
  propagation_policy: "propagation_policy_example" # String | Whether and how garbage collection will be performed. Either this field or OrphanDependents may be set, but not both. The default policy is decided by the existing finalizer set in the metadata.finalizers and the resource-specific default policy. Acceptable values are: 'Orphan' - orphan the dependents; 'Background' - allow the garbage collector to delete the dependents in the background; 'Foreground' - a cascading policy that deletes all dependents in the foreground.
}

begin
  result = api_instance.delete_volume_attachment(name, , opts)
  p result
rescue Kubernetes::ApiError => e
  puts "Exception when calling StorageV1beta1Api->delete_volume_attachment: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **String**| name of the VolumeAttachment | 
 **pretty** | **String**| If &#39;true&#39;, then the output is pretty printed. | [optional] 
 **body** | [**V1DeleteOptions**](V1DeleteOptions.md)|  | [optional] 
 **dry_run** | **String**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] 
 **grace_period_seconds** | **Integer**| The duration in seconds before the object should be deleted. Value must be non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately. | [optional] 
 **orphan_dependents** | **BOOLEAN**| Deprecated: please use the PropagationPolicy, this field will be deprecated in 1.7. Should the dependent objects be orphaned. If true/false, the \&quot;orphan\&quot; finalizer will be added to/removed from the object&#39;s finalizers list. Either this field or PropagationPolicy may be set, but not both. | [optional] 
 **propagation_policy** | **String**| Whether and how garbage collection will be performed. Either this field or OrphanDependents may be set, but not both. The default policy is decided by the existing finalizer set in the metadata.finalizers and the resource-specific default policy. Acceptable values are: &#39;Orphan&#39; - orphan the dependents; &#39;Background&#39; - allow the garbage collector to delete the dependents in the background; &#39;Foreground&#39; - a cascading policy that deletes all dependents in the foreground. | [optional] 

### Return type

[**V1Status**](V1Status.md)

### Authorization

[BearerToken](../README.md#BearerToken)

### HTTP request headers

 - **Content-Type**: */*
 - **Accept**: application/json, application/yaml, application/vnd.kubernetes.protobuf



# **get_api_resources**
> V1APIResourceList get_api_resources



get available resources

### Example
```ruby
# load the gem
require 'kubernetes'
# setup authorization
Kubernetes.configure do |config|
  # Configure API key authorization: BearerToken
  config.api_key['authorization'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['authorization'] = 'Bearer'
end

api_instance = Kubernetes::StorageV1beta1Api.new

begin
  result = api_instance.get_api_resources
  p result
rescue Kubernetes::ApiError => e
  puts "Exception when calling StorageV1beta1Api->get_api_resources: #{e}"
end
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**V1APIResourceList**](V1APIResourceList.md)

### Authorization

[BearerToken](../README.md#BearerToken)

### HTTP request headers

 - **Content-Type**: application/json, application/yaml, application/vnd.kubernetes.protobuf
 - **Accept**: application/json, application/yaml, application/vnd.kubernetes.protobuf



# **list_storage_class**
> V1beta1StorageClassList list_storage_class(opts)



list or watch objects of kind StorageClass

### Example
```ruby
# load the gem
require 'kubernetes'
# setup authorization
Kubernetes.configure do |config|
  # Configure API key authorization: BearerToken
  config.api_key['authorization'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['authorization'] = 'Bearer'
end

api_instance = Kubernetes::StorageV1beta1Api.new

opts = { 
  include_uninitialized: true, # BOOLEAN | If true, partially initialized resources are included in the response.
  pretty: "pretty_example", # String | If 'true', then the output is pretty printed.
  continue: "continue_example", # String | The continue option should be set when retrieving more results from the server. Since this value is server defined, clients may only use the continue value from a previous query result with identical query parameters (except for the value of continue) and the server may reject a continue value it does not recognize. If the specified continue value is no longer valid whether due to expiration (generally five to fifteen minutes) or a configuration change on the server, the server will respond with a 410 ResourceExpired error together with a continue token. If the client needs a consistent list, it must restart their list without the continue field. Otherwise, the client may send another list request with the token received with the 410 error, the server will respond with a list starting from the next key, but from the latest snapshot, which is inconsistent from the previous list results - objects that are created, modified, or deleted after the first list request will be included in the response, as long as their keys are after the \"next key\".  This field is not supported when watch is true. Clients may start a watch from the last resourceVersion value returned by the server and not miss any modifications.
  field_selector: "field_selector_example", # String | A selector to restrict the list of returned objects by their fields. Defaults to everything.
  label_selector: "label_selector_example", # String | A selector to restrict the list of returned objects by their labels. Defaults to everything.
  limit: 56, # Integer | limit is a maximum number of responses to return for a list call. If more items exist, the server will set the `continue` field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true.  The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned.
  resource_version: "resource_version_example", # String | When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. When specified for list: - if unset, then the result is returned from remote storage based on quorum-read flag; - if it's 0, then we simply return what we currently have in cache, no guarantee; - if set to non zero, then the result is at least as fresh as given rv.
  timeout_seconds: 56, # Integer | Timeout for the list/watch call. This limits the duration of the call, regardless of any activity or inactivity.
  watch: true # BOOLEAN | Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion.
}

begin
  result = api_instance.list_storage_class(opts)
  p result
rescue Kubernetes::ApiError => e
  puts "Exception when calling StorageV1beta1Api->list_storage_class: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **include_uninitialized** | **BOOLEAN**| If true, partially initialized resources are included in the response. | [optional] 
 **pretty** | **String**| If &#39;true&#39;, then the output is pretty printed. | [optional] 
 **continue** | **String**| The continue option should be set when retrieving more results from the server. Since this value is server defined, clients may only use the continue value from a previous query result with identical query parameters (except for the value of continue) and the server may reject a continue value it does not recognize. If the specified continue value is no longer valid whether due to expiration (generally five to fifteen minutes) or a configuration change on the server, the server will respond with a 410 ResourceExpired error together with a continue token. If the client needs a consistent list, it must restart their list without the continue field. Otherwise, the client may send another list request with the token received with the 410 error, the server will respond with a list starting from the next key, but from the latest snapshot, which is inconsistent from the previous list results - objects that are created, modified, or deleted after the first list request will be included in the response, as long as their keys are after the \&quot;next key\&quot;.  This field is not supported when watch is true. Clients may start a watch from the last resourceVersion value returned by the server and not miss any modifications. | [optional] 
 **field_selector** | **String**| A selector to restrict the list of returned objects by their fields. Defaults to everything. | [optional] 
 **label_selector** | **String**| A selector to restrict the list of returned objects by their labels. Defaults to everything. | [optional] 
 **limit** | **Integer**| limit is a maximum number of responses to return for a list call. If more items exist, the server will set the &#x60;continue&#x60; field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true.  The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned. | [optional] 
 **resource_version** | **String**| When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. When specified for list: - if unset, then the result is returned from remote storage based on quorum-read flag; - if it&#39;s 0, then we simply return what we currently have in cache, no guarantee; - if set to non zero, then the result is at least as fresh as given rv. | [optional] 
 **timeout_seconds** | **Integer**| Timeout for the list/watch call. This limits the duration of the call, regardless of any activity or inactivity. | [optional] 
 **watch** | **BOOLEAN**| Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion. | [optional] 

### Return type

[**V1beta1StorageClassList**](V1beta1StorageClassList.md)

### Authorization

[BearerToken](../README.md#BearerToken)

### HTTP request headers

 - **Content-Type**: */*
 - **Accept**: application/json, application/yaml, application/vnd.kubernetes.protobuf, application/json;stream=watch, application/vnd.kubernetes.protobuf;stream=watch



# **list_volume_attachment**
> V1beta1VolumeAttachmentList list_volume_attachment(opts)



list or watch objects of kind VolumeAttachment

### Example
```ruby
# load the gem
require 'kubernetes'
# setup authorization
Kubernetes.configure do |config|
  # Configure API key authorization: BearerToken
  config.api_key['authorization'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['authorization'] = 'Bearer'
end

api_instance = Kubernetes::StorageV1beta1Api.new

opts = { 
  include_uninitialized: true, # BOOLEAN | If true, partially initialized resources are included in the response.
  pretty: "pretty_example", # String | If 'true', then the output is pretty printed.
  continue: "continue_example", # String | The continue option should be set when retrieving more results from the server. Since this value is server defined, clients may only use the continue value from a previous query result with identical query parameters (except for the value of continue) and the server may reject a continue value it does not recognize. If the specified continue value is no longer valid whether due to expiration (generally five to fifteen minutes) or a configuration change on the server, the server will respond with a 410 ResourceExpired error together with a continue token. If the client needs a consistent list, it must restart their list without the continue field. Otherwise, the client may send another list request with the token received with the 410 error, the server will respond with a list starting from the next key, but from the latest snapshot, which is inconsistent from the previous list results - objects that are created, modified, or deleted after the first list request will be included in the response, as long as their keys are after the \"next key\".  This field is not supported when watch is true. Clients may start a watch from the last resourceVersion value returned by the server and not miss any modifications.
  field_selector: "field_selector_example", # String | A selector to restrict the list of returned objects by their fields. Defaults to everything.
  label_selector: "label_selector_example", # String | A selector to restrict the list of returned objects by their labels. Defaults to everything.
  limit: 56, # Integer | limit is a maximum number of responses to return for a list call. If more items exist, the server will set the `continue` field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true.  The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned.
  resource_version: "resource_version_example", # String | When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. When specified for list: - if unset, then the result is returned from remote storage based on quorum-read flag; - if it's 0, then we simply return what we currently have in cache, no guarantee; - if set to non zero, then the result is at least as fresh as given rv.
  timeout_seconds: 56, # Integer | Timeout for the list/watch call. This limits the duration of the call, regardless of any activity or inactivity.
  watch: true # BOOLEAN | Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion.
}

begin
  result = api_instance.list_volume_attachment(opts)
  p result
rescue Kubernetes::ApiError => e
  puts "Exception when calling StorageV1beta1Api->list_volume_attachment: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **include_uninitialized** | **BOOLEAN**| If true, partially initialized resources are included in the response. | [optional] 
 **pretty** | **String**| If &#39;true&#39;, then the output is pretty printed. | [optional] 
 **continue** | **String**| The continue option should be set when retrieving more results from the server. Since this value is server defined, clients may only use the continue value from a previous query result with identical query parameters (except for the value of continue) and the server may reject a continue value it does not recognize. If the specified continue value is no longer valid whether due to expiration (generally five to fifteen minutes) or a configuration change on the server, the server will respond with a 410 ResourceExpired error together with a continue token. If the client needs a consistent list, it must restart their list without the continue field. Otherwise, the client may send another list request with the token received with the 410 error, the server will respond with a list starting from the next key, but from the latest snapshot, which is inconsistent from the previous list results - objects that are created, modified, or deleted after the first list request will be included in the response, as long as their keys are after the \&quot;next key\&quot;.  This field is not supported when watch is true. Clients may start a watch from the last resourceVersion value returned by the server and not miss any modifications. | [optional] 
 **field_selector** | **String**| A selector to restrict the list of returned objects by their fields. Defaults to everything. | [optional] 
 **label_selector** | **String**| A selector to restrict the list of returned objects by their labels. Defaults to everything. | [optional] 
 **limit** | **Integer**| limit is a maximum number of responses to return for a list call. If more items exist, the server will set the &#x60;continue&#x60; field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true.  The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned. | [optional] 
 **resource_version** | **String**| When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. When specified for list: - if unset, then the result is returned from remote storage based on quorum-read flag; - if it&#39;s 0, then we simply return what we currently have in cache, no guarantee; - if set to non zero, then the result is at least as fresh as given rv. | [optional] 
 **timeout_seconds** | **Integer**| Timeout for the list/watch call. This limits the duration of the call, regardless of any activity or inactivity. | [optional] 
 **watch** | **BOOLEAN**| Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion. | [optional] 

### Return type

[**V1beta1VolumeAttachmentList**](V1beta1VolumeAttachmentList.md)

### Authorization

[BearerToken](../README.md#BearerToken)

### HTTP request headers

 - **Content-Type**: */*
 - **Accept**: application/json, application/yaml, application/vnd.kubernetes.protobuf, application/json;stream=watch, application/vnd.kubernetes.protobuf;stream=watch



# **patch_storage_class**
> V1beta1StorageClass patch_storage_class(name, body, opts)



partially update the specified StorageClass

### Example
```ruby
# load the gem
require 'kubernetes'
# setup authorization
Kubernetes.configure do |config|
  # Configure API key authorization: BearerToken
  config.api_key['authorization'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['authorization'] = 'Bearer'
end

api_instance = Kubernetes::StorageV1beta1Api.new

name = "name_example" # String | name of the StorageClass

body = nil # Object | 

opts = { 
  pretty: "pretty_example", # String | If 'true', then the output is pretty printed.
  dry_run: "dry_run_example" # String | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
}

begin
  result = api_instance.patch_storage_class(name, body, opts)
  p result
rescue Kubernetes::ApiError => e
  puts "Exception when calling StorageV1beta1Api->patch_storage_class: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **String**| name of the StorageClass | 
 **body** | **Object**|  | 
 **pretty** | **String**| If &#39;true&#39;, then the output is pretty printed. | [optional] 
 **dry_run** | **String**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] 

### Return type

[**V1beta1StorageClass**](V1beta1StorageClass.md)

### Authorization

[BearerToken](../README.md#BearerToken)

### HTTP request headers

 - **Content-Type**: application/json-patch+json, application/merge-patch+json, application/strategic-merge-patch+json
 - **Accept**: application/json, application/yaml, application/vnd.kubernetes.protobuf



# **patch_volume_attachment**
> V1beta1VolumeAttachment patch_volume_attachment(name, body, opts)



partially update the specified VolumeAttachment

### Example
```ruby
# load the gem
require 'kubernetes'
# setup authorization
Kubernetes.configure do |config|
  # Configure API key authorization: BearerToken
  config.api_key['authorization'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['authorization'] = 'Bearer'
end

api_instance = Kubernetes::StorageV1beta1Api.new

name = "name_example" # String | name of the VolumeAttachment

body = nil # Object | 

opts = { 
  pretty: "pretty_example", # String | If 'true', then the output is pretty printed.
  dry_run: "dry_run_example" # String | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
}

begin
  result = api_instance.patch_volume_attachment(name, body, opts)
  p result
rescue Kubernetes::ApiError => e
  puts "Exception when calling StorageV1beta1Api->patch_volume_attachment: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **String**| name of the VolumeAttachment | 
 **body** | **Object**|  | 
 **pretty** | **String**| If &#39;true&#39;, then the output is pretty printed. | [optional] 
 **dry_run** | **String**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] 

### Return type

[**V1beta1VolumeAttachment**](V1beta1VolumeAttachment.md)

### Authorization

[BearerToken](../README.md#BearerToken)

### HTTP request headers

 - **Content-Type**: application/json-patch+json, application/merge-patch+json, application/strategic-merge-patch+json
 - **Accept**: application/json, application/yaml, application/vnd.kubernetes.protobuf



# **read_storage_class**
> V1beta1StorageClass read_storage_class(name, , opts)



read the specified StorageClass

### Example
```ruby
# load the gem
require 'kubernetes'
# setup authorization
Kubernetes.configure do |config|
  # Configure API key authorization: BearerToken
  config.api_key['authorization'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['authorization'] = 'Bearer'
end

api_instance = Kubernetes::StorageV1beta1Api.new

name = "name_example" # String | name of the StorageClass

opts = { 
  pretty: "pretty_example", # String | If 'true', then the output is pretty printed.
  exact: true, # BOOLEAN | Should the export be exact.  Exact export maintains cluster-specific fields like 'Namespace'.
  export: true # BOOLEAN | Should this value be exported.  Export strips fields that a user can not specify.
}

begin
  result = api_instance.read_storage_class(name, , opts)
  p result
rescue Kubernetes::ApiError => e
  puts "Exception when calling StorageV1beta1Api->read_storage_class: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **String**| name of the StorageClass | 
 **pretty** | **String**| If &#39;true&#39;, then the output is pretty printed. | [optional] 
 **exact** | **BOOLEAN**| Should the export be exact.  Exact export maintains cluster-specific fields like &#39;Namespace&#39;. | [optional] 
 **export** | **BOOLEAN**| Should this value be exported.  Export strips fields that a user can not specify. | [optional] 

### Return type

[**V1beta1StorageClass**](V1beta1StorageClass.md)

### Authorization

[BearerToken](../README.md#BearerToken)

### HTTP request headers

 - **Content-Type**: */*
 - **Accept**: application/json, application/yaml, application/vnd.kubernetes.protobuf



# **read_volume_attachment**
> V1beta1VolumeAttachment read_volume_attachment(name, , opts)



read the specified VolumeAttachment

### Example
```ruby
# load the gem
require 'kubernetes'
# setup authorization
Kubernetes.configure do |config|
  # Configure API key authorization: BearerToken
  config.api_key['authorization'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['authorization'] = 'Bearer'
end

api_instance = Kubernetes::StorageV1beta1Api.new

name = "name_example" # String | name of the VolumeAttachment

opts = { 
  pretty: "pretty_example", # String | If 'true', then the output is pretty printed.
  exact: true, # BOOLEAN | Should the export be exact.  Exact export maintains cluster-specific fields like 'Namespace'.
  export: true # BOOLEAN | Should this value be exported.  Export strips fields that a user can not specify.
}

begin
  result = api_instance.read_volume_attachment(name, , opts)
  p result
rescue Kubernetes::ApiError => e
  puts "Exception when calling StorageV1beta1Api->read_volume_attachment: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **String**| name of the VolumeAttachment | 
 **pretty** | **String**| If &#39;true&#39;, then the output is pretty printed. | [optional] 
 **exact** | **BOOLEAN**| Should the export be exact.  Exact export maintains cluster-specific fields like &#39;Namespace&#39;. | [optional] 
 **export** | **BOOLEAN**| Should this value be exported.  Export strips fields that a user can not specify. | [optional] 

### Return type

[**V1beta1VolumeAttachment**](V1beta1VolumeAttachment.md)

### Authorization

[BearerToken](../README.md#BearerToken)

### HTTP request headers

 - **Content-Type**: */*
 - **Accept**: application/json, application/yaml, application/vnd.kubernetes.protobuf



# **replace_storage_class**
> V1beta1StorageClass replace_storage_class(name, body, opts)



replace the specified StorageClass

### Example
```ruby
# load the gem
require 'kubernetes'
# setup authorization
Kubernetes.configure do |config|
  # Configure API key authorization: BearerToken
  config.api_key['authorization'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['authorization'] = 'Bearer'
end

api_instance = Kubernetes::StorageV1beta1Api.new

name = "name_example" # String | name of the StorageClass

body = Kubernetes::V1beta1StorageClass.new # V1beta1StorageClass | 

opts = { 
  pretty: "pretty_example", # String | If 'true', then the output is pretty printed.
  dry_run: "dry_run_example" # String | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
}

begin
  result = api_instance.replace_storage_class(name, body, opts)
  p result
rescue Kubernetes::ApiError => e
  puts "Exception when calling StorageV1beta1Api->replace_storage_class: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **String**| name of the StorageClass | 
 **body** | [**V1beta1StorageClass**](V1beta1StorageClass.md)|  | 
 **pretty** | **String**| If &#39;true&#39;, then the output is pretty printed. | [optional] 
 **dry_run** | **String**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] 

### Return type

[**V1beta1StorageClass**](V1beta1StorageClass.md)

### Authorization

[BearerToken](../README.md#BearerToken)

### HTTP request headers

 - **Content-Type**: */*
 - **Accept**: application/json, application/yaml, application/vnd.kubernetes.protobuf



# **replace_volume_attachment**
> V1beta1VolumeAttachment replace_volume_attachment(name, body, opts)



replace the specified VolumeAttachment

### Example
```ruby
# load the gem
require 'kubernetes'
# setup authorization
Kubernetes.configure do |config|
  # Configure API key authorization: BearerToken
  config.api_key['authorization'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['authorization'] = 'Bearer'
end

api_instance = Kubernetes::StorageV1beta1Api.new

name = "name_example" # String | name of the VolumeAttachment

body = Kubernetes::V1beta1VolumeAttachment.new # V1beta1VolumeAttachment | 

opts = { 
  pretty: "pretty_example", # String | If 'true', then the output is pretty printed.
  dry_run: "dry_run_example" # String | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
}

begin
  result = api_instance.replace_volume_attachment(name, body, opts)
  p result
rescue Kubernetes::ApiError => e
  puts "Exception when calling StorageV1beta1Api->replace_volume_attachment: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **String**| name of the VolumeAttachment | 
 **body** | [**V1beta1VolumeAttachment**](V1beta1VolumeAttachment.md)|  | 
 **pretty** | **String**| If &#39;true&#39;, then the output is pretty printed. | [optional] 
 **dry_run** | **String**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] 

### Return type

[**V1beta1VolumeAttachment**](V1beta1VolumeAttachment.md)

### Authorization

[BearerToken](../README.md#BearerToken)

### HTTP request headers

 - **Content-Type**: */*
 - **Accept**: application/json, application/yaml, application/vnd.kubernetes.protobuf



