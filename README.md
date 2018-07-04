# Kickstart
* [Kickstarter Crowdfunding Essential Training](https://www.linkedin.com/learning/kickstarter-crowdfunding-essential-training)
* [Types](http://solidity.readthedocs.io/en/v0.4.24/types.html)
## CLI
* npm init - generate package.json
* npm install --save ganache-cli mocha solc fs-extra web3@1.0.0-beta.26 

## Infura
* npm install --save truffle-hdwallet-provider

https://rinkeby.infura.io/3kA8ESeQXjRLadxqbhvB

## Truffle
* npm install truffle-hdwallet-provider

## Campaign Contract
### Variables
**Variables** | - | - 
--- | --- | ---
**manager** | `address` | address of the person who is managing the campaign
**minimumContribution** | `uint` | Min donation required to be considered a contributor or `approver`
**approvers** | `mapping` | List of addresses for every person who has donated money
**requests** | `Request[]` | List of requests that the manager has created.

### Functions
Functions | - | -
--- | --- | ---
**Campaign** | Constructor function that sets the minimumContribution and the owner
**contribute** | Called when someone wants to donate money to the campaign and become 'approver'
**createRequest** | Called by the manager to create a new `spending request`
**approveRequest** | Called by each contributor to approve a spending request
**finalizeRequest** | After a request has gotten enough approvals, the manager can call this to get money sent to the vendor

### Struct
**Request Struct** | - | - 
--- | --- | ---
**description** | string | Purpose of request.
**amount** | uint | Ether to transfer.
**recipient** | address | Who gets the money.
**complete** | bool | Whether the request is done.
**approvals** | mapping | Track who has voted.
**approvalCount** | uint | Track number of approvals.


## Variables
* [Units and Globally Available Variables](http://solidity.readthedocs.io/en/v0.4.24/units-and-global-variables.html)

## Reference Types
**Name** | Notes | Examples 
--- | --- | ---
**fixed array** | Array that contains a single type of element.  It has an unchanging length. | int[3] --> [1,2,3], bool[2] --> [true, false]
**dynamic array** | Array that contains a single type of element.  Over time it can change in size. | int[] --> [1,2,3], bool[] --> [true, false]
**mapping** | Collection of key value pairs.  Think of Javascript object, Ruby hashes, or Python dictionary.  All keys must be of the same type and all value must be of the same type. | mapping(string => string), mapping(int => bool)
**struct** | Collection of key value pairs that can have different types. | Struct Car{string make; string model; unit value;}
