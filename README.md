
# Module-20-Challenge - Develop Joint Savings Account Using Solidity on a Cross-Border Ethereum Blockchain
A fintech startup company is disrupting the finance industry with its own cross-border, Ethereum-compatible blockchain that connects financial institutions building smart contracts to automate many of the institutions’ financial processes and features, such as hosting joint savings accounts.

--- 
---
## User Story
As a Fintech developer you have been asked to automate the creation of joint savings accounts that accepts two user addresses. These addresses will be able to control a joint savings account. Your smart contract will use ether management functions to implement the requirements for providing the features of the joint savings account. These features will consist of the ability to deposit and withdraw funds from the account.

The Starter Code was provided to expedite the development process. Remix IDE is used for the development and testing.

---
---
## Acceptance Criteria  

Create and work within a local blockchain development environment using the JavaScript VM provided by the Remix IDE. 

* The `Starter Code` for the application must be modified to design a **smart contract** called **JointSavings** with the following functions
    * withdraw
    * deposit
    * setAccounts
    * fallback deposit function

* Deploy the smart contract to transfer and withdraw funds

---
---
## The Application

The Starter code for the **JointSavings smart contract** was modified in `Remix IDE` with the following functions:
* withdraw  
    - use `require` function to check for the account validity and display message if invalid.
    - use `require` function to check if sufficient balance exists for the withdrawl, display a message if not.
    - withdraw using `address.transfer` function, only after verifying account valididty and upon sufficient balance.
    - update the state variables holding `lastToWithdraw`, `lastWithdrawAmount` and `contractBalance`.
* deposit  
    - update the `contractBalance` state variable from the contract balance extracted from `address(this).balance`.
* setAccounts  
    - enable accepting the two account addresses for the joint account, and update the corresponding state variables `accountOne` and `accountTwo` respectively.
* fallback deposit function  
    - define the fallback function using `external payable` to accept payments received from outside of the `deposit` function.


## Installation Guide

### Clone the application code from Github as follows:
copy the URL link of the application from its Github repository      
open the Terminal window and clone as follows:  

   1. %cd to_your_preferred_directory_where_you want_to_store_this_application  
    
   2. %git clone URL_link_that_was_copied_in_step_1_above   
    
   3. %ls       
        Module-20    
        
   4. %cd Module-20   

The entire application files in the current directory are as follows:

* execution_results              (screenshots used in README)
    - after_deposit_eth_1.png
    - click_on_compile.png
    - compile_success.png
    - compile.png
    - deploy.png
    - deployed_contract.png
    - deposit_eth_1.png
    - deposit_eth_5.png
    - deposit_eth_10.png
    - remix_main.png
    - select_joint_savings.png
    - set_addresses.png
    - withdraw_5_eth_acct_1.png
    - withdraw_10_eth_acct_2.png
    - withdrawl_insuff_funds.png
* joint_savings.sol             (solidity contract)
* README.md                     (this file.. you are reading)
* Starter_Code                  (Starter Code)
    - joint_savings.sol         (starter code)

---
---

## Deploy the JointSavings smart contract to Transfer and Withdraw funds
The **JointSavings** contract was deployed using Remix IDE. The contract is defined in the file named `joint_savings.sol`, installed above.
* Invoke [Remix IDE - https://remix.ethereum.org/](https://remix.ethereum.org/) on your web browser like `Chrome`.  
* Use `Open Files` in the **File** section to navigate to `joint_savings.sol`
* [click on `joint_savings.sol`](execution_results/remix_main.png) to compile and run
      
### Compile and Deploy the JointSavings Contract

* [Click on the image just top-left of Solidity Compiler text (looks like recycle sign)](execution_results/compile.png) to compile the contract. Look at the [Green checkmark](execution_results/compile_success.png)  for success!
* Click on the image just below the `solidity compiler` button to navigate to the [Deploy & Run Transactions](execution_results/deploy.png) pane, and make sure that “Remix VM (London)” is selected as the environment.
* Click the `Deploy` button to deploy your smart contract, and then confirm that it [successfully deployed](execution_results/deployed_contract.png).

### Interact with the Deployed JointSavings Contract
* Use the `setAccounts` function to define the authorized Ethereum address that will be able to withdraw funds from your contract.

>NOTE
You can either use the following Ethereum addresses or create new, dummy addresses on the Vanity-ETH (Links to an external site.) website, which includes an Ethereum vanity address generator.

>Dummy account1 address: 0x0c0669Cd5e60a6F4b8ce437E4a4A007093D368Cb
>Dummy account2 address: 0x7A1f3dFAa0a4a19844B606CD6e91d693083B12c0  

* [We used the above addresses.](execution_results/set_addresses.png) 

* Test the deposit functionality of your smart contract by sending the following amounts of ether. After each transaction, use the `contractBalance` variable to verify that the funds were added to your contract:

    - Transaction 1: [Send 1 ether as wei](execution_results/after_deposit_eth_1.png)
    - Transaction 2: [Send 10 ether as wei](execution_results/deposit_eth_10.png)
    - Transaction 3: [Send 5 ether as wei](execution_results/deposit_eth_5.png)
>NOTE
Remembering how to convert ether to wei and vice versa can be challenging. So, you can use a website like [Ethereum Unit Converter](https://eth-converter.com/) to ease doing the conversion.

* Once you’ve successfully deposited funds into your contract, test the contract’s withdrawal functionality by withdrawing:  

    - [5 ether into accountOne](execution_results/withdraw_5_eth_acct_1.png) 
    - [10 ether into accountTwo](execution_results/withdraw_10_eth_acct_2.png) 
    - [7 ether and check for insufficient funds](execution_results/withdrawl_insuff_funds.png)
    
You can review `contractBalance`, `lastToWithdraw` and `lastWithdrawAmount` variables to verify that the transaction accuracy in the screenshots above.

---
---

## Technologies
The application is developed using:  
* Language: Solidity  
* Development Environment: VS Code and Terminal
* OS: Mac OS 12.1

---
---

## Contributors 
Ashok Pandey - ashok.pragati@gmail.com, www.linkedin.com/in/ashok-pandey-a7201237  

---
---

## License
The source code is the property of the developer. The users can copy and use the code freely but the developer is not responsible for any liability arising out of the code and its derivatives.

---
---
