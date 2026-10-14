# TransactionException

Present only when the payment waits for the merchant's decision. paid_late: coins arrived within 6h after the window closed (status stays expired; complete it with Mark as paid in the dashboard, which also sends payment.completed). needs_review: ETH/ERC-20 deposit address balance dropped while open, payment unknown (status pending). 

## Enum

* `PAID_LATE` (value: `'paid_late'`)

* `NEEDS_REVIEW` (value: `'needs_review'`)

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


