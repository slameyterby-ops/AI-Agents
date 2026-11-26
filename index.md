SP-BN PAYROLL RECONCILIATION
KNOWLEDGE RULES
FROZEN REFERENCE VERSION

PURPOSE

This Knowledge file provides the interpretation rules, workbook conventions, mappings, presentation standards and recurring payroll patterns used when comparing:

SP = Portage Bill / payroll source.
BN = Payroll Summary / validation source.
Master = Active SP-BN discrepancy register.

The Master contains unresolved items only.


1. IDENTIFICATION

Primary identifier:

EMP CODE in SP = Crew IPN in BN.

Names are supporting information only.

Never determine identity using name alone.

A person can have multiple SP and BN records in one payroll period.


2. SOURCE STRUCTURE

SP may contain:

- Main payroll rows.
- Off-signers.
- Continuation rows.
- Split periods.
- Transfers.
- Sign-off items.
- Deferred payments.
- Previous balances.
- Final balances.

BN may contain:

- SAIL.
- STBY.
- Settlement.
- Sign-off.
- Transfer.
- Multiple activity rows for one Crew IPN.

All applicable rows must be considered before comparison.


3. SP/BN AGGREGATION

If BN has both SAIL and STBY:

Do not compare SP against either BN row individually.

Aggregate the applicable activity rows and trace the balance movement between them.

Important:

BN transfer/beginning balance movements may link the STBY and SAIL rows.

Do not simply sum Beginning Balance and Final Balance fields.

Determine the chronological flow.


4. PAYROLL COMPONENT MAPPING

Equivalent items may use different labels.

Known examples:

BN Comm
=
SP CALLING CARDS / DATA CARDS / RECOVER ADJ.

BN Chinese Social Welfare deductions
=
SP SB&T / SB&TFULL depending on the crew group and payroll treatment.

BN Vol Allotment
=
May correspond to SP allotment / settlement treatment and can cause a negative BN balance without an overpayment.

BN Supplementary Allowance at Sign Off
=
May differ from SP ordinary Supplementary Allowance.

BN Performance Bonus Paid at Sign Off
=
May differ from SP ordinary Performance Bonus.

Reimbursed Meal Fees
=
Must be checked across SAIL/STBY as BN reimbursement may appear on a separate activity row.

Reimbursed Land Transport / Hotel / Boiler Suit
=
Treat as reimbursement and confirm whether paid or carried in SP/payslip.

Opening Balance Adjustment Plus
=
Can explain apparent SP Total Earnings differences. Do not classify as an earnings error if the adjustment correctly explains the balance movement.


5. BALANCE INTERPRETATION

Always distinguish:

- Earnings.
- Deductions.
- Previous/Beginning Balance.
- Current Month.
- Transfer.
- Final Balance.

Final Balance must be understood as a balance-chain result, not an isolated discrepancy.

Examples:

A non-zero Final Balance may simply mean an amount remains payable or recoverable later.

A negative BN Final Balance may be caused by:

- Vol Allotment adjustment.
- Sign-off settlement.
- Transfer movement.
- Recovery.
- Timing difference.

Check the payslip and SP before deciding whether an underpayment or overpayment exists.


6. ROUNDING

Small rounding values such as USD 0.01, USD 0.02 or USD 0.03 should normally be treated as balance-tracking items rather than genuine underpayment/overpayment unless they indicate a larger calculation problem.

Where the payroll otherwise reconciles:

Use:

REVIEW - Balance Tracking

Retain only if the balance needs to be checked against the following payroll.

Chat status:

✅ NO ACTION REQUIRED


7. SIGN-OFF CASES

Sign-off processing frequently creates apparent differences because BN may use:

- Supplementary Allowance at Sign Off.
- Performance Bonus Paid at Sign Off.
- STBY settlement.
- Transfer amounts.
- Vol Allotment.

SP may present the same settlement differently.

Before flagging:

- Aggregate SAIL and STBY.
- Check sign-off date.
- Check ordinary versus sign-off components.
- Check deduction/allotment.
- Check payslip if available.
- Check the resulting Final Balance.

If payslip verifies that the crew was correctly paid and no amount remains outstanding:

Close the case.

Do not retain it just because SP and BN present the transaction differently.


8. VOL ALLOTMENT

Vol Allotment can be used as part of adjustment/settlement activity.

A negative BN balance caused by a valid Vol Allotment adjustment is not automatically an overpayment.

If:

- The Vol Allotment explains the BN balance.
- SP balances.
- Payslip confirms correct payment.
- No outstanding payable or recoverable amount exists.

Then:

Close/remove the row.


9. COMMUNICATIONS / DATA CARD

BN Comm represents communications-related deduction.

Where the crew purchased additional satellite internet/data:

BN Comm
should be compared with:
SP CALLING CARDS / DATA CARDS / RECOVER ADJ.

If BN contains a genuine communications deduction and SP omits it:

SP has deducted less than BN.

This can create an overpayment/recovery case.

Component highlighting must follow the classification colour rule.


10. REIMBURSEMENTS

A reimbursement shown in SP but not identically shown in BN is not automatically an overpayment.

Determine whether:

- It was actually paid to the crew.
- It was valid.
- BN captured it elsewhere.
- It remains in Final Balance.

If confirmed paid correctly:

Close the row.

If confirmed payable but unpaid:

UNDERPAID.

If evidence is insufficient:

PENDING USER REVIEW.


11. MISSING LATER-PAYROLL ROW

A crew member being absent from the following month does not prove settlement.

If a previous discrepancy exists and no later SP/BN evidence is available:

Keep the row active at the latest month for which evidence exists.

Do not assume zero.

Do not delete solely because the crew is absent.


12. REVIEW VERSUS USER REVIEW

REVIEW means:

The case remains active for future checking.

Examples:

- Balance remains.
- Deferred payment scheduled.
- Recovery pending.
- Rounding balance.
- Sign-off settlement to verify.
- Future payroll will provide closure evidence.

REVIEW does not mean the user must act.

Use:

✅ NO ACTION REQUIRED

when the assistant can simply check later payroll evidence.


PENDING USER REVIEW means:

The assistant cannot resolve the issue from the available evidence and needs the user's knowledge, confirmation or another document.

Use:

🚩 USER REVIEW REQUIRED


13. ACTIVE-REGISTER PRINCIPLE

Master is not a history log.

Resolved items should be removed.

The REMARKS field contains the current explanation for active cases.

Historical explanations should not remain if they are no longer relevant to the active issue.


14. REMARKS STANDARD

Preferred formats:

UNDERPAID - [explanation]

OVERPAID - [explanation]

ABNORMAL - [explanation]

REVIEW - Balance Tracking - [explanation]

REVIEW - Settlement Verification - [explanation]

REVIEW - Sign-Off Settlement - [explanation]

REVIEW - Deferred Payment - [explanation]

PENDING USER REVIEW - [unresolved issue and exact question for user]

Remarks should normally include:

- Month.
- Main SP amount.
- Main BN amount.
- Component causing the difference.
- Balance effect.
- What remains unresolved.
- What evidence would close the case.


15. COLOUR / HIGHLIGHTING REFERENCE

Maintain existing workbook colour conventions.

Blue:
Normal reference fields such as Total Deduction / Previous Balance / Final Balance where used by the Master template.

Orange:
Underpaid component or non-zero Previous/Final Balance requiring attention.

Red:
Overpaid component.

Yellow:
Total-level mismatch requiring attention/review.

No highlight:
Normal values or insignificant/ignored rounding where appropriate.

Highlights must agree with REMARKS.

Do not mark an overpayment cell orange.

Do not mark an underpayment component red.

Do not highlight a component as an error when the difference has already been explained as valid payroll treatment.


16. ZERO RULE

Zero differences do not belong in discrepancy cells.

Prefer blanks for zero values in the discrepancy register.

Do not create a discrepancy merely because one system displays zero and the other displays blank.


17. WHOLE-MASTER COUNTING

After every update, classification totals must be calculated from the final active Master REMARKS.

Required cumulative categories:

- UNDERPAID.
- OVERPAID.
- ABNORMAL.
- REVIEW.
- PENDING USER REVIEW.

These counts represent the entire active Master, not only the vessel just processed.

Counts may overlap.

Example:

A REMARK containing both:

PENDING USER REVIEW
and
ABNORMAL

may count in both categories.

Current-vessel row movement counts remain separate:

- Rows added.
- Rows modified.
- Rows removed.


18. CHAT REPORTING STANDARD

For each vessel:

[Vessel], [Month Year]

Active case(s)

[EMP CODE, Name]

- Relevant SP figures.
- Relevant BN figures.
- Balance figures.
- Exact difference.

Explain in simple English.

Then show:

✅ NO ACTION REQUIRED

if the user does not need to provide anything.

OR

🚩 USER REVIEW REQUIRED

if the user must provide a confirmation, explanation or document.


Other handling

Briefly explain material cases that were checked and cleared.


Completion Summary

Current vessel update:

- Rows added.
- Rows modified.
- Rows removed.

Whole active Master:

- UNDERPAID.
- OVERPAID.
- ABNORMAL.
- REVIEW.
- PENDING USER REVIEW.
- Validation failures.


19. USER-REVIEW PRESENTATION

If user review is required, explain each case simply.

Format:

EMP CODE, Crew Name, Vessel

Issue:
[What is different.]

Checked:
[What SP/BN evidence has already been checked.]

Need from you:
[One clear question.]

Avoid technical explanations unless necessary.

If nothing is required from the user:

✅ NO ACTION REQUIRED


20. LANGUAGE

Chat explanations should use simple English.

Workbook REMARKS may contain more detailed payroll language.

Be precise with amounts.

Avoid vague descriptions such as:

“does not tally”

when the specific difference can be stated.


21. SOURCE PRIORITY

For payroll amount comparison:

SP = payroll source.
BN = validation source.

For identifying genuine settlement:

Use the full available evidence, including:

- SP.
- BN.
- Payslip where available.
- Later payroll.
- User-confirmed business treatment.

Do not override supported settlement evidence merely because column presentation differs between SP and BN.
