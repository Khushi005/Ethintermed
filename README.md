# Ethintermed
# ScholarshipEligibilityChecker
The ScholarshipEligibilityChecker is a Solidity smart contract designed to evaluate and manage scholarship eligibility based on the Cumulative Grade Point Average (CGPA) system. The contract allows the owner to check eligibility for different types of scholarships and update the CGPA.

# Features
Check Eligibility for Full Scholarship: Requires a CGPA of 9.5 or higher.
Check Eligibility for Half Scholarship: Requires a CGPA of 8.5 or higher.
Check Eligibility for Quarter Scholarship: Requires a CGPA of 7.5 or higher.
Check Minimum CGPA: Ensures the CGPA is at least 4.0.
Check for Any Scholarship: Verifies if the CGPA meets the minimum requirement of 5.0 for any scholarship.
Ownership Control: Only the contract owner can perform eligibility checks and update the CGPA.
# Contract Details
State Variables
uint256 public CGPA = 8;: Stores the current CGPA, initialized to 8.
address public owner;: Stores the address of the contract owner.
# Events
event CGPAChanged(uint256 currentCGPA);: Emitted when the CGPA is updated.
# Modifiers
modifier onlyOwner(): Restricts function access to the owner.
# Constructor
constructor(): Sets the deployer of the contract as the owner.
# Functions
function checkforFullScholarship(uint256 currentCGPA) external onlyOwner: Checks eligibility for a full scholarship.

Requires currentCGPA >= 9.5.
Updates CGPA and emits CGPAChanged.
function checkforHalfScholarship(uint256 currentCGPA) external onlyOwner: Checks eligibility for a half scholarship.

* Requires currentCGPA >= 8.5.
* Updates CGPA and emits CGPAChanged.
function checkforQuarterScholarship(uint256 currentCGPA) external onlyOwner: Checks eligibility for a quarter scholarship.

* Requires currentCGPA >= 7.5.
* Updates CGPA and emits CGPAChanged.
function checkMinimumCGPA() external view: Asserts that the CGPA is at least 4.0.

function checkforAnyScholarship(uint256 currentCGPA) external onlyOwner: Checks if the currentCGPA meets the minimum requirement for any scholarship.

* Requires currentCGPA >= 5.0.
* Updates CGPA and emits CGPAChanged.
# Usage
Deployment
Deploy the contract using your preferred Ethereum development environment (e.g., Remix, Truffle, Hardhat).

1 Interacting with the Contract
*  Check Eligibility for Full Scholarship

2 Call checkforFullScholarship with the desired CGPA.
*  Check Eligibility for Half Scholarship

3 Call checkforHalfScholarship with the desired CGPA.
*  Check Eligibility for Quarter Scholarship

4 Call checkforQuarterScholarship with the desired CGPA.
*  Check Minimum CGPA

5 Call checkMinimumCGPA to verify the minimum CGPA.
*  Check for Any Scholarship

6 Call checkforAnyScholarship with the desired CGPA.

# License
This project is licensed under the MIT License.
