# CrafterToken
A simple token smart contract implemented in solidity to meet the following requirements.

##### REQUIREMENTS
    1. The contract has public variables that store the details about the coin (Token Name, Token Abbrv., Total Supply)
    2. It has a mapping of addresses to balances (address => uint)
    3. It has a mint function that takes two parameters: an address and a value. 
       The function then increases the total supply by that number and increases the balance 
       of the “sender” address by that amount
    4. It has a burn function, which works the opposite of the mint function, as it will destroy tokens. 
       It will take an address and value just like the mint functions. It will then deduct the value from the total supply 
       and from the balance of the “sender”.
    5. Lastly, the burn function has conditionals to make sure the balance of "sender" is greater than or equal 
       to the amount that is supposed to be burned.
