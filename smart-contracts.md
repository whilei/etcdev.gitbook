---
description: Smart contracts are cool.
---

# Smart Contracts

### Creating a Basic Token

{% code-tabs %}
{% code-tabs-item title="contract.sol" %}
```text

pragma solidity ^0.4.20;

contract MyToken {
    /* This creates an array with all balances */
    mapping (address => uint256) public balanceOf;

    /* Initializes contract with initial supply tokens to the creator of the contract */
    function MyToken(
        uint256 initialSupply
        ) public {
        balanceOf[msg.sender] = initialSupply;              // Give the creator all initial tokens
    }

    /* Send coins */
    function transfer(address _to, uint256 _value) public {
        require(balanceOf[msg.sender] >= _value);           // Check if the sender has enough
        require(balanceOf[_to] + _value >= balanceOf[_to]); // Check for overflows
        balanceOf[msg.sender] -= _value;                    // Subtract from the sender
        balanceOf[_to] += _value;                           // Add the same to the recipient
    }
}
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% tabs %}
{% tab title="Geth" %}
```text
This is how to do it in Geth
```
{% endtab %}

{% tab title="Parity" %}
```text
This is how to do it in Parity
```
{% endtab %}
{% endtabs %}

