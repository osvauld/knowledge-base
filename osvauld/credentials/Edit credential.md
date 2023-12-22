When editing credential fetch all the shared users of the [[Credential]] , [[Decryption|| decrypt]] the credential using [[Users]] private key then [[Encryption|| encrypt]] with the shared users key and send the payload. 
BE will delete the old encrypted data and update it with new data. Only [[Owner]]  of credential can edit it.
[[Changing access Type]]
This process is currently not reversible.