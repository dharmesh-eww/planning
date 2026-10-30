# Screen 08 — Accounts and Transfers

## Accounts
Cash, bank, wallet, and custom account types. Show account name, currency, current balance, and archived state.

## Account behavior
Create/edit/archive accounts; opening balance; account-specific transaction history. Balance is derived from opening balance plus income minus expenses and transfers.

## Transfer flow
Choose source and destination, amount, currency compatibility, date, and note. Update both accounts atomically. Do not count transfer as income or expense.

## Acceptance
Never combine balances in different currencies. Archive rather than delete accounts with historical transactions.
