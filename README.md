# Building and Deploying a Decentralised Voting System with PyTeal and React
![Frame 27](https://user-images.githubusercontent.com/23031920/157607141-556aceb3-1357-4117-9cc9-6f43c91a0eb5.jpeg)


The business value of this tutorial is to teach how to write a smart contract code with PyTeal and Deploy using the Algorand JavaScript SDK and React on the Frontend to interact with the application.

The goal of the voting smart contract is to enable voters vote for their candidate of choice from a list of candidates.And the votes will be stored globally on the Algorand blockchain.

The voting system allows accounts to register and vote for arbitrary choices. Here a choice is any byte slice and anyone is allowed to register to vote.

This tutorial has a configurable registration period defined by the global state Registration Begin and Registration End which restrict when accounts can register to vote. There is also a separate configurable voting period defined by the global state Voting Begin and Voting End which restrict when voting can take place. But for the purpose of testing/demo the registration and voting period will be left open.

An account must register in order to vote. Accounts cannot vote more than once. The results are visible in the global state of the application, and the winner is the candidate with the highest number of votes.


## PyTeal Smart Contract
PyTeal is a python library for generating TEAL programs that provides a convenient and familiar syntax.
This handles building of the smart contract with PyTeal. The smart contract code can be found in `src/contract.py`

## TEAL
TEAL is Transaction Execution Approval Language. PyTeal code will be compiled to TEAL. The TEAL code consist of the Approval Program and Clear State Program.
The Approval program can be found in `src/contract/vote_approval.teal` and the Clear State Program can be found in `src/contract/vote_clear_state.teal`

## Frontend Interactions with React
To interact with the application the UI code can be found in `src/components`

## AlgoSigner
- The AlgoSigner will be used for signing the transactions on the demo app.

## Deploy Smart Contract with the Algorand JavaScript SDK
The JavaScript SDK will be used for deploying the smart contract code.

# Setup Requirements
- [Algorand JavaScript SDK](https://github.com/algorand/js-algorand-sdk)
- [Vs Code](https://code.visualstudio.com/) or any IDE of your choice
- [Node Package Manager](https://nodejs.org/download/)
- [Create React App](https://github.com/facebook/create-react-app) . This creates a react boilerplate app.
- [Styled Components](https://styled-components.com/)
- [Python 3.6 or higher](https://www.python.org/downloads/)
- [Pyteal Installation](https://pyteal.readthedocs.io/en/stable/installation.html)

## Run the Code
To test the code 
- Clone this repository
- Make account on Purestake API
- Copy API key to env file
- Install Algosigner web extension
- create testnet account
- Save credentials
- Fund that ^ account on Algorand faucet
- . venv/bin/activate
- python3 contract/contract.py
- deactivate
- npm start
- connect wallet, regiser, sign with AlgoSigner, set vote
# Demo
<img width="1440" alt="Screenshot 2022-03-16 at 03 14 24" src="https://user-images.githubusercontent.com/23031920/158504411-bb1eef56-0bdb-4f6c-881c-875294b2976a.png">

Here is a [demo link](https://votingdapp.vercel.app/) to the deployed Application on vercel.

# License
Distributed under the MIT License. See for more information. [LICENSE](https://github.com/gconnect/voting-dapp-pyteal-react/blob/master/LICENSE)

# Blog and Video Tutorial
For more details you can checkout the blog post [here](https://developer.algorand.org/tutorials/building-and-deploying-voting-smart-contract-with-pyteal-and-react/) . And here is the link to the [youtube demo](https://youtu.be/RWpB7p0Aas0)

# Disclaimer

# Warning
This project is not audited and should not be used in a production environment.





