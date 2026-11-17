# CP-057 ClaimFlow: Multi-Level Expense Approval Workflow Engine

## Team
vinaykumar Talawar (1AT25EC427), Mehataab D S (1AT24EC083), C Track

## How to run

bash
gcc ClaimFlow.c -o ClaimFlow.exe
./ClaimFlow.exe


## Features that work

1. *Submit an Expense Claim:* Employees can submit expense claims by entering their Employee ID, Name, Expense Category, Amount, Date, and Receipt Availability.

2. *Category Limit Validation:* Automatically checks submitted claims against predefined expense category limits and flags claims that exceed the allowed limits.

3. *Multi-Level Approval Workflow:* Routes claims based on the approval threshold:
   - Claims up to ₹10,000 require Manager approval only.
   - Claims above ₹10,000 require both Manager and Finance approval.

4. *Claim Status Tracking:* Tracks the approval progress of every claim, including Pending Manager Approval, Pending Finance Approval, Approved, and Rejected.

5. *Policy Violation Reports:* Generates reports identifying claims that exceed predefined category limits, including employee details, claim amount, and permitted category limit.

6. *Employee-Wise Reimbursement Reports:* Calculates and displays the total approved reimbursement amount for each employee.

7. *Overall Claim Summary:* Displays total submitted claims, approved claims, rejected claims, pending claims, and total approved reimbursement.

8. *Display All Claims:* Provides an overview of all submitted expense claims and their current approval statuses.

## Sample run

text
========================================
       CLAIMFLOW WORKFLOW ENGINE
  Multi-Level Expense Approval System
========================================

============== MAIN MENU ==============
1. Submit Expense Claim
2. Manager Approval
3. Finance Approval
4. Track Claim Status
5. Generate Reports
6. Display All Claims
0. Exit

Enter your choice: 1

========== SUBMIT EXPENSE CLAIM ==========
Enter Employee ID: EMP101
Enter Employee Name: Rahul

Expense Categories:
1. Travel
2. Food
3. Accommodation
4. Medical
5. Office Supplies
6. Other

Select Category: 1
Enter Claim Amount: 18000
Enter Claim Date (DD-MM-YYYY): 17-11-2026
Receipt Attached? (1=Yes, 0=No): 1

Claim submitted successfully!
Claim ID: 1001
WARNING: Category limit exceeded!
Approval Route: Manager -> Finance
Current Status: Pending Manager Approval

Enter your choice: 2

========== MANAGER APPROVAL ==========

Claim ID: 1001
Employee: Rahul
Category: Travel
Amount: Rs. 18000.00
Policy Violation: YES
Receipt: Attached

Enter Claim ID to process (0 to exit): 1001
1. Approve
2. Reject
Select action: 1

Manager approved the claim.
Forwarded to Finance Department.

Enter your choice: 3

========== FINANCE APPROVAL ==========

Claim ID: 1001
Employee: Rahul
Category: Travel
Amount: Rs. 18000.00
Policy Violation: YES

Enter Claim ID to process (0 to exit): 1001
1. Approve
2. Reject
Select action: 1

Finance approved the claim!
Reimbursement completed.

Enter your choice: 4

========== TRACK CLAIM ==========

Enter Claim ID: 1001

Claim ID: 1001
Employee ID: EMP101
Employee Name: Rahul
Category: Travel
Amount: Rs. 18000.00
Date: 17-11-2026
Receipt: Attached
Category Limit: Rs. 15000.00
Policy Violation: YES

--- APPROVAL HISTORY ---
Manager: Approved
Finance: Approved

Final Status: Approved


## Technology Used

- C Programming Language
- Structures
- Arrays
- Functions
- Conditional Statements
- Loops
- String Handling
- Standard C Libraries
