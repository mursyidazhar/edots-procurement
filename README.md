[README.md](https://github.com/user-attachments/files/34308823/README.md)
# Procurement ERP: Purchase Request to Goods Receipt

A clickable prototype of a multi-branch procurement flow, built for the
**Product Manager – ERP & Procurement** technical test (Use Case 2).

It covers the full cycle with live, connected data:

1. **Purchase Request**: create a request with items, destination warehouse and justification.
2. **Approval**: amount-based approval matrix per branch, sequential levels, auto-approve when the requester is the approver.
3. **Purchase Order**: created from approved PR lines (PR Line list), one PO per warehouse, vendor picked in a popup, unit price, discount, tax and a 10% price tolerance that needs a reason.
4. **Goods Receipt**: receiving (capped at the PO quantity, extras as free items), then inspection (accepted / rejected with reason), backorder or close short.
5. **Dashboard** and **Procurement flow** (swimlane flowchart) for monitoring.

## Run it

It is a single static file with no dependencies and no build step.

- Open `index.html` in a browser, or
- Publish with GitHub Pages: *Settings → Pages → Deploy from a branch → `main` / root*.

## How to try the flow

Use **Viewing as** (bottom left) to switch role, or the *View as …* links shown on each screen.

| Step | View as | Where |
| --- | --- | --- |
| Create and submit a PR | Dimas Pratama (Requester) | Purchase Request → New request |
| Approve | Andi Saputra (Branch Manager) | Purchase Request → filter *Waiting for my approval* |
| Create PO | Rudi Hartono (Procurement) | Purchase Request Line → tick lines → Create purchase order |
| Receive and inspect | Wulan Sari (WH Jakarta) / Agus Setiawan (WH Bandung) / Eko Prasetyo (WH Surabaya) | Goods receipts |
| Configure approval matrix | Lina Hartati (Procurement Head, admin) | Configuration → Approval Matrix |

Data is sample data held in memory. Reloading the page or **Reset demo data** restores it.

## Notes

- All amounts are in Rupiah. Tax options are PPN 11% and No tax.
- The PRD for this prototype is maintained separately (see the link shared with this repository).
