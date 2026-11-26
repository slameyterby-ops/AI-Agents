# Payroll Reconciliation Knowledge Base

## Core Principles
- SP (PortageBill) is the payroll source.
- BN (Payroll Summary) is the validation source.
- The discrepancy master is a tracking register, not payroll evidence.
- Use payroll evidence before workbook history.

## Resolution Rules
A discrepancy may be removed only when evidence proves settlement through:
- Missing payment paid
- Recovery completed
- Previous Balance cleared
- Final Balance cleared
- Transfer settlement completed
- Cross-vessel settlement completed
- Sign-off settlement completed
- Settlement identified in payroll
- Reimbursement settlement identified
- Aggregated SP rows balancing BN
- Rounding balance cleared

Absence from payroll is not proof of settlement.

## SP Investigation Rules
### Multiple SP Rows
Aggregate all applicable rows before comparison.
Include:
- Earnings
- Deductions
- Reimbursements
- Previous Balance
- Final Balance
- Total Earnings
- Total Deduction
- Allotments

### Continuation Rows
May contain:
- Blank EMP CODE
- Additional payroll periods
- Additional reimbursements
- Additional totals

Use only when worksheet structure clearly shows the same crew member.

### Duplicate Protection
Do not aggregate:
- Report totals
- Summary rows
- Duplicate exports
- Repeated totals

## BN Investigation Rules
Review separately:
- SAIL
- STBY
- Settlement rows

Evaluate:
- Earnings
- Deductions
- Current Month
- Beginning Balance
- Transfer Amount
- Final Balance

Aggregate only after review.

## Settlement Logic
### Split Activity Periods
Trace:
1. Initial payroll period
2. Final Balance
3. Carry-forward
4. Subsequent payroll period
5. Final settlement

If the chain reconciles, the discrepancy may be resolved.

### BN Current Month
Negative Current Month amounts are not automatically discrepancies.
They may offset settlements, reimbursements, transfers, allotments, balances or payroll adjustments.

### Sign-Off Settlement
Potential locations:
- SAIL
- STBY
- Settlement payroll
- Following-month payroll
- Transfers
- Final Balance

### Deferred Payments
Examples:
- Supplementary Allowance
- Performance Bonus
- Rejoining Incentive
- Sign-Off Allowance
- EX-WORK
- Travel Claims
- Reimbursements

## Reimbursement Investigation
Check:
- Medical
- Dental
- Meal
- Land Transport
- Hotel
- Boiler Suit
- Airfare
- Visa
- Travel Claims

Possible locations:
- Main SP row
- Continuation SP row
- Additional SP row
- BN SAIL
- BN STBY
- Settlement rows

## Allotment Interpretation
BN:
- VOL Allotment
- Vol Allotment/BOW_PAL
- Allot.(C)
- Allot.(V)

SP:
- Allotment Special
- Allotment Regular

General interpretation:
- Special = earlier payroll period
- Regular = later payroll period

## Balance Tracking
### Matching Balances
Matching SP and BN balances are not discrepancies by themselves.

### Opening Balance Adjustments
Require investigation before classification.

### Negative Final Balances
Investigate:
- Sign-off settlement
- Transfer settlement
- Recovery
- Settlement verification

ABNORMAL only when a payroll error is confirmed.

## Rounding Balances
Typical residuals:
- 0.01
- 0.02
- 0.03

When earnings, deductions and components reconcile:
- Use REVIEW – Balance Tracking.
- Remove only after clearing.

## Component Mapping
Known mappings:
- BN Comm -> SP CALLING CARDS
- BN Comm -> SP DATA CARDS
- BN Comm -> SP RECOVER ADJ

Mappings identify equivalent fields but do not automatically reconcile them.

## Singapore CPF Rules
Definitions:
- CPFEE = Employee CPF
- CPFER = Employer CPF
- CDAC-EE = Chinese SHG
- MBMF-EE = Malay SHG
- SINDA-EE = Indian SHG
- ECF-EE = Eurasian SHG
- SDL-ER = Skills Development Levy

Rules:
- SHG deductions are additional deductions.
- SHG is not included in CPFEE.
- SHG is not included in CPFER.
- SDL-ER is not included in CPFER.
