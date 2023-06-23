// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;


contract MyToken {
Step 1 : I created a variables using string to hold the values name,token, and total supply, i make it public.
    // public variables here
    string public tokenName = "PESO";
    string public tokenAbbrv = "PS";
    uint public totalSupply = 0;
Step 2 : Mapping is for to assiociate with the uint.
    // mapping variable here
    mapping (address => uint) public balances;
Step 3 : I created a function that will get the result of addition or summing up the total supply and value.
    // mint function
    function mint (address add, uint val)public {
        totalSupply += val;
        balances[add] += val;
    }
Step 4 : I created the burn function that will get the result of subraction of the total supply and the value i also add if statement so that the function can't burn more than value that we have.
    // burn function
       function burn (address add, uint val)public {
        if (balances[add] >= val){
         totalSupply -= val;
         balances[add] -= val;
        }
    }




}
