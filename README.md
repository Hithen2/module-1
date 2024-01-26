# Newspaper Printing 

## Overview

This Solidity smart contract, named NewspaperPrinting, is designed to facilitate the printing of newspapers on a blockchain. It includes functions to print a new paper and check ink levels before printing copies. The contract is equipped with ink level tracking to ensure that printing operations do not exceed the available ink supply.

## Smart Contract Details

### Contract Variables

- `totalInk`: Represents the total amount of ink available in milliliters. It is initially set to 10 ml.

### Functions

1. **printNewspaper**

   - **Parameters**: 
     - `paperSize`: The size of the newspaper to be printed.
     - `hasCyan`, `hasMagenta`, `hasYellow`, `hasBlack`: Boolean parameters indicating the presence of each color in the printing process.

   - **Description**: 
     - Checks if the provided paper size is greater than 420, using an assert statement.
     - Requires the presence of all four colors (Cyan, Magenta, Yellow, Black) for successful printing.

2. **printCopies**

   - **Parameters**: 
     - `numberOfCopies`: The number of newspaper copies to be printed.

   - **Description**: 
     - Checks if there is sufficient ink to print the specified number of copies.
     - If the ink is insufficient, the function reverts with a warning message.
     - If there is enough ink, the specified number of copies is printed, and the total ink level is reduced accordingly.

## Usage Instructions

1. **Deploying the Contract**:
   - Deploy the NewspaperPrinting smart contract on a compatible Ethereum blockchain network, ensuring that the deployment account has enough gas and funds.

2. **Interacting with the Contract**:
   - Call the `printNewspaper` function to initiate the printing process, providing the required parameters.
   - Use the `printCopies` function to print a specified number of newspaper copies while checking for ink availability.

3. **Monitoring Ink Levels**:
   - Keep track of the `totalInk` variable to monitor the remaining ink supply. If the ink level is low, consider refilling the ink before initiating further printing operations.

## License

This smart contract is released under the MIT License. See the [LICENSE](./LICENSE) file for more details.

## Author 
srk
srkh5116@gmail.com
