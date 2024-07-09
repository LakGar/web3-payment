#Web3 Payment
This project is a decentralized payment system built on the Ethereum blockchain using Solidity and Hardhat. It allows users to create payment requests, pay requests, and keep a transaction history, similar to PayPal but on a decentralized platform.

Features
Add Name to Wallet Address: Users can associate their wallet address with a name.
Create Payment Requests: Users can request payments from other users.
Pay Requests: Users can pay requests made to them.
Transaction History: Users can view their transaction history.
Installation
Clone the repository:

bash
Copy code
git clone https://github.com/LakGar/web3-payment.git
cd web3-payment
Install Dependencies:

bash
Copy code
npm install
Usage
Compile the Smart Contract:

bash
Copy code
npx hardhat compile
Deploy the Smart Contract:

bash
Copy code
npx hardhat run scripts/deploy.js --network localhost
Run Tests:

bash
Copy code
npx hardhat test
Start Hardhat Node:

bash
Copy code
npx hardhat node
Contract Overview
Functions
addName(string memory _name): Adds a name to the sender's wallet address.
createRequest(address user, uint256 _amount, string memory _message): Creates a payment request to a specified user.
payRequest(uint256 _request) public payable: Pays a specified request.
getMyRequests(address _user) public view returns (address[], uint256[], string[], string[]): Retrieves all requests sent to a user.
getMyHistory(address _user) public view returns (sendReceive[]): Retrieves the transaction history of a user.
getMyName(address _user) public view returns (userName): Retrieves the name associated with a user's wallet address.
Contributing
Fork the repository
Create your feature branch (git checkout -b feature/your-feature)
Commit your changes (git commit -am 'Add some feature')
Push to the branch (git push origin feature/your-feature)
Create a new Pull Request
License
This project is licensed under the MIT License.
