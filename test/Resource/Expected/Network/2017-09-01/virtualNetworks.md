# Microsoft.Network/virtualNetworks template reference
API Version: 2017-09-01
## Template format

To create a Microsoft.Network/virtualNetworks resource, add the following JSON to the resources section of your template.

```json
{
  "name": "string",
  "type": "Microsoft.Network/virtualNetworks",
  "apiVersion": "2017-09-01",
  "id": "string",
  "location": "string",
  "tags": {},
  "properties": {
    "addressSpace": {
      "addressPrefixes": [
        "string"
      ]
    },
    "dhcpOptions": {
      "dnsServers": [
        "string"
      ]
    },
    "subnets": [
      {
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
          "serviceEndpoints": [
            {
              "service": "string",
              "locations": [
                "string"
              ],
              "provisioningState": "string"
            }
          ],
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
        "name": "string",
        "etag": "string"
      }
    ],
    "virtualNetworkPeerings": [
      {
        "id": "string",
        "properties": {
          "allowVirtualNetworkAccess": boolean,
          "allowForwardedTraffic": boolean,
          "allowGatewayTransit": boolean,
          "useRemoteGateways": boolean,
          "remoteVirtualNetwork": {
            "id": "string"
          },
          "remoteAddressSpace": {
            "addressPrefixes": [
              "string"
            ]
          },
          "peeringState": "string",
          "provisioningState": "string"
        },
        "name": "string",
        "etag": "string"
      }
    ],
    "resourceGuid": "string",
    "provisioningState": "string",
    "enableDdosProtection": boolean,
    "enableVmProtection": boolean
  },
  "etag": "string",
  "resources": []
}
```
## Property values

The following tables describe the values you need to set in the schema.

<a id="Microsoft.Network/virtualNetworks" />
### Microsoft.Network/virtualNetworks object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  name | string | Yes |  |
|  type | enum | Yes | Microsoft.Network/virtualNetworks |
|  apiVersion | enum | Yes | 2017-09-01 |
|  id | string | No | Resource ID. |
|  location | string | No | Resource location. |
|  tags | object | No | Resource tags. |
|  properties | object | Yes | Properties of the virtual network. - [VirtualNetworkPropertiesFormat object](#VirtualNetworkPropertiesFormat) |
|  etag | string | No | Gets a unique read-only string that changes whenever the resource is updated. |
|  resources | array | No | [virtualNetworkPeerings](./virtualNetworks/virtualNetworkPeerings.md) [subnets](./virtualNetworks/subnets.md) |


<a id="VirtualNetworkPropertiesFormat" />
### VirtualNetworkPropertiesFormat object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  addressSpace | object | No | The AddressSpace that contains an array of IP address ranges that can be used by subnets. - [AddressSpace object](#AddressSpace) |
|  dhcpOptions | object | No | The dhcpOptions that contains an array of DNS servers available to VMs deployed in the virtual network. - [DhcpOptions object](#DhcpOptions) |
|  subnets | array | No | A list of subnets in a Virtual Network. - [Subnet object](#Subnet) |
|  virtualNetworkPeerings | array | No | A list of peerings in a Virtual Network. - [VirtualNetworkPeering object](#VirtualNetworkPeering) |
|  resourceGuid | string | No | The resourceGuid property of the Virtual Network resource. |
|  provisioningState | string | No | The provisioning state of the PublicIP resource. Possible values are: 'Updating', 'Deleting', and 'Failed'. |
|  enableDdosProtection | boolean | No | Indicates if DDoS protection is enabled for all the protected resources in a Virtual Network. |
|  enableVmProtection | boolean | No | Indicates if Vm protection is enabled for all the subnets in a Virtual Network. |


<a id="AddressSpace" />
### AddressSpace object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  addressPrefixes | array | No | A list of address blocks reserved for this virtual network in CIDR notation. - string |


<a id="DhcpOptions" />
### DhcpOptions object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  dnsServers | array | No | The list of DNS servers IP addresses. - string |


<a id="Subnet" />
### Subnet object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  id | string | No | Resource ID. |
|  properties | object | No | Properties of the subnet. - [SubnetPropertiesFormat object](#SubnetPropertiesFormat) |
|  name | string | No | The name of the resource that is unique within a resource group. This name can be used to access the resource. |
|  etag | string | No | A unique read-only string that changes whenever the resource is updated. |


<a id="VirtualNetworkPeering" />
### VirtualNetworkPeering object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  id | string | No | Resource ID. |
|  properties | object | No | Properties of the virtual network peering. - [VirtualNetworkPeeringPropertiesFormat object](#VirtualNetworkPeeringPropertiesFormat) |
|  name | string | No | The name of the resource that is unique within a resource group. This name can be used to access the resource. |
|  etag | string | No | A unique read-only string that changes whenever the resource is updated. |


<a id="SubnetPropertiesFormat" />
### SubnetPropertiesFormat object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  addressPrefix | string | No | The address prefix for the subnet. |
|  networkSecurityGroup | object | No | The reference of the NetworkSecurityGroup resource. - [NetworkSecurityGroup object](#NetworkSecurityGroup) |
|  routeTable | object | No | The reference of the RouteTable resource. - [RouteTable object](#RouteTable) |
|  serviceEndpoints | array | No | An array of service endpoints. - [ServiceEndpointPropertiesFormat object](#ServiceEndpointPropertiesFormat) |
|  resourceNavigationLinks | array | No | Gets an array of references to the external resources using subnet. - [ResourceNavigationLink object](#ResourceNavigationLink) |
|  provisioningState | string | No | The provisioning state of the resource. |


<a id="VirtualNetworkPeeringPropertiesFormat" />
### VirtualNetworkPeeringPropertiesFormat object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  allowVirtualNetworkAccess | boolean | No | Whether the VMs in the linked virtual network space would be able to access all the VMs in local Virtual network space. |
|  allowForwardedTraffic | boolean | No | Whether the forwarded traffic from the VMs in the remote virtual network will be allowed/disallowed. |
|  allowGatewayTransit | boolean | No | If gateway links can be used in remote virtual networking to link to this virtual network. |
|  useRemoteGateways | boolean | No | If remote gateways can be used on this virtual network. If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit. Only one peering can have this flag set to true. This flag cannot be set if virtual network already has a gateway. |
|  remoteVirtualNetwork | object | No | The reference of the remote virtual network. The remote virtual network can be in the same or different region (preview). See here to register for the preview and learn more (https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-create-peering). - [SubResource object](#SubResource) |
|  remoteAddressSpace | object | No | The reference of the remote virtual network address space. - [AddressSpace object](#AddressSpace) |
|  peeringState | enum | No | The status of the virtual network peering. Possible values are 'Initiated', 'Connected', and 'Disconnected'. - Initiated, Connected, Disconnected |
|  provisioningState | string | No | The provisioning state of the resource. |


<a id="NetworkSecurityGroup" />
### NetworkSecurityGroup object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  id | string | No | Resource ID. |
|  location | string | No | Resource location. |
|  tags | object | No | Resource tags. |
|  properties | object | No | Properties of the network security group - [NetworkSecurityGroupPropertiesFormat object](#NetworkSecurityGroupPropertiesFormat) |
|  etag | string | No | A unique read-only string that changes whenever the resource is updated. |


<a id="RouteTable" />
### RouteTable object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  id | string | No | Resource ID. |
|  location | string | No | Resource location. |
|  tags | object | No | Resource tags. |
|  properties | object | No | Properties of the route table. - [RouteTablePropertiesFormat object](#RouteTablePropertiesFormat) |
|  etag | string | No | Gets a unique read-only string that changes whenever the resource is updated. |


<a id="ServiceEndpointPropertiesFormat" />
### ServiceEndpointPropertiesFormat object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  service | string | No | The type of the endpoint service. |
|  locations | array | No | A list of locations. - string |
|  provisioningState | string | No | The provisioning state of the resource. |


<a id="ResourceNavigationLink" />
### ResourceNavigationLink object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  id | string | No | Resource ID. |
|  properties | object | No | Resource navigation link properties format. - [ResourceNavigationLinkFormat object](#ResourceNavigationLinkFormat) |
|  name | string | No | Name of the resource that is unique within a resource group. This name can be used to access the resource. |


<a id="SubResource" />
### SubResource object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  id | string | No | Resource ID. |


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
|  properties | object | No | Properties of the security rule - [SecurityRulePropertiesFormat object](#SecurityRulePropertiesFormat) |
|  name | string | No | The name of the resource that is unique within a resource group. This name can be used to access the resource. |
|  etag | string | No | A unique read-only string that changes whenever the resource is updated. |


<a id="Route" />
### Route object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  id | string | No | Resource ID. |
|  properties | object | No | Properties of the route. - [RoutePropertiesFormat object](#RoutePropertiesFormat) |
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


<a id="RoutePropertiesFormat" />
### RoutePropertiesFormat object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  addressPrefix | string | No | The destination CIDR to which the route applies. |
|  nextHopType | enum | Yes | The type of Azure hop the packet should be sent to. Possible values are: 'VirtualNetworkGateway', 'VnetLocal', 'Internet', 'VirtualAppliance', and 'None'. - VirtualNetworkGateway, VnetLocal, Internet, VirtualAppliance, None |
|  nextHopIpAddress | string | No | The IP address packets should be forwarded to. Next hop values are only allowed in routes where the next hop type is VirtualAppliance. |
|  provisioningState | string | No | The provisioning state of the resource. Possible values are: 'Updating', 'Deleting', and 'Failed'. |


<a id="ApplicationSecurityGroup" />
### ApplicationSecurityGroup object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  id | string | No | Resource ID. |
|  location | string | No | Resource location. |
|  tags | object | No | Resource tags. |
|  properties | object | No | Properties of the application security group. - [ApplicationSecurityGroupPropertiesFormat object](#ApplicationSecurityGroupPropertiesFormat) |

