# Pricing-Quanto-Option-for-Nikkei-225-Spot-and-3-month-USD-LIBOR-Rate
Final Project for NYU Courant Graduate Math Finance Course: MATH-GA2791

## Task
We intend to purchase a contract that pays an amount in USD at maturity T:
\begin{equation*}
    \text{max } [0,(\frac{S(T)}{S(0)}-k)\cdot (k' - \frac{L(T-\Delta,T-\Delta,T)}{L(0,T-\Delta,T)})]
\end{equation*}
Where:
\begin{itemize}
    \item $S(t)$ is the Nikkei-255 spot price quantoed from JPY into USD
    \item $L(t,T-\Delta, T)$ is the 3-month USD LIBOR rate between $T-\Delta$ and $T$ 
    \item $\Delta$ is a period of 3 months (0.25 years)
    \item $T$ the expiration date (e.g. 3 years)
    \item $k, k'$ given relative strike prices 
\end{itemize}
Our objective is to develop a pricing routine that computes the value of this contract using the deal terms, such as T, k, k', and market data like volatility and correlation between the underlying assets. In subsequent sections, we will outline the assumptions made in the models and discuss the origin of the data being used.

- Retrieved historical Nikkei-225 and USD/JPY rate data from Yahoo Finance
- Derived short rate, USD/JPY rate and LIBOR rate dynamics (Geometric Brownian Motion and Hull-White model); calibrated model parameters using historical data
- Built a Quanto Option pricing program by implementing a Monte Carlo algorithm

