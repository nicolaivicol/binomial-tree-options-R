# Pricing options via Binomial Trees in `R`
European, American, Chooser, Knock-Out, Average Strike

## Instructions:

The following function returns a data frame having the binomial tree mapped into it:

```R
getBinomTree(S0, K, vol, dT, r, qdiv, N_steps, isPut=F, isAmerican=F, 
   isAvgStrike=F, isKO=F, isChooser=F, H=NA, Kc=NA, Kp=NA, choose_t1=NA)
```

with the standard inputs for European and American options:    
- `S0`:  underlying asset price at t=0 (e.g. 100)
- `K`:  strike (e.g. 105)
- `vol`:  volatility (e.g. 0.15 for 15%)     
- `dT`:  time to maturity (years) (e.g. 1)
- `r`:  risk-free rate (e.g. 0.05)
- `qdiv`:  dividend rate
- `N_steps`:  number of time steps in tree (# levels = N_steps + 1 at root)
- `isPut`:  F:Call, T:Put
- `isAmerican`:  F:European, T:American   

and additional inputs for exotic options:  
*average strike:*    
- `isAvgStrike`: is average strike options

*knock-out:*    
- `isKO`:  is knock-out option
- `H`:  barrier strike for knock-out

*chooser:*     
- `isChooser`:  is chooser option
- `Kc`:  call strike for chooser option
- `Kp`:  put strike for chooser option
- `choose_t1`:  time to choose for chooser option

## Examples of pricing: [See here](https://htmlpreview.github.io/?https://github.com/nicolaivicol/binomial-tree-options-R/blob/master/examplesBinomTree.html)
