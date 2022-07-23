# ether_joint_savings
## Using an etherium blockchain to create a joint savings account for two blockchain wallets.

A fintech startup company has recently hired you. This company is disrupting the finance industry with its own cross-border, Ethereum-compatible blockchain that connects financial institutions. Currently, the team is building smart contracts to automate many of the institutions’ financial processes and features, such as hosting joint savings accounts.

To automate the creation of joint savings accounts, you’ll create a Solidity smart contract that accepts two user addresses. These addresses will be able to control a joint savings account. Your smart contract will use ether management functions to implement a financial institution’s requirements for providing the features of the joint savings account. These features will consist of the ability to deposit and withdraw funds from the account.

## Development

The development of the smart contract went pretty smoothly. First I created the contract and contract variables. Then I created public functions that the account owners could use to transact ether (wei) to and from the contract which acts as their joint savings account. I created a withdraw function, a deposit function, and a setter function to set up the accounts. Finally I included a fallback function which would pay back all parties in the case that incorrect parameters are set and the ether needs to be returned to its sender.

## Development issues

One part of the code that was challenging was creating a require function with two possible correct variables. The incorrect syntax I attempted was :
![image](https://user-images.githubusercontent.com/99841428/180591497-7c5d63d8-ddd4-47a8-8edf-00a730f79649.png)
After a bit of googling, the correct syntax was:
![image](https://user-images.githubusercontent.com/99841428/180591555-c95b378b-6739-4674-8e64-a750e0ac3e03.png)

## Deployment

The contract deployed successfully:
![image](https://user-images.githubusercontent.com/99841428/180622058-4884cccf-0de3-4c55-887a-7b128d37ea0a.png)

## Execution Results

### Set Accounts Function
![image](https://user-images.githubusercontent.com/99841428/180622154-b7e2b838-9009-463f-8675-9c86005d007d.png)
![image](https://user-images.githubusercontent.com/99841428/180622162-226cf66c-02f0-4722-8a35-a58e077dd12c.png)

### Deposit Function
Send one ether as wei
![image](https://user-images.githubusercontent.com/99841428/180622200-63f07162-2006-4278-9106-2745008e7efc.png)

Send 10 ether as wei
![image](https://user-images.githubusercontent.com/99841428/180622229-193f88ad-4a86-4b9f-bd54-536555e423f3.png)

Send 5 ether as ether
![image](https://user-images.githubusercontent.com/99841428/180622258-adc61d9c-9358-4602-98ed-c9698b0b4d94.png)

### Testing the Withdraw Function
Sending 5 ether to account one
![image](https://user-images.githubusercontent.com/99841428/180622315-34aba58f-8f95-4491-a4bd-3fbaaeb3a06c.png)

Sending 10 ether to account two
![image](https://user-images.githubusercontent.com/99841428/180622338-aaedf4bd-b45e-4a63-9241-44f8d77fa52c.png)

Calling the lastToWithdraw and lastToWithdrawAmount variables to see the balance of the account
![image](https://user-images.githubusercontent.com/99841428/180622368-1517f696-65f5-4bb9-a00d-8fdc4f4db30d.png)

