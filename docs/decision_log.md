# Decision log (proposed; confirm with mentor)
1. Python chosen for simple file processing and tests.
2. Decimal used for money; half-up rounding.
3. Base rounded to rupee before multiplier; task result to paise.
4. Customer cancellation before pickup earns zero; flat cancellation pay not surged.
5. Cancellation rate = partner cancellations / all task events; average uses rated completed tasks.
6. Gross for penalty cap excludes incentive.
7. Equipment pause checked before equipment deduction, after adjustments.
8. Tax base = earnings + incentive - penalty - equipment + adjustment, floored at zero.
9. PAN 20% override applied only when section threshold is met.
10. Financial-year totals track assessed base at batch time, including held amounts.
11. Marketplace transition uses same annual cumulative base but new section threshold.
12. Net rounded to rupee before minimum check (199.50 becomes 200).
13. Holds released at next Monday batch; no repeated tax on old balances.
14. Retry charge applied on each retry, not on original payment.
15. Adjustment limit uses signed weekly total; prior TDS never refunded.
16. Replay input files deterministically instead of using a database.
17. Separate ledger entries track earnings, deductions, payments and reversals.
18. Negative net is floored at zero; treatment of outstanding debt needs clarification.
