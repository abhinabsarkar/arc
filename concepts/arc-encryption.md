# Encryption in Azure Redis Cache
### Encryption in transit 
Recommendation is to use only TLS 1.2, to maintain all the communications secure and encrypted in transit.
### Encryption at rest
* **Non-persistent Redis** - Stored as in-memory data store, encryption at rest is not needed as the Virtual Machine that hosts the Redis node already guarantees the security and privacy of data in memory.
* **Persistent Redis** - Allows to persist data stored in Redis. Redis Persistence writes Redis data into an Azure Storage account that you own and manage. Azure Storage automatically encrypts data when it is persisted, and is encrypted with Microsoft-managed keys by default. You can continue to rely on Microsoft-managed keys for the encryption of your data, or you can manage encryption with your own keys. Data in Azure Storage is encrypted and decrypted transparently using 256-bit AES encryption, one of the strongest block ciphers available, and is FIPS 140-2 compliant. Azure Storage encryption is similar to BitLocker encryption on Windows.
## References
* [Encryption on Azure Cache for Redis](https://techcommunity.microsoft.com/t5/azure-paas-blog/encryption-on-azure-cache-for-redis/ba-p/1800449)