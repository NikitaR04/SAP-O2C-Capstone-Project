# SAP SD — Order-to-Cash (O2C) Capstone Project

## Overview

This project documents the complete **Order-to-Cash (O2C)** business process implemented using the **SAP SD (Sales & Distribution)** module in SAP S/4HANA.

The scenario is based on a fictitious company — **NovaTech Electronics Pvt. Ltd.** — processing a full B2B sales cycle, from capturing a customer inquiry to receiving final payment.

---

## Business Scenario

| Field | Details |
|---|---|
| Company | NovaTech Electronics Pvt. Ltd. |
| Customer | BlueStar Retail Pvt. Ltd. |
| Product | NT-Pro Laptop Model X |
| Quantity | 100 units |
| Unit Price | ₹55,000 per unit |
| Total Value | ₹55,00,000 |

---

## O2C Process — Steps & Transaction Codes

| Step | Activity | T-Code | SAP Module |
|---|---|---|---|
| 1 | Customer Inquiry | VA11 | SAP SD |
| 2 | Quotation Creation | VA21 | SAP SD |
| 3 | Sales Order Creation | VA01 | SAP SD |
| 4 | Outbound Delivery | VL01N | SAP SD / WM |
| 5 | Post Goods Issue | VL02N / LT03 | SAP SD / WM |
| 6 | Billing / Invoice | VF01 | SAP SD / FI |
| 7 | Incoming Payment | F-28 | SAP FI |

---

## Tech Stack

- SAP S/4HANA Cloud (Trial)
- SAP SD — Sales & Distribution Module
- SAP FI — Financial Accounting Module
- SAP WM — Warehouse Management Module

---

## Project Structure

```
SAP-O2C-Capstone-Project/
├── README.md
├── O2C_Process_Report.pdf
└── screenshots/
    ├── 01_va11_inquiry_initial.png
    ├── 02_va11_inquiry_overview.png
    ├── 03_va21_quotation_initial.png
    ├── 04_va21_quotation_overview.png
    ├── 05_va01_concept.png
    ├── 06_va01_sales_order_overview.png
    ├── 07_va01_shipping_tab.png
    ├── 08_vl01n_delivery_initial.png
    ├── 09_vl01n_delivery_quantities.png
    ├── 10_vl02n_post_goods_issue.png
    ├── 11_lt03_transfer_order_initial.png
    ├── 12_lt03_transfer_order_overview.png
    ├── 13_lt03_transfer_order_confirm.png
    ├── 14_vf01_billing_document.png
    ├── 15_f28_payment_header.png
    └── 16_f28_payment_open_items.png
```

---

## Key Learnings

- Every O2C step is tightly integrated — changes in the sales order automatically reflect in delivery, billing, and financials
- Post Goods Issue (VL02N) and Billing (VF01) both trigger automatic journal entries in SAP FI
- SAP maintains a complete document chain — fully traceable from Inquiry to Payment
- Master data (Customer Master, Material Master, Pricing Conditions) is the backbone of the entire cycle

---

## Future Improvements

- SAP CRM integration for customer interaction tracking
- Automated billing runs using VF04 (collective billing)
- Credit management via FD32 during sales order creation
- GST e-invoicing portal integration for automatic IRN generation
- SAP Analytics Cloud dashboards for real-time O2C monitoring

---

## Submitted By

| Field | Details |
|---|---|
| Name | Nikita Rani |
| Roll Number | 2305305 |
| Program | B.Tech Computer Science & Engineering |
| University | KIIT Deemed to be University, Bhubaneswar |
| Batch | 2023–2027 |
