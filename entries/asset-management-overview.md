# 📘 Asset Management & QA Testing – Self-Learning Notes

A structured learning journey on asset management concepts + how they connect to QA testing for financial platforms.

---

## 1. Asset Management Basics

**Main Goal of an Asset Manager**
- Maximize client returns **for a given level of risk**.
- Balance **risk vs reward** → not just chasing high returns.

**Active vs Passive Management**
- **Passive**: Replicates the market (e.g., S&P 500 index fund).
- **Active**: Attempts to **beat the market** by spotting inefficiencies.

**Tester’s Insight**
- Active managers face pressure to outperform → Even small errors in AI output can break client trust.

---

## 2. Investment Research

**Two Approaches**
- **Fundamental Analysis** → Product, management, financial health, competitors.
- **Quantitative Analysis** → Numbers, price patterns, volatility, momentum.

**Examples**
- Reading an annual report → **Fundamental**.
- Screening for +20% price rise last month → **Quantitative**.

**Tester’s Role**
- Validate both types of claims:
  - *Fundamental*: Use SQL to check company debt, cash flow, revenue.
  - *Quantitative*: Use Python/SQL to calculate momentum, volatility.

---

## 3. Portfolio & Diversification

**Definition**: A portfolio = collection of assets (stocks, bonds, real estate, cash).
**Diversification**: Spreads investments across sectors/assets to reduce risk.

**Tester’s Risk Check**
- If AI only picks tech stocks → sector concentration risk.
- Suggested tests:
  - Correlation analysis of holdings.
  - Shock test: simulate sector-wide news.

---

## 4. Holdings & Returns

- **Holdings** = Snapshot of owned assets at a single point in time.
- **Returns** = Performance change between two dates.

**Examples**
- Jan 31 vs Feb 28 holdings → calculate **monthly return**.
- Returns are like “interest earned” on a savings account.

---

## 5. Attribution Analysis

**Purpose**: Explains *why* a portfolio out/underperformed.

**Example**
- Report: *“Outperformance from stock selection in healthcare.”*
- Meaning: AI picked the right healthcare companies, not just lucky sector exposure.

**Tester’s Steps**
1. Pull AI’s healthcare holdings + returns (SQL).
2. Pull benchmark healthcare stocks (SQL).
3. Compute weighted average returns for both (Python).
4. Compare with attribution report output.

---

## 6. Structured Testing in Finance

### Regression Testing
- **Q:** Did new updates break old features?
- **Goal:** Stability.
- **Example:** After new feature, confirm Returns & Attribution still calculate correctly.

### Acceptance Testing
- **Q:** Does the new feature meet user requirements?
- **Goal:** Usability & correctness.
- **Example:** “Portfolio Risk” button → Generates score, within plausible range, updates on changes.

### Edge Case Testing
- **Q:** What happens under extreme or weird inputs?
- **Goal:** Ensure system resilience.
- **Examples:**
  - Negative stock prices.
  - NULL/missing financial data.
  - Market drops 50% in a day.

---

## 7. Example – Portfolio Risk Button

**Acceptance Test**
1. Click button → Verify risk score appears.
2. Check score within realistic range.
3. For a simple portfolio, manually calculate expected risk and compare.
4. Verify score updates correctly on buy/sell.

**Regression Test**
- Ensure returns & attribution unaffected.

**Edge Cases**
- Portfolio contains missing/NULL data.
- Extremely volatile stock (huge swings).

---

# 📑 How to Use This Guide

- ✅ Read concept → example → tester’s role.
- ✅ Try re-explaining each section in your own words.
- ✅ Build small Python/SQL test scripts to practice.
- ✅ Keep adding notes, code snippets, and test cases here as you learn.

---

# 🛠️ To-Do / Practice Checklist

- [ ] Write a Python script to calculate returns from two holdings files.
- [ ] SQL query to check company debt levels for a given ticker.
- [ ] Python script to compare portfolio vs benchmark returns.
- [ ] Design regression test cases for returns & attribution.
- [ ] Create edge case scenarios (negative price, missing data, sector crash).
