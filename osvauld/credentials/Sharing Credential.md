
##### What happens when you share a credential


- gets the details of the [[Credential]] using the credential id
- [[Decryption]] occurs
- gets the public keys of all target [[Users]] /[[Group]] whom the user wants to share the credential with also adds the [[Access Types]] 
- [[Encryption]] is done.
- sends the payload to back end.