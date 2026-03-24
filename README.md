# stock-portfolio-optimization-multi-goal-programming

## Abstract
Multi-objective programming is used to rebalance the investment weights of the stocks in the
S&P 500 ETF in SPY . Two models were developed with the following goals in mind, ranked:
limit principal investment, maximize dividend yield, minimize beta and P/E ratio, limit sector
holding and minimum resource allocation. The GLPK algorithm from Pulp was used to develop
the models where the second model only included the top 50 dividend paying stocks. Both
models resulted in beta, P/E ratio, and dividend yield better than SPY and QDIV , which was used
as a benchmark.

## Methods
In this paper, we develop an investment strategy for a stock portfolio modeling after the S&P 500
(SPY) as our “stock market”. The dataset was obtained from stockanalysis.com (A List of All
Stocks in the S&P 500 Index). It was read and cleaned up by dropping null values in the columns
of interest using the pandas library. For both the original and alternative goal programming
models, there are 1 constraint and 5 goals of varying weights. The constraint is the $1M principal
to invest in the stocks. The goals are as follows: each selected stock has a minimum allocation
of 1% principal, limit sector holding to 30% of the overall portfolio, maximize return on
investment by maximizing the dividend yield, minimize beta, and minimize P/E ratio.
