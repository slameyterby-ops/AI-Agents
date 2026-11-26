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

# Migration Exceptions And User Confirmed Rules

## SP Migration Extract Limitations
After completion of duplicate-row and continuation-row checks:
- Missing SP rows
- All-zero placeholders
- Hidden migration records
- Incomplete migration extracts

should not automatically create discrepancies.

## Active Register Philosophy
- The workbook is an active unresolved-items register.
- Resolved items should be removed.
- Retain an item only when future validation is still required.

## Month Handling
- Month should reflect the latest payroll evidence for that discrepancy.
- Cross-month comparison is permitted when settlement occurs later.

## User Confirmed Payroll Rules
### BN Current Month
Negative BN Current Month values may balance:
- Earnings
- Reimbursements
- Transfers
- Settlements
- Beginning balances

Do not classify until the entire chain is reconstructed.

### Reimbursement Rules
The following may explain differences and must be checked before classification:
- Airfare
- Visa
- Land Transport
- Hotel
- Boiler Suit
- Meal reimbursement

Reimbursements may appear in secondary or continuation SP rows.

### Multi-Row SP Aggregation Rule
Before creating a discrepancy:
- Search the entire SP workbook.
- Aggregate all applicable rows.
- Check continuation rows.
- Check reimbursement-only rows.

A discrepancy created from only the first SP row is invalid.

### CPF Migration Rules
- SHG deductions are separate from CPF contributions.
- SHG is not included in employee CPF.
- SHG is not included in employer CPF.
- SHG differences by themselves should not create discrepancy rows.

### Allotment Rules
- BN Vol Allotment may correspond to SP Allotment Special and/or Allotment Regular.
- Compare complete allotment flow before classification.

### Balance Chain Rules
SP Previous Balance and Final Balance may be part of a carry-forward chain.
Do not classify as discrepancies until the chain is reconstructed.

### Transfer Rules
Cross-vessel transfers may create settlement chains.
Review both vessels and subsequent payroll periods before classification.

### Sign-Off Rules
Sign-off settlements may occur in later payroll periods.
A missing payment in the current period does not automatically mean UNDERPAID.

### Workbook Rules Confirmed By User
- Total Earnings column must show actual SP Total Earnings.
- Total Deduction column must show actual SP Total Deduction.
- Component columns should contain only unreconciled SP minus BN differences.
- Use workbook headers for placement, not remembered column letters.
- Numeric values remain black font.
- Highlight discrepancies according to workbook legend.

## Future Rule Maintenance
Add newly confirmed patterns here.
Do not modify the Frozen Agent Prompt unless workflow or workbook structure changes.

