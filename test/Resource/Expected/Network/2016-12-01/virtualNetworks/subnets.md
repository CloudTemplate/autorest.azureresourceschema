# Microsoft.Network/virtualNetworks/subnets template reference
API Version: 2016-12-01
## Template format

To create a Microsoft.Network/virtualNetworks/subnets resource, add the following JSON to the resources section of your template.

```json
{
  "name": "string",
  "type": "Microsoft.Network/virtualNetworks/subnets",
  "apiVersion": "2016-12-01",
  "id": "string",
  "properties": {
    "addressPrefix": "string",
    "networkSecurityGroup": {
      "id": "string",
      "location": "string",
      "tags": {},
      "properties": {
        "securityRules": [
          {
            "id": "string",
            "properties": {
              "description": "string",
              "protocol": "string",
              "sourcePortRange": "string",
              "destinationPortRange": "string",
              "sourceAddressPrefix": "string",
              "destinationAddressPrefix": "string",
              "access": "string",
              "priority": "integer",
              "direction": "string",
              "provisioningState": "string"
            },
            "name": "string",
            "etag": "string"
          }
        ],
        "defaultSecurityRules": [
          {
            "id": "string",
            "properties": {
              "description": "string",
              "protocol": "string",
              "sourcePortRange": "string",
              "destinationPortRange": "string",
              "sourceAddressPrefix": "string",
              "destinationAddressPrefix": "string",
              "access": "string",
              "priority": "integer",
              "direction": "string",
              "provisioningState": "string"
            },
            "name": "string",
            "etag": "string"
          }
        ],
        "resourceGuid": "string",
        "provisioningState": "string"
      },
      "etag": "string"
    },
    "routeTable": {
      "id": "string",
      "location": "string",
      "tags": {},
      "properties": {
        "routes": [
          {
            "id": "string",
            "properties": {
              "addressPrefix": "string",
              "nextHopType": "string",
              "nextHopIpAddress": "string",
              "provisioningState": "string"
            },
            "name": "string",
            "etag": "string"
          }
        ],
        "provisioningState": "string"
      },
      "etag": "string"
    },
    "resourceNavigationLinks": [
      {
        "id": "string",
        "properties": {
          "linkedResourceType": "string",
          "link": "string"
        },
        "name": "string"
      }
    ],
    "provisioningState": "string"
  },
  "etag": "string"
}
```
## Property values

The following tables describe the values you need to set in the schema.

<a id="Microsoft.Network/virtualNetworks/subnets" />
### Microsoft.Network/virtualNetworks/subnets object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  name | string | Yes |  |
|  type | enum | Yes | Microsoft.Network/virtualNetworks/subnets |
|  apiVersion | enum | Yes | 2016-12-01 |
|  id | string | No | Resource ID. |
|  properties | object | Yes | [SubnetPropertiesFormat object](#SubnetPropertiesFormat) |
|  etag | string | No | A unique read-only string that changes whenever the resource is updated. |


<a id="SubnetPropertiesFormat" />
### SubnetPropertiesFormat object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  addressPrefix | string | No | The address prefix for the subnet. |
|  networkSecurityGroup | object | No | The reference of the NetworkSecurityGroup resource. - [NetworkSecurityGroup object](#NetworkSecurityGroup) |
|  routeTable | object | No | The reference of the RouteTable resource. - [RouteTable object](#RouteTable) |
|  resourceNavigationLinks | array | No | Gets an array of references to the external resources using subnet. - [ResourceNavigationLink object](#ResourceNavigationLink) |
|  provisioningState | string | No | The provisioning state of the resource. |


<a id="NetworkSecurityGroup" />
### NetworkSecurityGroup object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  id | string | No | Resource ID. |
|  location | string | No | Resource location. |
|  tags | object | No | Resource tags. |
|  properties | object | No | [NetworkSecurityGroupPropertiesFormat object](#NetworkSecurityGroupPropertiesFormat) |
|  etag | string | No | A unique read-only string that changes whenever the resource is updated. |


<a id="RouteTable" />
### RouteTable object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  id | string | No | Resource ID. |
|  location | string | No | Resource location. |
|  tags | object | No | Resource tags. |
|  properties | object | No | [RouteTablePropertiesFormat object](#RouteTablePropertiesFormat) |
|  etag | string | No | Gets a unique read-only string that changes whenever the resource is updated. |


<a id="ResourceNavigationLink" />
### ResourceNavigationLink object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  id | string | No | Resource ID. |
|  properties | object | No | [ResourceNavigationLinkFormat object](#ResourceNavigationLinkFormat) |
|  name | string | No | Name of the resource that is unique within a resource group. This name can be used to access the resource. |


<a id="NetworkSecurityGroupPropertiesFormat" />
### NetworkSecurityGroupPropertiesFormat object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  securityRules | array | No | A collection of security rules of the network security group. - [SecurityRule object](#SecurityRule) |
|  defaultSecurityRules | array | No | The default security rules of network security group. - [SecurityRule object](#SecurityRule) |
|  resourceGuid | string | No | The resource GUID property of the network security group resource. |
|  provisioningState | string | No | The provisioning state of the public IP resource. Possible values are: 'Updating', 'Deleting', and 'Failed'. |


<a id="RouteTablePropertiesFormat" />
### RouteTablePropertiesFormat object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  routes | array | No | Collection of routes contained within a route table. - [Route object](#Route) |
|  provisioningState | string | No | The provisioning state of the resource. Possible values are: 'Updating', 'Deleting', and 'Failed'. |


<a id="ResourceNavigationLinkFormat" />
### ResourceNavigationLinkFormat object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  linkedResourceType | string | No | Resource type of the linked resource. |
|  link | string | No | Link to the external resource |


<a id="SecurityRule" />
### SecurityRule object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  id | string | No | Resource ID. |
|  properties | object | No | [SecurityRulePropertiesFormat object](#SecurityRulePropertiesFormat) |
|  name | string | No | The name of the resource that is unique within a resource group. This name can be used to access the resource. |
|  etag | string | No | A unique read-only string that changes whenever the resource is updated. |


<a id="Route" />
### Route object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  id | string | No | Resource ID. |
|  properties | object | No | [RoutePropertiesFormat object](#RoutePropertiesFormat) |
|  name | string | No | The name of the resource that is unique within a resource group. This name can be used to access the resource. |
|  etag | string | No | A unique read-only string that changes whenever the resource is updated. |


<a id="SecurityRulePropertiesFormat" />
### SecurityRulePropertiesFormat object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  description | string | No | A description for this rule. Restricted to 140 chars. |
|  protocol | enum | Yes | Network protocol this rule applies to. Possible values are 'Tcp', 'Udp', and '*'. - Tcp, Udp, * |
|  sourcePortRange | string | No | The source port or range. Integer or range between 0 and 65535. Asterix '*' can also be used to match all ports. |
|  destinationPortRange | string | No | The destination port or range. Integer or range between 0 and 65535. Asterix '*' can also be used to match all ports. |
|  sourceAddressPrefix | string | Yes | The CIDR or source IP range. Asterix '*' can also be used to match all source IPs. Default tags such as 'VirtualNetwork', 'AzureLoadBalancer' and 'Internet' can also be used. If this is an ingress rule, specifies where network traffic originates from.  |
|  destinationAddressPrefix | string | Yes | The destination address prefix. CIDR or source IP range. Asterix '*' can also be used to match all source IPs. Default tags such as 'VirtualNetwork', 'AzureLoadBalancer' and 'Internet' can also be used. |
|  access | enum | Yes | The network traffic is allowed or denied. Possible values are: 'Allow' and 'Deny'. - Allow or Deny |
|  priority | integer | No | The priority of the rule. The value can be between 100 and 4096. The priority number must be unique for each rule in the collection. The lower the priority number, the higher the priority of the rule. |
|  direction | enum | Yes | The direction of the rule. The direction specifies if rule will be evaluated on incoming or outcoming traffic. Possible values are: 'Inbound' and 'Outbound'. - Inbound or Outbound |
|  provisioningState | string | No | The provisioning state of the public IP resource. Possible values are: 'Updating', 'Deleting', and 'Failed'. |


<a id="RoutePropertiesFormat" />
### RoutePropertiesFormat object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  addressPrefix | string | No | The destination CIDR to which the route applies. |
|  nextHopType | enum | Yes | The type of Azure hop the packet should be sent to. Possible values are: 'VirtualNetworkGateway', 'VnetLocal', 'Internet', 'VirtualAppliance', and 'None'. - VirtualNetworkGateway, VnetLocal, Internet, VirtualAppliance, None |
|  nextHopIpAddress | string | No | The IP address packets should be forwarded to. Next hop values are only allowed in routes where the next hop type is VirtualAppliance. |
|  provisioningState | string | No | The provisioning state of the resource. Possible values are: 'Updating', 'Deleting', and 'Failed'. |

