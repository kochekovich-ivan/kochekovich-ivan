## Core Concepts

### 1. Expected Return of a Portfolio
The portfolio’s return is the weighted average of individual asset returns.

E(Rp) = Σ (wi × E(Ri))  
- wi — weight of asset i in the portfolio  
- E(Ri) — expected return of asset i  

### 2. Portfolio Variance (Risk)
Risk is measured by variance (or standard deviation) of portfolio returns.  

σp² = ΣΣ (wi × wj × Cov(Ri, Rj))  
- Cov(Ri, Rj) — covariance between returns of asset i and j  
- If assets are negatively correlated, portfolio risk decreases.  

### 3. Efficient Frontier
- A set of optimal portfolios offering the **highest return for a given risk**.  
- Portfolios below the frontier are suboptimal.  

### 4. Diversification Effect
- Holding multiple assets reduces overall risk.  
- The benefit depends on correlations: the lower the correlation, the greater the reduction in risk.  

### 5. Risk-Free Asset and Capital Market Line (CML)
- By combining a risk-free asset (e.g., government bonds) with a risky portfolio, investors can achieve different risk-return combinations.  
- The tangent line to the efficient frontier from the risk-free rate is the CML.  
- The tangent point is the **market portfolio**.  

## Example (Two-Asset Case)

Expected portfolio return:  
E(Rp) = w1 × E(R1) + w2 × E(R2)  

Portfolio variance:  
σp² = w1²σ1² + w2²σ2² + 2w1w2σ1σ2ρ12  

- ρ12 — correlation coefficient between asset 1 and 2.  
- If ρ12 < 1, diversification reduces risk.  

## Advantages

- Provides a structured way to balance risk and return.  
- Demonstrates the importance of correlations between assets.  
- Basis for modern financial models and portfolio optimization.  

## Limitations

- Assumes investors are rational and risk-averse.  
- Assumes normally distributed returns (not always true in reality).  
- Relies on historical data for returns, variances, and correlations — may not predict the future.  
- Transaction costs and taxes are ignored.  

## Applications / Use Cases

- Portfolio optimization in investment management.  
- Constructing mutual funds, ETFs, and pension fund strategies.  
- Foundation for later models like the CAPM (Capital Asset Pricing Model).  
