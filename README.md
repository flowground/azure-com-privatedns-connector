# ![LOGO](logo.png) PrivateDnsManagementClient **flow**ground Connector

## Description

A generated **flow**ground connector for the PrivateDnsManagementClient API (version 2018-09-01).

Generated from: https://api.apis.guru/v2/specs/azure.com/privatedns/2018-09-01/swagger.json<br/>
Generated at: 2019-05-07T17:38:37+03:00

## API Description

The Private DNS Management Client.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Lists the Private DNS zones in all resource groups in a subscription.

*Tags:* `PrivateZones`

#### Input Parameters
* `$top` - _optional_ - The maximum number of Private DNS zones to return. If not specified, returns up to 100 zones.
* `api-version` - _required_ - Client Api Version.
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Lists the Private DNS zones within a resource group.

*Tags:* `PrivateZones`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `$top` - _optional_ - The maximum number of record sets to return. If not specified, returns up to 100 record sets.
* `api-version` - _required_ - Client Api Version.
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Deletes a Private DNS zone. WARNING: All DNS records in the zone will also be deleted. This operation cannot be undone. Private DNS zone cannot be deleted unless all virtual network links to it are removed.

*Tags:* `PrivateZones`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `privateZoneName` - _required_ - The name of the Private DNS zone (without a terminating dot).
* `If-Match` - _optional_ - The ETag of the Private DNS zone. Omit this value to always delete the current zone. Specify the last-seen ETag value to prevent accidentally deleting any concurrent changes.
* `api-version` - _required_ - Client Api Version.
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Gets a Private DNS zone. Retrieves the zone properties, but not the virtual networks links or the record sets within the zone.

*Tags:* `PrivateZones`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `privateZoneName` - _required_ - The name of the Private DNS zone (without a terminating dot).
* `api-version` - _required_ - Client Api Version.
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Updates a Private DNS zone. Does not modify virtual network links or DNS records within the zone.

*Tags:* `PrivateZones`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `privateZoneName` - _required_ - The name of the Private DNS zone (without a terminating dot).
* `If-Match` - _optional_ - The ETag of the Private DNS zone. Omit this value to always overwrite the current zone. Specify the last-seen ETag value to prevent accidentally overwriting any concurrent changes.
* `api-version` - _required_ - Client Api Version.
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Creates or updates a Private DNS zone. Does not modify Links to virtual networks or DNS records within the zone.

*Tags:* `PrivateZones`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `privateZoneName` - _required_ - The name of the Private DNS zone (without a terminating dot).
* `If-Match` - _optional_ - The ETag of the Private DNS zone. Omit this value to always overwrite the current zone. Specify the last-seen ETag value to prevent accidentally overwriting any concurrent changes.
* `If-None-Match` - _optional_ - Set to '*' to allow a new Private DNS zone to be created, but to prevent updating an existing zone. Other values will be ignored.
* `api-version` - _required_ - Client Api Version.
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Lists all record sets in a Private DNS zone.

*Tags:* `RecordSets`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `privateZoneName` - _required_ - The name of the Private DNS zone (without a terminating dot).
* `$top` - _optional_ - The maximum number of record sets to return. If not specified, returns up to 100 record sets.
* `$recordsetnamesuffix` - _optional_ - The suffix label of the record set name to be used to filter the record set enumeration. If this parameter is specified, the returned enumeration will only contain records that end with ".<recordsetnamesuffix>".
* `api-version` - _required_ - Client Api Version.
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Lists the virtual network links to the specified Private DNS zone.

*Tags:* `VirtualNetworkLinks`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `privateZoneName` - _required_ - The name of the Private DNS zone (without a terminating dot).
* `$top` - _optional_ - The maximum number of virtual network links to return. If not specified, returns up to 100 virtual network links.
* `api-version` - _required_ - Client Api Version.
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Deletes a virtual network link to the specified Private DNS zone. WARNING: In case of a registration virtual network, all auto-registered DNS records in the zone for the virtual network will also be deleted. This operation cannot be undone.

*Tags:* `VirtualNetworkLinks`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `privateZoneName` - _required_ - The name of the Private DNS zone (without a terminating dot).
* `virtualNetworkLinkName` - _required_ - The name of the virtual network link.
* `If-Match` - _optional_ - The ETag of the virtual network link to the Private DNS zone. Omit this value to always delete the current zone. Specify the last-seen ETag value to prevent accidentally deleting any concurrent changes.
* `api-version` - _required_ - Client Api Version.
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Gets a virtual network link to the specified Private DNS zone.

*Tags:* `VirtualNetworkLinks`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `privateZoneName` - _required_ - The name of the Private DNS zone (without a terminating dot).
* `virtualNetworkLinkName` - _required_ - The name of the virtual network link.
* `api-version` - _required_ - Client Api Version.
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Updates a virtual network link to the specified Private DNS zone.

*Tags:* `VirtualNetworkLinks`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `privateZoneName` - _required_ - The name of the Private DNS zone (without a terminating dot).
* `virtualNetworkLinkName` - _required_ - The name of the virtual network link.
* `If-Match` - _optional_ - The ETag of the virtual network link to the Private DNS zone. Omit this value to always overwrite the current virtual network link. Specify the last-seen ETag value to prevent accidentally overwriting any concurrent changes.
* `api-version` - _required_ - Client Api Version.
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Creates or updates a virtual network link to the specified Private DNS zone.

*Tags:* `VirtualNetworkLinks`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `privateZoneName` - _required_ - The name of the Private DNS zone (without a terminating dot).
* `virtualNetworkLinkName` - _required_ - The name of the virtual network link.
* `If-Match` - _optional_ - The ETag of the virtual network link to the Private DNS zone. Omit this value to always overwrite the current virtual network link. Specify the last-seen ETag value to prevent accidentally overwriting any concurrent changes.
* `If-None-Match` - _optional_ - Set to '*' to allow a new virtual network link to the Private DNS zone to be created, but to prevent updating an existing link. Other values will be ignored.
* `api-version` - _required_ - Client Api Version.
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Lists the record sets of a specified type in a Private DNS zone.

*Tags:* `RecordSets`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `privateZoneName` - _required_ - The name of the Private DNS zone (without a terminating dot).
* `recordType` - _required_ - The type of record sets to enumerate.
    Possible values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT.
* `$top` - _optional_ - The maximum number of record sets to return. If not specified, returns up to 100 record sets.
* `$recordsetnamesuffix` - _optional_ - The suffix label of the record set name to be used to filter the record set enumeration. If this parameter is specified, the returned enumeration will only contain records that end with ".<recordsetnamesuffix>".
* `api-version` - _required_ - Client Api Version.
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Deletes a record set from a Private DNS zone. This operation cannot be undone.

*Tags:* `RecordSets`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `privateZoneName` - _required_ - The name of the Private DNS zone (without a terminating dot).
* `recordType` - _required_ - The type of DNS record in this record set. Record sets of type SOA cannot be deleted (they are deleted when the Private DNS zone is deleted).
    Possible values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT.
* `relativeRecordSetName` - _required_ - The name of the record set, relative to the name of the zone.
* `If-Match` - _optional_ - The ETag of the record set. Omit this value to always delete the current record set. Specify the last-seen ETag value to prevent accidentally deleting any concurrent changes.
* `api-version` - _required_ - Client Api Version.
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Gets a record set.

*Tags:* `RecordSets`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `privateZoneName` - _required_ - The name of the Private DNS zone (without a terminating dot).
* `recordType` - _required_ - The type of DNS record in this record set.
    Possible values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT.
* `relativeRecordSetName` - _required_ - The name of the record set, relative to the name of the zone.
* `api-version` - _required_ - Client Api Version.
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Updates a record set within a Private DNS zone.

*Tags:* `RecordSets`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `privateZoneName` - _required_ - The name of the Private DNS zone (without a terminating dot).
* `recordType` - _required_ - The type of DNS record in this record set.
    Possible values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT.
* `relativeRecordSetName` - _required_ - The name of the record set, relative to the name of the zone.
* `If-Match` - _optional_ - The ETag of the record set. Omit this value to always overwrite the current record set. Specify the last-seen ETag value to prevent accidentally overwriting concurrent changes.
* `api-version` - _required_ - Client Api Version.
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Creates or updates a record set within a Private DNS zone.

*Tags:* `RecordSets`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `privateZoneName` - _required_ - The name of the Private DNS zone (without a terminating dot).
* `recordType` - _required_ - The type of DNS record in this record set. Record sets of type SOA can be updated but not created (they are created when the Private DNS zone is created).
    Possible values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT.
* `relativeRecordSetName` - _required_ - The name of the record set, relative to the name of the zone.
* `If-Match` - _optional_ - The ETag of the record set. Omit this value to always overwrite the current record set. Specify the last-seen ETag value to prevent accidentally overwriting any concurrent changes.
* `If-None-Match` - _optional_ - Set to '*' to allow a new record set to be created, but to prevent updating an existing record set. Other values will be ignored.
* `api-version` - _required_ - Client Api Version.
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

## License

**flow**ground :- Telekom iPaaS / azure-com-privatedns-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
