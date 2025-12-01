# AI-Assisted Valuation of Callable Corporate Bonds

## Project Overview
This project values a **10-Year Callable Bond** (5% Coupon) under two distinct market environments. The model uses a **Vasicek stochastic process** to simulate interest rate paths and applies **Backward Induction** to price the embedded call option.

## 1. Modeling Assumptions
* **Bond Structure:** Face Value $1000, 5% Annual Coupon, Callable at Par ($1000) after Year 5.
* **Model Used:** Vasicek One-Factor Model for interest rate diffusion.
* **Valuation Method:** Monte Carlo Simulation (1,000 paths) with Backward Induction logic.

## 2. Market Scenarios Created
I designed two unique narratives to stress-test the bond's "Negative Convexity":

### Scenario A: "The Hard Landing"
* **Narrative:** A recession triggers a central bank pivot.
* **Parameters:** Rates revert to a long-term mean of **1%** with high volatility (**3%**).
* **Outcome:** High risk of the bond being called.

### Scenario B: "The Inflationary Spiral"
* **Narrative:** Persistent inflation forces rates higher.
* **Parameters:** Rates drift to a long-term mean of **8%** with low volatility (**1%**).
* **Outcome:** Call option expires worthless; bond acts like a standard fixed-income security.

## 3. AI & Tool Usage
* **GitHub:** Used for version control and to prove independent data generation (timestamped commits).
* **AI Assistance:** AI tools were used to debug the Vasicek discretization code and optimize the vectorization of the backward induction loop in Python. The scenario narratives were self-designed based on macro-economic theory.
