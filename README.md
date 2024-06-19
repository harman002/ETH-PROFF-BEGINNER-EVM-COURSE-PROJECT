# Project Title

ETH Proff Beginner Course Under Solidity:
Create a Token

# Discription

ETH Proof Beginners EVM course project.First of all I created contract named myToken and inside of that i create public variables to store coin details, map addresses to balances, and implement functions like mint and burn and handle increasing total supply and managing balances effectively!
# Functionality
Created a contract Named myToken and then i created public variables to store coin details like tokenName,tokenAbbrv and assign both of them with some Strings totalSuppply with values 0 the i used mapping to map the variables(address into uint(unsigned Integers)) This address will Contain the value of token
then Created two Functions named mint and burn which takes two parameters named address and values. We will add this value to totalSupply Simply we can say that we are increasing the value of totalSupply then we will add this Value in the given address
Code we will Update the balance of that address burn function is doing the same thing inside of burn function we created a if statement and this if statement check that the balance of the given address is greater then or equal to the given value if the balance is less than the given value then it does not do nothing means it has no enough value
if the condition satisfies that it decrease the value from that address and totalSupply
# Code
// SPDX-License-Identifier: MIT
pragma solidity 0.8.26;
contract myToken{
    string public tokenName="Harman";
    string public tokenAbbrv="Mna";
    uint public totalSupply=0;

    mapping(address => uint) public balance;

    function mint(address _address, uint _value)public{
        totalSupply +=_value;
        balance[_address]+=_value;
    }

    function burn(address _address, uint128 _value)public{
        if(balance[_address]>= _value){
           totalSupply -= _value;
           balance[_address] -= _value;
        }
    }
}
# Author
 Harmandeep Singh

 mail:harmandeep7448@icloud.com
