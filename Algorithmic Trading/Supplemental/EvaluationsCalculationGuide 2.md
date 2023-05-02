# Evaluation Metric Calculations

Below is a list of evaluation metrics commonly used to evaluate portfolio/investment performance.

### Annualized Return

A time weighted annual percentage representing the return on an investment over a period of time (also referred to as Compound Annual Growth Rate or CAGR)

<img src="https://render.githubusercontent.com/render/math?math=CAGR = (\frac{\text{End Value}}{\text{Beg Value}} )^ {1/n}-1">

where:

n = number of periods

### Annual Volatility

The annualized degree of variation in trading prices over time for a given set of daily returns.

<img src="https://render.githubusercontent.com/render/math?math=\text{Annual Volatility} = \text{Standard Deviation}(\text{Daily Returns})* \sqrt{n}">

where:

n = number of periods, here 252
### Sharpe Ratio

The return of investment compared to its risk, measured by the difference between the return on investment and the risk-free return.


<img src="https://render.githubusercontent.com/render/math?math=\text{Sharpe Ratio} = \frac{\text{Portfolio Return}-\text{Risk Free Rate}}{\text{Standard Deviation}}">

### Downside Deviation/Return

The measure of risk for returns that are below the minimal acceptable return. Downside deviation is calculated similar to standard deviation; however, deviation is only focused on returns that are less than the minimum acceptable return.

### Sortino Ratio

The quotient of harmful volatility and overall volatility. The Sortino ratio focuses on downside deviation rather than standard deviation.

<img src="https://render.githubusercontent.com/render/math?math=\text{Sortino Ratio}   = \frac{\text{Portfolio Return}-\text{Risk Free Rate}}{\text{Downside Standard Deviation}}">
