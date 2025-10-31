# Vending_Machine

This project implements a fully functional **FSM-based Vending Machine** using Verilog HDL.  
The machine supports **multiple products, coin-based payment, online payment, and cancel/refund logic**.

---

##  Features

- Supports **5 products**:
  - Pen (₹15)
  - Notebook (₹50)
  - Coke (₹30)
  - Lays (₹35)
  - Water Bottle (₹20)

- Accepts **two types of payment**:
  - Coin Input (total value entered)
  - Online Payment flag

- **Cancel transaction** at any time → returns full money.
- **Automatic change return** if extra money is inserted.
- Clear **state output**, **selected price**, and **dispense signal**.

---

##  Finite State Machine (FSM) States

| State Code | State Name | Description |
|-----------|------------|-------------|
| 0000      | IDLE | Waiting for user to start |
| 0001      | SELECT_PRODUCT | Waiting for product selection |
| 0010      | PEN_SELECTION | Price = 15 |
| 0011      | NOTEBOOK_SELECTION | Price = 50 |
| 0100      | COKE_SELECTION | Price = 30 |
| 0101      | LAYS_SELECTION | Price = 35 |
| 0110      | WATER_BOTTLE_SELECTION | Price = 20 |
| 0111      | DISPENSE_AND_RETURN | Product is dispensed and change (if any) is returned |
