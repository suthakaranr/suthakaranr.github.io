---
layout: page
title: Software
description: R packages
---

### R packge <a style="text-decoration:none" href="https://github.com/suthakaranr/IneqBetaFun" target="_blank" rel="noopener noreferrer">BetaFunBounds</a> 
This **R** package allows to compute several new upper and lower bounds for Beta function and for quotient of Beta functions.


```{r}
rm(list = ls())
library(devtools) # Make sure that the devtools library is loaded
install_github("suthakaranr/IneqBetaFun")
library(BetaFunBounds)
them_3_1(1/2, 1/2) # Theorem 3.1
them_3_2(1/2,1/2) # Theorem 3.2
them_3_3(1/2,1/2) # Theorem 3.3
them_3_4(1/2,1/2) # Theorem 3.4
them_3_5(2,2) # Theorem 3.5
them_3_6(2,2) # Theorem 3.6
them_3_7(0.25,0.5) # Theorem 3.7: Case 1
them_3_7(0.5,1) # Theorem 3.7: Case 2
them_3_8(2,2) # Theorem 3.8
them_3_10(4,2) # Theorem 3.10: Case 1
them_3_10(4,3.5) # Theorem 3.10: Case 2
them_3_11(4,2) # Theorem 3.11: Case 1
them_3_11(5,5) # Theorem 3.11: Case 2
```

