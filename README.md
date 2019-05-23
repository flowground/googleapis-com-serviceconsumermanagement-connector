# ![LOGO](logo.png) Service Consumer Management **flow**ground Connector

## Description

A generated **flow**ground connector for the Service Consumer Management API (version v1).

Generated from: https://api.apis.guru/v2/specs/googleapis.com/serviceconsumermanagement/v1/swagger.json<br/>
Generated at: 2019-05-23T12:13:38+03:00

## API Description

Manages the service consumers of a Service Infrastructure service.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Delete a tenancy unit.  Before the tenancy unit is deleted, there should be<br/>
> no tenant resources in it not in DELETED state.<br/>
> Operation<response: Empty>.

*Tags:* `services`

#### Input Parameters
* `name` - _required_ - Name of the tenancy unit to be deleted.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Gets the latest state of a long-running operation.  Clients can use this<br/>
> method to poll the operation result at intervals as recommended by the API<br/>
> service.

*Tags:* `operations`

#### Input Parameters
* `name` - _required_ - The name of the operation resource.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Apply configuration to an existing tenant project.<br/>
> This project must exist in active state and have the original owner<br/>
> account. Caller must have the permission to add a project to the given<br/>
> tenancy unit. Configuration will be applied, but any existing settings on<br/>
> the project will not be modified.<br/>
> Specified policy bindings will be applied. Existing binding will not be<br/>
> modified.<br/>
> Specified services will be activated.   No service will be deactivated.<br/>
> New billing configuration will be applied if specified.<br/>
> Omit billing configuration to keep the existing one.<br/>
> Service account in the project will be created if previously non existing.<br/>
> Specified folder will be ignored, moving tenant project to a different<br/>
> folder is not supported.<br/>
> Operation fails if any of the steps fail, but no rollback of already<br/>
> applied configuration changes is attempted.<br/>
> Operation<response: Empty>.

*Tags:* `services`

#### Input Parameters
* `name` - _required_ - Name of the tenancy unit.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Attach an existing project to the tenancy unit as a new tenant<br/>
> resource. The project could be either the tenant project reserved by<br/>
> calling AddTenantProject under tenancy unit for the producer project of<br/>
> service, or from outside.<br/>
> Caller will be checked against the permission as if calling<br/>
> AddTenantProject on the same consumer.<br/>
> To trigger the attachement, the targeted tenant project must be in a<br/>
> folder. Please also make sure ServiceConsumerManagement service account is<br/>
> the owner of that project. Note that these two requirements are already met<br/>
> if the project is reserved through AddTenantProject.<br/>
> Operation<response: Empty>.

*Tags:* `services`

#### Input Parameters
* `name` - _required_ - Name of the tenancy unit that project will be attached to.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Starts asynchronous cancellation on a long-running operation.  The server<br/>
> makes a best effort to cancel the operation, but success is not<br/>
> guaranteed.  If the server doesn't support this method, it returns<br/>
> `google.rpc.Code.UNIMPLEMENTED`.  Clients can use<br/>
> Operations.GetOperation or<br/>
> other methods to check whether the cancellation succeeded or whether the<br/>
> operation completed despite cancellation. On successful cancellation,<br/>
> the operation is not deleted; instead, it becomes an operation with<br/>
> an Operation.error value with a google.rpc.Status.code of 1,<br/>
> corresponding to `Code.CANCELLED`.

*Tags:* `operations`

#### Input Parameters
* `name` - _required_ - The name of the operation resource to be cancelled.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Removes specified project resource identified by tenant resource tag.<br/>
> It will remove project lien with 'TenantManager' origin if that was added.<br/>
> It will then attempt to delete the project. If that operation fails, this<br/>
> method fails.<br/>
> Calls to remove already removed or non-existent tenant project<br/>
> will succeed.<br/>
> After the project has been deleted, or if was already in DELETED state,<br/>
> resource metadata is permanently removed from the tenancy unit.<br/>
> Operation<response: Empty>.

*Tags:* `services`

#### Input Parameters
* `name` - _required_ - Name of the tenancy unit.
Such as 'services/service.googleapis.com/projects/12345/tenancyUnits/abcd'.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Find the tenancy unit for a service and consumer.<br/>
> This method should not be used in producers' runtime path, for example<br/>
> finding the tenant project number when creating VMs. Producers should<br/>
> persist the tenant project information after the project is created.

*Tags:* `services`

#### Input Parameters
* `filter` - _optional_ - Filter expression over tenancy resources field. Optional.
* `pageSize` - _optional_ - The maximum number of results returned by this request.
* `pageToken` - _optional_ - The continuation token, which is used to page through large result sets.
To get the next page of results, set this parameter to the value of
`nextPageToken` from the previous response.
* `parent` - _required_ - Service and consumer. Required.
services/{service}/{collection id}/{resource id}
{collection id} is the cloud resource collection type representing the
service consumer, for example 'projects', or 'organizations'.
{resource id} is the consumer numeric id, such as project number: '123456'.
{service} the name of a service, for example 'service.googleapis.com'.
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Creates a tenancy unit with no tenant resources.

*Tags:* `services`

#### Input Parameters
* `parent` - _required_ - services/{service}/{collection id}/{resource id}
{collection id} is the cloud resource collection type representing the
service consumer, for example 'projects', or 'organizations'.
{resource id} is the consumer numeric id, such as project number: '123456'.
{service} the name of a service, for example 'service.googleapis.com'.
Enabled service binding using the new tenancy unit.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Add a new tenant project to the tenancy unit.<br/>
> There can be at most 512 tenant projects in a tenancy unit.<br/>
> If there are previously failed `AddTenantProject` calls, you might need to<br/>
> call `RemoveTenantProject` first to clean them before you can make another<br/>
> `AddTenantProject` with the same tag.<br/>
> Operation<response: Empty>.

*Tags:* `services`

#### Input Parameters
* `parent` - _required_ - Name of the tenancy unit.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Search tenancy units for a service.

*Tags:* `services`

#### Input Parameters
* `pageSize` - _optional_ - The maximum number of results returned by this request. Currently, the
default maximum is set to 1000. If page_size is not provided or the size
provided is a number larger than 1000, it will be automatically set to
1000.

Optional.
* `pageToken` - _optional_ - The continuation token, which is used to page through large result sets.
To get the next page of results, set this parameter to the value of
`nextPageToken` from the previous response.

Optional.
* `parent` - _required_ - Service for which search is performed.
services/{service}
{service} the name of a service, for example 'service.googleapis.com'.
* `query` - _optional_ - Set a query `{expression}` for querying tenancy units. Your `{expression}`
must be in the format: `field_name=literal_string`. The `field_name` is the
name of the field you want to compare. Supported fields are
`tenant_resources.tag` and `tenant_resources.resource`.

For example, to search tenancy units that contain at least one tenant
resource with given tag 'xyz', use query `tenant_resources.tag=xyz`.
To search tenancy units that contain at least one tenant resource with
given resource name 'projects/123456', use query
`tenant_resources.resource=projects/123456`.

Multiple expressions can be joined with `AND`s. Tenancy units must match
all expressions to be included in the result set. For example,
`tenant_resources.tag=xyz AND tenant_resources.resource=projects/123456`

Optional.
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

## License

**flow**ground :- Telekom iPaaS / googleapis-com-serviceconsumermanagement-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
