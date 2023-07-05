# SOLIDITY

Solidity is a high-level programming language primarily used for developing smart contracts on blockchain platforms, with Ethereum being the most prominent one. It is designed to enable the creation of decentralized applications (dApps) and execute complex logic on the blockchain

## Description

Solidity is a powerful programming language for developing smart contracts on the Ethereum blockchain. Its rich feature set, compatibility with the Ethereum ecosystem, and focus on security make it a popular choice for creating decentralized applications and implementing trustless business logic

## Getting Started



### Executing program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyContract.sol). Copy and paste the following code into the file:
contract MyToken {

    // public variables here
    string public tokenName = "PESO";
    string public tokenAbbrv = "PS";
    uint public totalSupply = 0;

    // mapping variable here
    mapping (address => uint) public balances;

    // mint function
    function mint (address add, uint val)public {
        totalSupply += val;
        balances[add] += val;
    }

    // burn function
       function burn (address add, uint val)public {
        if (balances[add] >= val){
         totalSupply -= val;
         balances[add] -= val;
        }
    }

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile MyContract.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the "tokenName" function. Click on the "tokenName" contract in the left-hand sidebar, and then click on the "tokenName" function. Finally, click on the "transact" button to execute the function and retrieve the "PESO" message. Same procedure with the tokenAbbrv, you will get the result abbrevation "PS"
Then with the Mint and Burn function copy the account link to the address then input a value to mint or burn to get the total supply value.



}

## Authors

Gyllvdrakegelo
@https://twitter.com/Gyllvdrakegelo

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
