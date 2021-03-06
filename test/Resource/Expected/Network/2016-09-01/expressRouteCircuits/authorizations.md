# Microsoft.Network/expressRouteCircuits/authorizations template reference
API Version: 2016-09-01
## Template format

To create a Microsoft.Network/expressRouteCircuits/authorizations resource, add the following JSON to the resources section of your template.

```json
{
  "name": "string",
  "type": "Microsoft.Network/expressRouteCircuits/authorizations",
  "apiVersion": "2016-09-01",
  "id": "string",
  "properties": {
    "authorizationKey": "string",
    "authorizationUseStatus": "string",
    "provisioningState": "string"
  },
  "etag": "string"
}
```
## Property values

The following tables describe the values you need to set in the schema.

<a id="Microsoft.Network/expressRouteCircuits/authorizations" />
### Microsoft.Network/expressRouteCircuits/authorizations object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  name | string | Yes |  |
|  type | enum | Yes | Microsoft.Network/expressRouteCircuits/authorizations |
|  apiVersion | enum | Yes | 2016-09-01 |
|  id | string | No | Resource ID. |
|  properties | object | Yes | [AuthorizationPropertiesFormat object](#AuthorizationPropertiesFormat) |
|  etag | string | No | A unique read-only string that changes whenever the resource is updated. |


<a id="AuthorizationPropertiesFormat" />
### AuthorizationPropertiesFormat object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  authorizationKey | string | No | The authorization key. |
|  authorizationUseStatus | enum | No | AuthorizationUseStatus. Possible values are: 'Available' and 'InUse'. - Available or InUse |
|  provisioningState | string | No | Gets the provisioning state of the public IP resource. Possible values are: 'Updating', 'Deleting', and 'Failed'. |

