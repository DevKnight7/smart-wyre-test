# Smartwyre Developer Test - Solution

This is a solution for the Smartwyre Developer Test. The task involves refactoring the code in `RebateService.cs` to improve adherence to SOLID principles, testability, and readability. Additionally, unit tests are to be added to the `Smartwyre.DeveloperTest.Tests` project, and the `RebateService` should be executed from the `Smartwyre.DeveloperTest.Runner` console application accepting inputs.

## Refactoring

The code in `RebateService.cs` has been refactored with the following changes:

- Introduced constructor injection for `RebateDataStore` and `ProductDataStore` dependencies, enabling easier testing and decoupling from concrete implementations.
- Extracted the calculation logic for different incentive types into separate methods, improving code organization and readability.
- Added validation checks for null rebate or product objects and handled the failure case appropriately.
- Implemented the `IRebateService` interface to ensure adherence to SOLID principles.

## Testability

To improve testability, the following changes were made:

- Introduced interfaces (`IRebateDataStore` and `IProductDataStore`) to abstract the dependencies on `RebateDataStore` and `ProductDataStore` respectively.
- Implemented the interfaces in `RebateDataStore` and `ProductDataStore`.
- Created an instance of `RebateService` in the test project with mock instances of the interfaces for testing purposes.

## Readability

The code was refactored to improve readability using the following techniques:

- Meaningful variable and method naming.
- Proper indentation and formatting for improved code structure.
- Removal of unnecessary comments and redundant code to reduce clutter and increase code clarity.

## Running the Solution

To run the solution and execute the `RebateService` from the `Smartwyre.DeveloperTest.Runner` console application:

1. Build the solution using your preferred development environment or by running the appropriate build command.
2. Run the `Smartwyre.DeveloperTest.Runner` project, which launches the console application.
3. Follow the prompts in the console to provide the necessary inputs for rebate calculation.

## Testing the Solution

Unit tests have been added to the `Smartwyre.DeveloperTest.Tests` project to verify the functionality of the `RebateService` class. The tests cover various scenarios and ensure that the rebates are calculated correctly and that the service behaves as expected.

To run the tests:

1. Build the solution.
2. Open the Test Explorer in your preferred test runner or IDE.
3. Run all the tests in the `Smartwyre.DeveloperTest.Tests` project.
4. Ensure that all tests pass successfully.

The tests cover the following scenarios:

- Valid product and rebate identifiers return the expected product and rebate objects respectively.
- Invalid product and rebate identifiers return null objects.
- Rebate calculation for different incentive types returns the expected results.
- Invalid rebate calculation returns a failure result.

The tests validate the correctness and accuracy of the rebate calculations performed by the `RebateService` class.