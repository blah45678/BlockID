# BlockID
This is the code for my team's Blockchain@UBC 2018 Blockathon submission.
The challenge was to solve the issue of homeless people in downtown East Vancouver not having IDs, which are required for them to get access to many services that they need (e.g. health care, banks etc).
Our solution was for homeless people to have access to an Ethereum wallet(s) via a (salted?) hash of something such as a biometric marker (fingerprint, iris etc) or any other unique thing that can be hashed. That hash is then turned into a private key (and therefore an Eth address), used to encrypt documents symmetrically which are then stored on IPFS, and the IPFS file location hash is stored on Ethereum in such a way that it can be retrieved again since it's linked to the person's Ethereum address.
The homeless person, nor the person wanting to ID them, would need to know anything about blockchain as all the backend details can be abstracted away in a simple software program. The user would only have to tap/scan whatever unique thing and the software would do all the conversions/fetching to retrieve the images of IDs, and decrypt them with the private key itself - which would only be stored in RAM, not on a disk.
In addition, organisations and other users could endorse users' IDs by attaching comments to a user's address that are signed by their private key corresponding to an address that is known to be a specific location (such as a housing office or food kitchen etc). This could either give extra trust to the validity of a scan of documents, or just replace the need for government IDs entirely (which is good enough for most low-security use cases such as accessing buildings and getting food/health care, but not good enough for, say, opening a bank account).
