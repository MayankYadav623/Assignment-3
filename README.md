# Assignment-3
Solidity 

// SPDX-License-Identifier: MIT pragma solidity ^0.8.0;

/* Solidity Smart Contract Tutorial - HelloWorld Example

Development Steps:

SETUP ENVIRONMENT:

Open https://remix.ethereum.org in browserNo installation required

CREATE CONTRACT FILE:

Click "File Explorer" icon (left sidebar)Click "+" button to create new fileName it "HelloWorld.sol"

WRITE CONTRACT CODE:

Copy and paste this entire fileOr type the contract code below

COMPILE:

Click "Solidity Compiler" icon (3rd icon)Select compiler version 0.8.0+Click "Compile HelloWorld.sol"

DEPLOY:

Click "Deploy & Run" icon (4th icon)Select "JavaScript VM" environmentClick orange "Deploy" button

INTERACT:

Under "Deployed Contracts": a. Click "greeting" to view current message b. Type new message in "updateGreeting" field c. Click "transact" to update (owner only) */

contract HelloWorld { string public greeting; address public owner;

constructor() { greeting = "Hello Web3 World!"; owner = msg.sender; } function updateGreeting(string memory newGreeting) public { require(msg.sender == owner, "Only owner can update greeting"); greeting = newGreeting; } /* CUSTOMIZATION OPTIONS: 1. Change initial greeting in constructor 2. Rename contract (HelloWorld) 3. Modify function names (updateGreeting) 4. Add new functions as needed SECURITY OPTIONS: 1. Implement time-locks for changes 2. Add multi-signature requirements 3. Create upgradeability pattern NEXT STEPS: 1. Add event emissions for tracking 2. Write unit tests in JavaScript 3. Deploy to Ethereum testnet */ 

}

