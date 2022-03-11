# Deployed contracts: https://ropsten.etherscan.io/address/0x81c287B84c3705Cf1Fb1ac6DAc63fBd61f8eAEe3
# Deployed front-end: https://DeCT.ndehouche.repl.co

# Decentralized Clinical Trials Management
Contracts to manage the ownership, licensing and access control of clinical trial data
Added-value of a public (permissionless) blockchain: Access Management and Payment Processing
Limitation of a public blockchain: Data storage
Architecture choice: Smart contract for access management and payment processing, external service (arweave, Ocean libraries, IPFS) for data storage.

Three categories of users:

**Contract owner:**
Verifies data collectors.

**Data collector:**
Verified identity, 
Deposits data in external source, 
Creates a dataset, 
Id, 
Hash, 
Owner, 
Creator,  
Royalties.

**Data owner:**
Has attributes (no PII), stored in a struct, 
Verifies that data has been correctly deposited, 
Agrees on royalties, 
Determines access duration, 
Approves data creation,  
Mapping is created.

**Data licensee:**
Anonymous, defined by address, 
Pays fee, split between data collector and data owner, as per royalty agreement, 
Access is temporarily granted, 
Whitelisted licensees go past a Web3js/EtherJs paywall to access data.

**Additional modules:**
Search for data owners according to a clinical trial’s criteria, 
Randomization with Chainlink VRF.

