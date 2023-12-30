# Electricity Bill 

## Overview

This Solidity smart contract, named `ElectricityBill`, is designed to manage and process electricity bills for customers. The contract allows the owner to generate bills for customers based on the consumed units and provides a method for customers to pay their bills.

## Features

1. **Bill Generation**: The contract owner can generate electricity bills for customers by providing the customer's address and the number of consumed units. The bill amount is calculated based on a fixed rate per kilowatt-hour.

2. **Payment Handling**: Customers can pay their bills by calling the `payBill` function. The payment process is restricted to the contract owner to ensure that only authorized entities can process payments. If the payment amount exceeds the unpaid bill, the excess amount is refunded to the payer.

3. **Owner Access Control**: The contract includes a modifier `onlyOwner`, ensuring that certain functions can only be executed by the contract owner. This adds a layer of security and control over critical operations.

## Contract Structure

- **State Variables**:
  - `owner`: The address of the contract owner.
  - `unpaidBills`: A mapping of customer addresses to their respective unpaid bill amounts.

- **Modifiers**:
  - `onlyOwner`: Ensures that only the contract owner can execute certain functions.

- **Constructor**:
  - Sets the contract owner to the address that deployed the contract.

- **Functions**:
  - `payBill`: Allows the contract owner to process bill payments. The payment amount should cover the entire unpaid bill, and any excess amount is refunded.
  - `generateBill`: Generates electricity bills for customers based on consumed units. It includes validations for consumed units and bill amount.

## Usage

1. Deploy the contract to the Ethereum blockchain.

2. Set the electricity rate per kilowatt-hour by modifying the `rate` variable in the `generateBill` function.

3. Call the `generateBill` function to create bills for customers, specifying the customer's address and consumed units.

4. Customers can call the `payBill` function to pay their bills. The payment should be made by the contract owner.


## License
This smart contract is released under the MIT License. See the SPDX-License-Identifier in the source code for more details.

## Author

Harsha k varma

krishkat99@gmail.com
