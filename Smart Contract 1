# Smart Contracts

Self-executing code /agreements recorded on a blockchain that automate the terms of a deal, ensuring transparency and security. (e.g., written in Solidity for Ethereum).

![image](https://github.com/user-attachments/assets/3b08659e-b1e0-4632-b409-70c1aaee79d9)

## Types of Smart Contracts

### 1. Smart Legal Contract:

There are legal guarantees for smart contracts. They follow the format seen in contracts: "If this occurs, then this will occur." Legal smart contracts provide more openness between contracting entities than traditional documents because they are stored on blockchain and cannot be altered. Contracts are executed by the parties using digital signatures.

### 2. Decentralized Autonomous Organizations (DAOs):

DAOs are democratic organisations with voting powers granted by a smart contract. A decentralised autonomous organisation, or DAO, is a blockchain-based entity with a shared goal under collective governance. There is no such thing as an executive or president. Instead, the organization's operations and the distribution of assets are governed by blockchain-based principles that are incorporated into the contract's code.

### 3. Application Logic Contracts:

Application-based code that usually keeps up with multiple other blockchain contracts makes up application logic contracts, or ALCs. It permits device-to-device interactions such as blockchain integration and the Internet of Things. These are signed between computers and other contracts rather than between people or organisations like other kinds of smart contracts.

![image](https://github.com/user-attachments/assets/fdd3a1b9-03c5-48e0-8749-8743d16171ba)


## Smart Contract Working

![image](https://github.com/user-attachments/assets/6c50806c-fbac-4d5c-96cd-6fe7923477ae)

#### Identify Agreement: 
Multiple parties identify the cooperative opportunity and desired outcomes and agreements could include business processes, asset swaps, etc.

#### Set conditions: 
Smart contracts could be initiated by parties themselves or when certain conditions are met like financial market indices, events like GPS locations, etc.

#### Code business logic:
A computer program is written that will be executed automatically when the conditional parameters are met.

#### Encryption and blockchain technology: 
Encryption provides secure authentication and transfer of messages between parties relating to smart contracts.

#### Execution and processing: 
In blockchain iteration, whenever consensus is reached between the parties regarding authentication and verification then the code is executed and the outcomes are memorialized for compliance and verification.

#### Network updates: 
After smart contracts are executed, all the nodes on the network update their ledger to reflect the new state. Once the record is posted and verified on the blockchain network, it cannot be modified, it is in append mode only.




## a basic Solidity smart contract that stores and retrieves a single integer value. Deploy it on Remix IDE.

steps :-
1.Open remix.ethereum.org
2.Create new file (SimpleStorage.sol)
3.Paste the code
4. Compile using Solidity compiler plugin
5. go to debug then under environment option , select metamask and connect to your metamask account. 
![image](https://github.com/user-attachments/assets/7e15b9c4-afd0-4341-bb35-71d3e11839e7)

![Screenshot 2025-05-18 114112](https://github.com/user-attachments/assets/356ca2a8-a0ea-44e6-ab7c-95af1422c5d3)

6.Deploy using Deploy & Run Transactions plugin
7. then copy the transaction address and go and paste it on etherscan and done with it .

## code  
``` 
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract SimpleStorage {
    uint storedData;
    
    function set(uint x) public {
        storedData = x;
    }
    
    function get() public view returns (uint) {
        return storedData;
    }
}
``` 


![Image](https://github.com/user-attachments/assets/e7afc484-4217-4d7d-9534-6288594abb9a)

![Screenshot 2025-05-18 113656](https://github.com/user-attachments/assets/845c852b-ffd0-41ae-b8d9-dd8ca72a3a10)

## Question:
Create a voting system with multiple candidates. Each address can vote only once.

Write a contract that manages a list of student records (name, roll number). Allow adding and retrieving student data.

Develop a contract that only allows the deployer (owner) to call a specific function (use modifiers).

Write a contract where people can donate Ether and the top 3 donors are tracked.

Implement a simple auction system where users can place bids, and the highest bidder wins.

Create a contract that splits incoming Ether between 3 fixed addresses.
