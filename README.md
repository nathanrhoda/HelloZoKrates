# HelloZoKrates
Implementing Succinct Zero-Knowledge proofs (zkSnarks) with ZoKrates in Remix

This repo will demonstrate making use of zokrates to generate a zero know proof and the steps involved in demonstrating it on remix

# For Remix
- Install zokrates plugin


# Steps

1. Create a fire up remix http://remix.ethereum.org/ and create a file to implement the algorithm for the proof (see main.zok)
2. After that compile using the zokarates plugin
3. After Compilation you should see root and target under the compute accordian Enter root and target values to test the algorithm 
4. Run setup to create the proofing key 
5. Export Verifier to generate the verifier solidity file
6. Navigate back to solidity compiler ensure the contract selected is the verifier that was created from Zokrates export
7. Compile the verifier solidity file
8. Navigate to Deploy tab in remix and select verifier contract if it is not already selected and deploy
9. Navigate back to zokrates plugin and generate proof
10. Copy the verifier inputs generated
11. Navigate back to deploy tab and paste verifier inputs
12. Select down arrow to reveal pasted inputs better 
13. Click call to test the proof    


Run Zokrates
1. docker run -v <path to your project folder>:/home/zokrates/code -ti zokrates/zokrates /bin/bash

Compile Zokrates program
2. /path/to/zokrates compile -i <program_name>.code

Generate the trusted setup
3. /path/to/zokrates setup

Compute Witness
4. /path/to/zokrates compute-witness -a <a> <b> ... <n>

Generate Proof
5. /path/to/zokrates generate-proof

Export Verifier
6. path/to/zokrates export-verifier
