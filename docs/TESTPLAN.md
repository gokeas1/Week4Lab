# Student Account System Test Plan

This test plan covers the business logic and implementation of the COBOL-based student account management system. It is designed to validate the application's behavior with business stakeholders and will serve as a basis for future unit and integration tests in the Node.js transformation.

| Test Case ID | Test Case Description                | Pre-conditions                | Test Steps                                                                 | Expected Result                                      | Actual Result | Status (Pass/Fail) | Comments |
|--------------|--------------------------------------|-------------------------------|----------------------------------------------------------------------------|------------------------------------------------------|---------------|--------------------|----------|
| TC-01        | View initial account balance         | Application is started        | 1. Start app<br>2. Select 'View Balance' (option 1)                        | Balance displayed as 1000.00                         |               |                    |          |
| TC-02        | Credit account with valid amount     | Application is started        | 1. Start app<br>2. Select 'Credit Account' (option 2)<br>3. Enter 200.00   | Balance increases by 200.00; new balance shown       |               |                    |          |
| TC-03        | Debit account with sufficient funds  | Account balance >= debit amt  | 1. Start app<br>2. Select 'Debit Account' (option 3)<br>3. Enter 100.00   | Balance decreases by 100.00; new balance shown       |               |                    |          |
| TC-04        | Debit account with insufficient funds| Account balance < debit amt   | 1. Start app<br>2. Select 'Debit Account' (option 3)<br>3. Enter 2000.00  | Error: 'Insufficient funds for this debit.'          |               |                    |          |
| TC-05        | Credit account with zero amount      | Application is started        | 1. Start app<br>2. Select 'Credit Account' (option 2)<br>3. Enter 0.00    | Balance remains unchanged; new balance shown         |               |                    |          |
| TC-06        | Debit account with zero amount       | Application is started        | 1. Start app<br>2. Select 'Debit Account' (option 3)<br>3. Enter 0.00    | Balance remains unchanged; new balance shown         |               |                    |          |
| TC-07        | Exit application                     | Application is started        | 1. Start app<br>2. Select 'Exit' (option 4)                                 | Program displays goodbye message and terminates       |               |                    |          |
| TC-08        | Invalid menu option                  | Application is started        | 1. Start app<br>2. Enter invalid option (e.g., 5 or letter)                | Error: 'Invalid choice, please select 1-4.'           |               |                    |          |
| TC-09        | Multiple sequential operations       | Application is started        | 1. Start app<br>2. Credit 100.00<br>3. Debit 50.00<br>4. View Balance      | Balance reflects all operations correctly             |               |                    |          |

> **Note:** Actual Result, Status, and Comments are to be filled during test execution.
