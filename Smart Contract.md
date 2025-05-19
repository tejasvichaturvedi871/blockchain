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
1-Create a voting system with multiple candidates. Each address can vote only once.

2-Write a contract that manages a list of student records (name, roll number). Allow adding and retrieving student data.

3-Develop a contract that only allows the deployer (owner) to call a specific function (use modifiers).

4-Write a contract where people can donate Ether and the top 3 donors are tracked.

5-Implement a simple auction system where users can place bids, and the highest bidder wins.

6-Create a contract that splits incoming Ether between 3 fixed addresses.

# **PRACTICAL 1**
# **Create a voting system with multiple candidates. Each address can vote only once.**
**Objective :**

Create and deploy a simple voting system in Solidity where:

Each voter can vote only once.

Each candidate has a vote count.

Users can view candidate details and vote count.

votingSystem.sol

        // SPDX-License-Identifier: MIT
        pragma solidity ^0.8.0;

       contract Voting {
             struct Candidate {
                  string name;
                  uint voteCount;
    }

    address public owner;
    mapping(address => bool) public hasVoted;
    Candidate[] public candidates;

    constructor(string[] memory candidateNames) {
        owner = msg.sender;
        for (uint i = 0; i < candidateNames.length; i++) {
            candidates.push(Candidate(candidateNames[i], 0));
        }
      }

    function vote(uint candidateIndex) public {
        require(!hasVoted[msg.sender], "You have already voted.");
        require(candidateIndex < candidates.length, "Invalid candidate.");
        hasVoted[msg.sender] = true;
        candidates[candidateIndex].voteCount++;
    }
}



     

![image](https://github.com/user-attachments/assets/d4039479-7f32-4f62-a971-48f29a350e31)
![image](https://github.com/user-attachments/assets/f38cbcd2-2146-4830-8116-29f9039b2b91)

# **Deployment & Testing Steps (in Remix)**

# Step 1: Setup Environment

Open Remix IDE

Create a new file votingSystem.sol and paste the code above.

Compile with Solidity compiler version 0.8.0 (or compatible).

Go to the Deploy & Run Transactions tab.

Set Environment to Remix VM (Prague).

![image](https://github.com/user-attachments/assets/d6fae800-cd4f-4dbd-b4dc-6f2ea8b2bde4)

# Step 2: Deploy Contract

In the Deploy section, enter candidate names as a string array:

    ["Tejasvi", "bob", "Taniya"]
    
Click Deploy.

![image](https://github.com/user-attachments/assets/aca619dc-3ba7-4036-a0cb-b068fb562c0f)

# Step 3: Interact With Contract

Check candidates:

Expand candidates public array.

Use indexes 1, 2, and 3 to view:

          name

          voteCount

 **Vote:**

In the vote function, enter a candidate index (e.g., 2 for Charlie).

Click transact.
![image](https://github.com/user-attachments/assets/6f186cae-f69c-4372-b3ba-7ffd490fa5b5)

# OUTPUT 
![image](https://github.com/user-attachments/assets/eff48137-1349-4bb1-81a4-304277828509)
![image](https://github.com/user-attachments/assets/1bba8d2a-b086-4458-9cf5-38a09141570d)
![image](https://github.com/user-attachments/assets/ed44de0f-0f43-40c4-9d58-77cc38855757)
![image](https://github.com/user-attachments/assets/f1965c1b-ed42-4995-8673-f009365af7ff)
![image](https://github.com/user-attachments/assets/40315d4f-f7b3-436d-b2b8-0cdde291c829)
![image](https://github.com/user-attachments/assets/1e017933-49f6-431f-8655-a263cd7f4ca3)
![image](https://github.com/user-attachments/assets/b38f7616-e2c5-49d0-a25b-e9a743fec11b)
![image](https://github.com/user-attachments/assets/76b1f73d-0f76-4423-a73b-5a84e7e57627)
![image](https://github.com/user-attachments/assets/9f4e0367-68ba-4650-bf30-d6656e0516b8)


# **Practical 2 : Student records** 
# **Write a contract that manages a list of student records (name, roll number). Allow adding and retrieving student data.**
**code: StudentRecords.sol**


    // SPDX-License-Identifier: MIT
      pragma solidity ^0.8.0;

     contract StudentRecords {
    
    // Define a structure to hold student details
    struct Student {
        string name;
        uint rollNumber;
    }

    // Dynamic array to store student records
    Student[] private students;

    // Function to add a new student
    function addStudent(string memory _name, uint _rollNumber) public {
        students.push(Student(_name, _rollNumber));
    }

    // Function to get student details by index
    function getStudent(uint index) public view returns (string memory, uint) {
        require(index < students.length, "Student index out of bounds");
        Student memory s = students[index];
        return (s.name, s.rollNumber);
    }

    // Optional: Get total number of students
    function getStudentCount() public view returns (uint) {
        return students.length;
     }
   }


 ![image](https://github.com/user-attachments/assets/e2ab6e37-8072-43be-a3a7-5c42d09b2d0e)
 ![image](https://github.com/user-attachments/assets/c1f73643-07ac-477f-8636-8d48937cb9e7)

# STEPS

**How to Test in Remix**

Paste the code in a new file: StudentRecords.sol.

Compile with Solidity ^0.8.0.

Deploy the contract.

Use addStudent("Alice", 101) and addStudent("Bob", 102).

Call getStudent(0) and getStudent(1) to retrieve data.

Use getStudentCount() to check the total number of students added.


![image](https://github.com/user-attachments/assets/78150f68-e6a5-4c0c-ae6a-e193f7fe12f4)

![image](https://github.com/user-attachments/assets/236b05a5-8b8f-4590-8009-948ff88cb0c7)


# Output


![image](https://github.com/user-attachments/assets/4002552e-b50d-441f-8da4-f979b3b3968f)

![image](https://github.com/user-attachments/assets/a9a7d91f-850e-44cc-a8a9-df283b96f333)

![image](https://github.com/user-attachments/assets/baf80fd0-0c86-416b-8e40-5fd8ab4bfcc7)

![image](https://github.com/user-attachments/assets/7e62ec07-6ca4-4bda-b0f1-665bbaa080fa)

![image](https://github.com/user-attachments/assets/ea794423-b477-4b86-b1ce-31758a34653b)

![image](https://github.com/user-attachments/assets/95f8b2c7-7f83-401a-a2d1-928517cb1715)

# **Practical 3: OwnerRestricted**
# **Develop a contract that only allows the deployer (owner) to call a specific function (use modifiers).**
**Code: OwnerRestricted.sol**

      // SPDX-License-Identifier: MIT
        pragma solidity ^0.8.0;
  
        contract OwnerRestricted {
            address public owner;

    // Set the deployer as the owner when the contract is deployed
    constructor() {
        owner = msg.sender;
    }

    // Modifier that allows only the owner to execute a function
    modifier onlyOwner() {
        require(msg.sender == owner, "Not the contract owner");
        _;
    }

    // Example function that only the owner can call
    function secretFunction() public onlyOwner returns (string memory) {
        return "This is a secret only for the owner!";
    }

    // Anyone can call this function
    function publicFunction() public pure returns (string memory) {
        return "This is a public function";
     }
    }

![image](https://github.com/user-attachments/assets/cc7c5e3a-5bc1-43f6-a80a-4bfd68261077)

# STEPS
**How to Test in Remix**

Paste the code into a new file OwnerRestricted.sol.

Compile the contract.

Deploy using an account (this account becomes the owner).

Call secretFunction() – it should succeed.

Change the account (top-left in Remix) and call secretFunction() again – it should fail with: Not the contract owner.

![image](https://github.com/user-attachments/assets/5f9ff87d-d39d-43a4-9b31-c04f8bdb4e6a)
![image](https://github.com/user-attachments/assets/91a1cd95-3863-42fc-bdd8-4772e5005408)



# OUTPUT
![image](https://github.com/user-attachments/assets/4c0e2a91-55aa-4766-9562-74bde8f41efe)
