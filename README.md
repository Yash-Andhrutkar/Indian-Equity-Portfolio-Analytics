# Indian Equity Portfolio Analytics

A dynamic Excel-based portfolio analytics model for a diversified Indian equity portfolio, covering **performance measurement, benchmark comparison, risk analysis, diversification, drawdown analysis, and return/risk attribution**.

The portfolio consists of **7 Indian large-cap equities across 7 sectors**, with the **NIFTY 50** as the benchmark.

The model uses weekly market data and is designed to refresh as new observations become available. A separate monthly PDF dashboard provides an executive-level visual summary of the portfolio.

---

## Project Overview

This project demonstrates the construction of a portfolio analytics framework in Microsoft Excel.

The model integrates market data, portfolio calculations, benchmark analysis, risk metrics, attribution analysis, and visualization into a structured analytical workflow.

### Key Areas Covered

- Portfolio performance
- NIFTY 50 benchmark comparison
- Excess return
- Annualized volatility
- Sharpe ratio
- Portfolio beta
- Jensen's alpha
- Maximum drawdown
- Growth of ₹100
- Return contribution by holding
- Risk contribution by holding
- Correlation analysis
- Diversification analysis
- Sector exposure

---

## Portfolio Composition

| Company | Sector | Weight |
|---|---|---:|
| Reliance Industries | Energy / Conglomerate | 23% |
| Bharti Airtel | Telecom | 15% |
| HDFC Bank | Banking | 15% |
| Larsen & Toubro | Industrials / Infrastructure | 14% |
| Cipla | Pharmaceuticals | 12% |
| Maruti Suzuki | Automobile | 12% |
| HCL Technologies | Information Technology | 9% |
| **Total** |  | **100%** |

**Benchmark:** NIFTY 50  
**Data Frequency:** Weekly  
**Portfolio Holdings:** 7  
**Sector Exposure:** 7 sectors

---

## Repository Structure

```text
indian-equity-portfolio-analytics/
│
├── model/
│   └── Indian_Equity_Portfolio_Analytics.xlsx
│
├── reports/
│   └── Indian_Equity_Portfolio_Monthly_Dashboard.pdf
│
└── README.md
```

---

## Excel Model

The Excel workbook is the core analytical model.

It is structured into separate worksheets for market data, calculations, risk analytics, attribution, and presentation.

### Workbook Structure

- `Overview`
- `Inputs`
- `Holdings`
- `Prices`
- `Market_Data`
- `Returns`
- `Risk_Analysis`
- `Correlation`
- `Drawdown`
- `Benchmark`
- `Contribution`
- `Dashboard`

This separation helps maintain transparency between raw market data, portfolio calculations, analytical outputs, and visualization.

---

## Market Data

Historical equity prices are retrieved using Excel's `STOCKHISTORY` functionality.

The NIFTY 50 benchmark data is incorporated separately through Power Query.

The model uses **weekly observations** for portfolio and benchmark analysis.

The refresh architecture allows new market observations to flow through the model without rebuilding the analytical framework.

---

## Portfolio Performance

Weekly security returns are calculated from historical price observations and combined using the portfolio's target weights.

The model evaluates both absolute portfolio performance and performance relative to the NIFTY 50.

Key performance measures include:

- Portfolio return
- Benchmark return
- Excess return
- Growth of ₹100
- Risk-adjusted performance
- Benchmark-relative performance

---

## Risk Analysis

The model evaluates portfolio risk using several commonly used portfolio analytics metrics.

### Annualized Volatility

Measures the annualized variability of weekly portfolio returns.

### Sharpe Ratio

Evaluates portfolio return relative to total portfolio risk using a risk-free rate assumption.

### Beta

Measures the sensitivity of portfolio returns to movements in the NIFTY 50.

### Jensen's Alpha

Evaluates portfolio performance relative to the return implied by its systematic market risk.

### Maximum Drawdown

Measures the largest peak-to-trough decline experienced by the portfolio during the historical observation period.

---

## Growth of ₹100

The model tracks the hypothetical growth of **₹100 invested in the portfolio** and compares it against ₹100 invested in the NIFTY 50 over the same period.

This provides a visual representation of cumulative portfolio performance relative to the benchmark.

The underlying time series is designed to extend as new weekly observations become available.

---

## Drawdown Analysis

Portfolio drawdowns are tracked through time and compared against the NIFTY 50.

This allows the model to evaluate:

- Historical downside periods
- Peak-to-trough portfolio losses
- Benchmark drawdowns
- Relative downside behaviour

---

## Return Attribution

The model decomposes portfolio performance by security to identify the contribution of each holding to overall portfolio return.

This helps identify:

- Top positive contributors
- Largest detractors
- Relationship between portfolio weight and performance contribution

Return attribution provides additional insight beyond simply observing individual stock returns.

---

## Risk Contribution

Portfolio risk is decomposed across the seven holdings using the portfolio covariance structure.

This identifies how much each security contributes to total portfolio risk.

Risk contribution can differ substantially from portfolio weight because it depends on:

- Security volatility
- Portfolio weight
- Covariance with other holdings

This provides a more complete view of portfolio concentration than capital allocation alone.

---

## Correlation Analysis

A **7 × 7 correlation matrix** evaluates the historical relationship between weekly returns across portfolio holdings.

The model also evaluates:

- Average pairwise correlation
- Highest pairwise correlation
- Lowest pairwise correlation
- Diversification ratio

Correlation analysis helps determine whether combining the selected securities provides meaningful diversification benefits.

---

## Diversification Analysis

The portfolio contains companies from seven different sectors:

- Energy / Conglomerate
- Telecom
- Banking
- Industrials / Infrastructure
- Pharmaceuticals
- Automobile
- Information Technology

The diversification ratio and correlation structure are used to evaluate the extent to which combining these holdings reduces aggregate portfolio risk.

---

## Benchmark Analysis

The **NIFTY 50** serves as the portfolio benchmark.

Portfolio and benchmark results are compared across measures including:

- Return
- Volatility
- Sharpe ratio
- Maximum drawdown
- Growth of ₹100
- Beta
- Excess return

This allows the portfolio to be evaluated in both absolute and benchmark-relative terms.

---

## Monthly Portfolio Dashboard

A separate PDF dashboard provides a concise, presentation-focused summary of the portfolio.

The dashboard includes:

- Portfolio vs NIFTY 50 performance
- Growth of ₹100
- Portfolio allocation
- Sector exposure
- Annualized volatility
- Sharpe ratio
- Beta
- Jensen's alpha
- Maximum drawdown
- Drawdown comparison
- Return contribution
- Risk contribution
- Correlation matrix
- Diversification metrics
- Portfolio observations

The PDF acts as a **monthly snapshot**, while the Excel workbook remains the underlying dynamic analytical model.

### Latest Monthly Report

[View the Monthly Portfolio Dashboard](reports/Indian_Equity_Portfolio_Monthly_Dashboard.pdf)

---

## Dynamic Refresh Workflow

The analytical workflow is designed as:

```text
Excel Market Data Refresh
          ↓
Stock Price Update
          ↓
NIFTY 50 Benchmark Refresh
          ↓
Weekly Return Calculation
          ↓
Portfolio Performance Calculation
          ↓
Risk & Benchmark Analysis
          ↓
Correlation & Diversification Analysis
          ↓
Return & Risk Attribution
          ↓
Dashboard Update
          ↓
Monthly PDF Dashboard
```

The Excel workbook can therefore continue to be used as additional weekly market observations become available.

The PDF dashboard is regenerated periodically to provide an updated presentation of the latest portfolio results.

---

## Monthly Reporting Process

The intended reporting workflow is:

1. Open the Excel model.
2. Refresh market data.
3. Refresh the NIFTY 50 benchmark.
4. Allow portfolio calculations to update.
5. Review portfolio and risk analytics.
6. Generate an updated monthly dashboard PDF.
7. Publish the latest report to the repository.

This separates the **dynamic analytical model** from the **executive-facing monthly report**.

---

## Tools & Techniques

### Tools

- Microsoft Excel
- Excel STOCKHISTORY
- Power Query

### Financial Analytics

- Portfolio return analysis
- Benchmark analysis
- Annualized volatility
- Sharpe ratio
- Beta
- Jensen's alpha
- Maximum drawdown
- Covariance analysis
- Correlation analysis
- Diversification analysis
- Return attribution
- Risk contribution

### Excel Techniques

- Dynamic formulas
- Dynamic named ranges
- INDEX-based ranges
- Lookup functions
- Conditional formatting
- Financial dashboards
- Data visualization
- Power Query data integration

---

## Project Objectives

This project was developed to demonstrate practical skills relevant to:

- Financial Analysis
- Investment Analysis
- Portfolio Analytics
- Risk Analysis
- Data Analysis
- Business Analysis

The objective is not simply to calculate portfolio returns, but to build a structured framework that connects:

**Market Data → Portfolio Performance → Risk → Attribution → Benchmarking → Visualization**

---

## Key Learning Outcomes

The project demonstrates the ability to:

- Structure a multi-sheet financial model
- Integrate market data into Excel
- Analyze portfolio performance using weekly return data
- Compare portfolio performance against a market benchmark
- Measure systematic and total portfolio risk
- Analyze historical drawdowns
- Decompose portfolio returns by holding
- Decompose portfolio risk by holding
- Evaluate security correlations
- Quantify diversification benefits
- Translate financial calculations into a professional dashboard
- Present analytical results through a concise monthly portfolio report

---

## Model Limitations

The analysis is based on historical market data and a predefined portfolio allocation.

The model does not account for all real-world portfolio considerations, including:

- Transaction costs
- Taxes
- Slippage
- Liquidity constraints
- Portfolio management fees
- Future changes in market conditions

Historical relationships between securities, including volatility and correlation, may change over time.

---

## Disclaimer

This project is created for **analytical, educational, and portfolio demonstration purposes only**.

It does not constitute investment advice, financial advice, a recommendation, or a solicitation to buy or sell any security.

Historical performance is not indicative of future results.
