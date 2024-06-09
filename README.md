# Entropic-Portfolio-Optimization
This is Entropic Portfolio Optimization, focusing on minimizing risk through two advanced risk measures: Entropic Value at Risk (EVaR) and Entropic Drawdown at Risk (EDaR). The code is organized into two main parts:

# 1. Entropic Value at Risk Optimization
## 1.1 The Entropic Value at Risk (EVaR)
EVaR is a risk measure that serves as an upper bound for Value at Risk (VaR) and Conditional Value at Risk (CVaR). It is defined using the moment generating function and is parameterized by a significance level $\alpha$.

## 1.2 EVaR Minimization
The EVaR minimization problem is set up using disciplined convex programming (DCP) principles and solved using the CVXPY library. The optimization aims to find the portfolio weights that minimize EVaR subject to constraints on expected return, asset weights, and non-negativity.

### Key steps include:
- Downloading historical asset price data using the yfinance library.
- Calculating daily returns.
- Setting up and solving the EVaR minimization problem using CVXPY, which involves defining variables, constraints, and the objective function.
- Displaying the optimal portfolio weights and annualized statistics (return, standard deviation, variance).

# 2. Entropic Drawdown at Risk Optimization
## 2.1 The Entropic Drawdown at Risk (EDaR)
EDaR is an advanced risk measure that extends the concept of EVaR to drawdowns, representing the risk of large portfolio losses over time.

## 2.2 Maximization of Return/EDaR Ratio
The optimization problem aims to maximize the return-to-EDaR ratio. It is formulated as a linear fractional programming problem and converted into a DCP problem using Charnes and Cooper transformation. The objective is to find the portfolio that maximizes return while minimizing EDaR, subject to various constraints.

### Key steps include:
- Defining cumulative returns and drawdown variables.
- Setting up and solving the EDaR optimization problem using CVXPY, with appropriate constraints and the risk objective.
- Displaying the optimal portfolio weights and annualized statistics (return, standard deviation, variance).
- This code provides a comprehensive approach to portfolio optimization using sophisticated risk measures, leveraging modern convex optimization techniques and financial data analysis.
