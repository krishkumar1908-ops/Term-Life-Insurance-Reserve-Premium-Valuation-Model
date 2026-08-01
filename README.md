[README (1).md](https://github.com/user-attachments/files/30619545/README.1.md)
# Term Life Insurance Reserve & Premium Valuation Model

**Author:** KRISH

**Date:** AUGUST 2026

**Purpose:** Actuarial Analysis Project

## Overview

This project calculates the fair premium and year-by-year statutory reserve for a
term life insurance policy using life-contingent actuarial mathematics, built on
the Society of Actuaries' 2015 Valuation Basic Table (VBT).

## Key Findings

- **Base Case Net Annual Premium:** $278.92 (per $100,000 of coverage)
- **Peak Reserve:** $1,139.15, reached at policy year 12 (age 57)
- **Most Sensitive To:** Policy Term (−30.8% to +61.3% swing in premium)
- **Key Insight:** Extending coverage from 20 to 30 years increases the premium
  by over 61% — more than double the impact of either the mortality assumption
  or the discount rate

## Policyholder Profile

- **Issue Age:** 45
- **Policy Term:** 20 years
- **Face Amount:** $100,000
- **Risk Class:** Male, Non-Smoker, Standard (RR100)
- **Mortality Basis:** 2015 VBT Primary Table, Age Last Birthday

## Methodology

Calculated premiums and reserves using:

1. Life table construction (lx, dx, px, qx) from the 2015 VBT mortality data
2. Commutation function development (Dx, Cx, Nx, Mx) under a 4% discount rate
3. Net Single Premium calculation via `(Mx − Mx+n) / Dx`
4. Net Annual Premium calculation via `NSP / äx:n` (annuity-due factor)
5. Year-by-year prospective reserve schedule (`(Mx+t − Mx+n) − P×(Nx+t − Nx+n)) / Dx+t`)
6. Multi-dimensional sensitivity analysis across discount rate (2–7%), mortality
   assumption (80–120%), and policy term (10–30 years)

## Files

- `Term_Life_Insurance_Reserve_Premium_Model.xlsx` - Complete Excel model

## Visualizations

Reserve Growth Over Policy Duration

<img width="976" height="551" alt="image" src="https://github.com/user-attachments/assets/8907b715-fe10-41c1-ab67-5e501a698c92" />


Net Annual Premium by Scenario

<img width="974" height="534" alt="image" src="https://github.com/user-attachments/assets/9185acee-ba77-4c12-9f9d-e44a7d754089" />


Tornado Chart - Sensitivity Ranking

<img width="984" height="571" alt="image" src="https://github.com/user-attachments/assets/ca42f7f2-24d9-47d4-a1c6-b84a38b8c952" />

## What I Learned

- Life contingencies and commutation functions (Dx, Cx, Nx, Mx)
- Sensitivity analysis for financial and pricing risk
- Excel modeling with formula-driven, dynamic calculations
- Why term life insurance pricing is so sensitive to policy length

## Limitations

- Single risk class only (Male, Non-Smoker, Standard RR100)
- Single policy (not a portfolio of policyholders)
- Deterministic (not stochastic)
- Educational purposes only

## Contact

krish.kumar1908@gmail.com
