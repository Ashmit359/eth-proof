// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {
    string public name; // Token Name
    string public symbol; // Token Abbreviation
    uint256 public totalSupply; // Total Supply

    mapping(address => uint256) public balances;

    constructor(string memory _name, string memory _symbol, uint256 _totalSupply) {
        name = _name;
        symbol = _symbol;
        totalSupply = _totalSupply;
        balances[msg.sender] = _totalSupply;
    }

    function mint(address _receiver, uint256 _value) public {
        require(_value > 0, "Mint value must be greater than zero");
        totalSupply += _value;
        balances[_receiver] += _value;
    }

    function burn(address _sender, uint256 _value) public {
        require(balances[_sender] >= _value, "Insufficient balance to burn");
        require(_value > 0, "Burn value must be greater than zero");
        totalSupply -= _value;
        balances[_sender] -= _value;
    }
}
