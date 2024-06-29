Message System

This whole stack code is designed to provide appropriate message exchanges among various organizational entities. Using the university as an example, the HOD may send messages to the faculty, faculty to the Hods, faculty to the Hods, and Hod to the Hods.




Description

Smart contract part

This contract is written in Solidity language, a programming language used for developing smart contracts on the Ethereum blockchain. In smart contract first we have enum Designation which will tell the designation of the members. members is a state variable to store the designation of members. addMember() adds a member with its designation. upMessage() can only called by faculities to send message to hod and downMessage() can be called by hod only to send message to faculities. horizontalMessage() can be called by both but to send message to the same level no hierarchical level. deleteMember() will delete the existing member.

Front end part

index.html and styles.css is used to create and design the structure and look of the front end and script.js is used for the logic purpose. In js file we have contract address, abi. Using this with ethers.js we get create the provider, signer and contract. then connect() is used to connect the wallet. and rest all the functions are connected with the solidity functions. checkMember() is used to get the designation of the member from blockchain and getDesignationName() provides the name of the designation for its integer value.
