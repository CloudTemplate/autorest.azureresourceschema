# Microsoft.Network/networkSecurityGroups template reference
API Version: 2017-10-01
## Template format

To create a Microsoft.Network/networkSecurityGroups resource, add the following JSON to the resources section of your template.

```json
{
  "name": "string",
  "type": "Microsoft.Network/networkSecurityGroups",
  "apiVersion": "2017-10-01",
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
          "sourceAddressPrefixes": [
            "string"
          ],
          "sourceApplicationSecurityGroups": [
            {
              "id": "string",
              "location": "string",
              "tags": {},
              "properties": {}
            }
          ],
          "destinationAddressPrefix": "string",
          "destinationAddressPrefixes": [
            "string"
          ],
          "destinationApplicationSecurityGroups": [
            {
              "id": "string",
              "location": "string",
              "tags": {},
              "properties": {}
            }
          ],
          "sourcePortRanges": [
            "string"
          ],
          "destinationPortRanges": [
            "string"
          ],
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
          "sourceAddressPrefixes": [
            "string"
          ],
          "sourceApplicationSecurityGroups": [
            {
              "id": "string",
              "location": "string",
              "tags": {},
              "properties": {}
            }
          ],
          "destinationAddressPrefix": "string",
          "destinationAddressPrefixes": [
            "string"
          ],
          "destinationApplicationSecurityGroups": [
            {
              "id": "string",
              "location": "string",
              "tags": {},
              "properties": {}
            }
          ],
          "sourcePortRanges": [
            "string"
          ],
          "destinationPortRanges": [
            "string"
          ],
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
  "etag": "string",
  "resources": []
}
```
## Property values

The following tables describe the values you need to set in the schema.

<a id="Microsoft.Network/networkSecurityGroups" />
### Microsoft.Network/networkSecurityGroups object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  name | string | Yes |  |
|  type | enum | Yes | Microsoft.Network/networkSecurityGroups |
|  apiVersion | enum | Yes | 2017-10-01 |
|  id | string | No | Resource ID. |
|  location | string | No | Resource location. |
|  tags | object | No | Resource tags. |
|  properties | object | Yes | Properties of the network security group - [NetworkSecurityGroupPropertiesFormat object](#NetworkSecurityGroupPropertiesFormat) |
|  etag | string | No | A unique read-only string that changes whenever the resource is updated. |
|  resources | array | No | [securityRules](./networkSecurityGroups/securityRules.md) |


<a id="NetworkSecurityGroupPropertiesFormat" />
### NetworkSecurityGroupPropertiesFormat object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  securityRules | array | No | A collection of security rules of the network security group. - [SecurityRule object](#SecurityRule) |
|  defaultSecurityRules | array | No | The default security rules of network security group. - [SecurityRule object](#SecurityRule) |
|  resourceGuid | string | No | The resource GUID property of the network security group resource. |
|  provisioningState | string | No | The provisioning state of the public IP resource. Possible values are: 'Updating', 'Deleting', and 'Failed'. |


<a id="SecurityRule" />
### SecurityRule object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  id | string | No | Resource ID. |
|  properties | object | No | Properties of the security rule - [SecurityRulePropertiesFormat object](#SecurityRulePropertiesFormat) |
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
|  sourceAddressPrefix | string | No | The CIDR or source IP range. Asterix '*' can also be used to match all source IPs. Default tags such as 'VirtualNetwork', 'AzureLoadBalancer' and 'Internet' can also be used. If this is an ingress rule, specifies where network traffic originates from.  |
|  sourceAddressPrefixes | array | No | The CIDR or source IP ranges. - string |
|  sourceApplicationSecurityGroups | array | No | The application security group specified as source. - [ApplicationSecurityGroup object](#ApplicationSecurityGroup) |
|  destinationAddressPrefix | string | No | The destination address prefix. CIDR or destination IP range. Asterix '*' can also be used to match all source IPs. Default tags such as 'VirtualNetwork', 'AzureLoadBalancer' and 'Internet' can also be used. |
|  destinationAddressPrefixes | array | No | The destination address prefixes. CIDR or destination IP ranges. - string |
|  destinationApplicationSecurityGroups | array | No | The application security group specified as destination. - [ApplicationSecurityGroup object](#ApplicationSecurityGroup) |
|  sourcePortRanges | array | No | The source port ranges. - string |
|  destinationPortRanges | array | No | The destination port ranges. - string |
|  access | enum | Yes | The network traffic is allowed or denied. Possible values are: 'Allow' and 'Deny'. - Allow or Deny |
|  priority | integer | No | The priority of the rule. The value can be between 100 and 4096. The priority number must be unique for each rule in the collection. The lower the priority number, the higher the priority of the rule. |
|  direction | enum | Yes | The direction of the rule. The direction specifies if rule will be evaluated on incoming or outcoming traffic. Possible values are: 'Inbound' and 'Outbound'. - Inbound or Outbound |
|  provisioningState | string | No | The provisioning state of the public IP resource. Possible values are: 'Updating', 'Deleting', and 'Failed'. |


<a id="ApplicationSecurityGroup" />
### ApplicationSecurityGroup object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  id | string | No | Resource ID. |
|  location | string | No | Resource location. |
|  tags | object | No | Resource tags. |
|  properties | object | No | Properties of the application security group. - [ApplicationSecurityGroupPropertiesFormat object](#ApplicationSecurityGroupPropertiesFormat) |

