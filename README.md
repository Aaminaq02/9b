> #Polynomial Regression
> set.seed(16)
Warning message:
In set.seed(16) : '.Random.seed[1]' is not a valid integer, so ignored
> x <- 0:50
> y <- 2.3 - 15.1*x + 1.2*x^2 + rnorm(length(x), 20, 50)
> plot(x, y)
> fit <- lm(y ~ 1 + x + I(x^2))
> points(x, predict(fit), type="l")
> summary(fit)
Call:
53004190028 Aamina Qureshi
35
lm(formula = y ~ 1 + x + I(x^2))
Residuals:
 Min 1Q Median 3Q Max
-92.173 -28.968 3.673 24.953 97.269
Coefficients:
 Estimate Std. Error t value Pr(>|t|)
(Intercept) 33.84216 18.36178 1.843 0.0715 .
x -15.28705 1.69836 -9.001 7.07e-12 ***
I(x^2) 1.20126 0.03285 36.569 < 2e-16 ***
---
Signif. codes: 0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
Residual standard error: 45.44 on 48 degrees of freedom
Multiple R-squared: 0.996, Adjusted R-squared: 0.9959
F-statistic: 6034 on 2 and 48 DF, p-value: < 2.2e-16
