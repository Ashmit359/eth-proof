Getting Started with Solidity

Problem Statement :

   REQUIREMENTS
1. Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
2. Your contract will have a mapping of addresses to balances (address => uint)
3. You will have a mint function that takes two parameters: an address and a value. 
   The function then increases the total supply by that number and increases the balance 
   of the “sender” address by that amount
4. Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. 
   It will take an address and value just like the mint functions. It will then deduct the value from the total supply 
   and from the balance of the “sender”.
5. Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal 
   to the amount that is supposed to be burned.


   Steps / Working :

Deployment : deploy it

![255328453-98fccae7-b5b3-4a98-b724-57878ae60f24](https://github.com/Ashmit359/eth-proof/assets/119657904/2ca6ca09-a99f-4ee7-a47d-df2e8d737cbc)

