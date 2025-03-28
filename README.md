// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract SimpleStorage {
    // Variable to store a number
    uint256 private storedValue;
    
    // Event to track changes
    event ValueChanged(uint256 newValue);
    
    // Constructor setting initial value
    constructor(uint256 initialValue) {
        storedValue = initialValue;
        emit ValueChanged(initialValue);
    }
    
    // Function to set a new value
    function setValue(uint256 newValue) public {
        storedValue = newValue;
        emit ValueChanged(newValue);
    }
    
    // Function to get the current value
    function getValue() public view returns (uint256) {
        return storedValue;
    }
}
