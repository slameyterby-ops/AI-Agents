PAYROLL RECONCILIATION RULES

SP is the source payroll system.

BN is used for validation.

GENERAL RULES

- Treat blank mapped values as zero.
- Component Difference = SP minus BN.
- Never assume the cause of a discrepancy.
- Every conclusion must be supported by SP or BN evidence.
- If evidence is insufficient, use PENDING USER REVIEW.

MULTIPLE SP ROWS

If the same EMP CODE appears multiple times in SP:

- Aggregate all valid rows.
- Aggregate continuation rows.
- Aggregate transfer-related rows.
- Aggregate split activity periods.
- Do not stop after the first row.

BALANCE CHAIN RULE

Never classify solely because Previous Balance or Final Balance differs.

Evaluate:

- Previous Balance
- Current Month
- Transfers
- Allotments
- Settlement activity
- Final Balance

before deciding whether a discrepancy exists.

SETTLEMENT RULE

Settlement in a later payroll month may resolve a prior discrepancy.

Remove an item only when:

- Settlement is confirmed; and
- No new discrepancy remains.

TRANSFER RULE

Transfers between vessels or ranks may create temporary balance differences.

Check both sides before classifying.

PROMOTION RULE

Promotion-related transfers may create payroll movement between vessels.

Review combined records before classification.

STBY RULE

Review STBY and SAIL activities separately before aggregation.

SIGN-OFF RULE

Sign-off settlements may appear in different payroll periods.

Check settlement timing before classification.

SPLIT ACTIVITY PERIOD RULE

A crew member may have multiple payroll periods in the same month.

Aggregate all related records.

MIGRATION RULE

Migration-related differences may arise from presentation differences between systems.

Validate the balance chain before creating a discrepancy.

SEPTEMBER MIGRATION RULE

Ignore:

- Crew missing completely from SP.
- Crew whose SP payroll values are all zero.

Review only populated SP records.

CPF RULE

Validate CPF using actual SP and BN values.

CPF SHF RULE

CPF SHF is separate from employee and employer CPF percentages.

Do not include CPF SHF in CPF percentage calculations.

ALLOTMENT RULE

BN Voluntary Allotment equals:

- Allotment Regular
- Allotment Special

Special usually represents earlier payroll period settlement.

Regular usually represents later payroll period settlement.

REIMBURSEMENT RULE

Check reimbursements separately.

Examples include:

- Airfare
- Visa
- Land transport
- Hotel
- Boiler suit
- Other reimbursement components

Future payroll review may be required when reimbursements create temporary differences.

FUTURE MONTH RULE

For unresolved items:

- Record the outstanding component.
- Record where the amount currently appears.
- Record what should be checked in the next payroll month.
