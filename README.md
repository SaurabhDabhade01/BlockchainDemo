Installation
Clone the Repository

sh
Copy code
git clone https://github.com/yourusername/blockchain-simulation.git
Navigate to the Project Directory

sh
Copy code
cd blockchain-simulation
Install Dependencies

This project requires Python 3.11.7. You can install the required libraries using:

sh
Copy code
pip install -r requirements.txt
Note: requirements.txt should list any additional Python libraries if there are any.

Usage
Run the Simulation

To start the blockchain simulation, simply run:

sh
Copy code
python blockchain_simulation.py
Functionality

Transaction Generation: Transactions are generated and validated to ensure they conform to the rules.
Block Creation: Blocks are created and appended to the blockchain after validating the transactions.
Chain Validation: The chain is checked for validity including transactions, block hashes, and linkages between blocks.
Functions
hashMe(msg=""): Generates a SHA-256 hash of the given message.
makeTransaction(maxValue=3): Creates a transaction with random amounts for Alice and Bob.
updateState(txn, state): Updates the state dictionary based on the given transaction.
isValidTxn(txn, state): Validates a transaction to ensure it is balanced and does not cause an overdraft.
makeBlock(txns, chain): Creates a new block with the given transactions and appends it to the chain.
checkBlockHash(block): Validates that the block’s hash matches its contents.
checkBlockValidity(block, parent, state): Validates the block including transactions, hash, and parent linkage.
checkChain(chain): Validates the entire chain for correctness.
Example
Here’s an example of how the simulation progresses:

Initial State:

python
Copy code
state = {'Alice': 50, 'Bob': 50}
Create Transactions and Blocks:

The simulation will create transactions, validate them, and then create blocks to append to the chain.

Check Chain Validity:

python
Copy code
checkChain(chain)
