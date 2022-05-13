---
layout: page
title: Software
description: R packages
---

#### <a style="text-decoration:none" href="https://github.com/suthakaranr/IneqBetaFun" target="_blank" rel="noopener noreferrer">IneqBetaFun</a> 
The **R** package **IneqBetaFun** provides several new upper and lower bounds for the Beta function and the quotient of Beta functions. Please see the examples below.


```{r}
rm(list = ls())
library(devtools) # Make sure that the devtools library is loaded
install_github("suthakaranr/IneqBetaFun")
library(IneqBetaFun)

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
them_3_11a(4,2) # Theorem 3.11: Case 1
them_3_11b(5,5) # Theorem 3.11: Case 2
corollary_2(1, 1.5) # Corollary 2
them_3_14(1,2) # Theorem 3.14
them_3_15(1,2) # Theorem 3.15

# Ratios of Beta Functions

them_3_9(0.5,0.75) # Theorem 3.9: Case 1: x1 <= x2
them_3_9(1.5,1) # Theorem 3.9: Case 2: x1 > x2
them_3_17(1, 1.5, 2) # Theorem 3.17
corollary_ratio_1(1, 1.5,2, 3) # Corollary 1
them_3_13(1, 1.5,2) # Theorem 3.13
them_3_16(1, 1.5,2) # Theorem 3.16
them_3_17(1, 1.5,2) # Theorem 3.17
```

<br/>


#### <a style="text-decoration:none" href="https://github.com/suthakaranr/EfficientClosedGPD" target="_blank" rel="noopener noreferrer">EfficientClosedGPD</a> 
The **R** package **EfficientClosedGPD** provides some efficient closed form estimators of the parameters of the
Generalized Pareto Distribution. Please see the examples below.


```{r}
rm(list = ls())
library(devtools) # Make sure that the devtools library is loaded
install_github("suthakaranr/EfficientClosedGPD")
library(EfficientClosedGPD)  # Load the package 
set.seed(650) 
x = rgpd2(40, 2, 2) # Generate sample
Method1(x) # Method 1
Method2(x) # Method 2
Method3(x) # Method 3
MethodQM(x) # Method QM
MethodPOS(x) # Method POS
MethodLCVM(x) # Method LCVM
```

