# Azure Cache for Redis network isolation

| Virtual Network injection |   Private Link    |	Firewall rules  |
|   :------ |  :------ | :------ |
| Runs Redis Cache service in a Virtual Network. It can only be accessed from virtual machines and applications within the VNet. | Connect to an Azure Cache instance from your virtual network via a private endpoint. The endpoint is assigned a private IP address in a subnet within the virtual network | Only client connections from the specified IP address ranges can connect to the cache. |
| Not publicly addressable | Cache instances are available from both within the VNet and publicly | Publicly addressable |
| Only available for Premium Azure Cache | Supported on Basic, Standard, and Premium Azure Cache | Supported for all pricing tier |
| Most secure | Secure | Least secure |
| Most expensive | Expensive | Least expensive |


## References
* [Network isolation options](https://docs.microsoft.com/en-us/azure/azure-cache-for-redis/cache-network-isolation)