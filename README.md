# python-blockchain
Example of a simple blockchain implemented in Python

This is a simple implementation of a blockchain, it includes basic functionalities such as adding blocks, checking if the chain is valid, and performing a proof of work.

This example uses the hashlib library to create SHA-256 hashes, which are used to secure the transactions in the blockchain. The json library is used to encode and decode the blocks as they are added to and read from the chain.

The code above creates a Python class called Blockchain, which is used to represent the blockchain data structure.

The __init__ method is called when an instance of the Blockchain class is created. It initializes an empty list called chain that will store the blocks in the blockchain. It also creates the first block, called the "genesis block", with an index of 1, a timestamp of the current time, a proof of 1, and a previous hash of 0.

The create_block method is used to add new blocks to the blockchain. It takes in two arguments, proof and previous_hash, and creates a new block dictionary with these values as well as the index and timestamp. The new block is then appended to the chain list.

The get_previous_block method returns the last block in the chain list, which is used to reference the previous block when adding a new block.

The proof_of_work method is used to perform a proof of work algorithm on the blockchain. This is a consensus algorithm that is used to secure the blockchain and prevent against attacks such as the double-spending problem. In this example, the proof of work is a simple algorithm that repeatedly increments a number, called new_proof, and checks to see if the hash of the new_proof squared minus the previous proof squared starts with four zeros.

The hash method takes in a block and uses the json library to convert it to a json object, then it uses the hashlib library to create a SHA-256 hash of the encoded block and returns the hexadecimal representation of the hash.

The is_chain_valid method is used to validate the blockchain by checking if the previous_hash of each block is equal to the hash of the previous block, and if the proof of work algorithm has been properly solved.

This is a simple implementation of a blockchain, it includes basic functionalities such as adding blocks, checking if the chain is valid, and performing a proof of work. Remember that this is just an example and it is not suitable for production use.
