This Bayesian final project was on Eliud Kipchoge’s sub 2 hour marathon.

Data: https://github.com/hmelberg/berlin-marathon

Eliud Kipchoge made history by running a marathon in less than 2 hours. However, this was not done during a normal marathon and Kipchoge had spotters to help him keep pace. This analysis explores how likely it would be for someone like Kipchoge to run a sub 2 hour marathon during a competitive race.

We decided to use the marathon times from the 2013 Berlin marathon.  

The dependend variable is netTime.

The independed variables of interest are:
- age
- region
- sex

A bayesian linear model was produced in the form $log(netTime) = \beta_0 + \beta_1\cdot log(age) + \beta_2\cdot region + \beta_3\cdot sex + \epsilon$.

The model was produced with the stan_glm function in the rstanarm library.

The residuals closely follow a normal distribution and the assumptions for a linear model are met.

6000 models were simulated and each model had a set of $\beta$'s as well as model variances ($\sigma^2$). Kipchoge was 34 years old, from the African region (Kenya), and is male. 
The expected time for each model was computed. 
The probability of running the marathon under 2 hours was calculated with a the assumption that errors are normally distributed, the expected times are the means, and the estimated $\sigma^2$'s. 
The probability distribution closely followed a beta distribuion. 
The median probability of Kipchoge running a marathon under 2 hours was estimated to be 5e-5 (0.005%).
This highlights Kipchoge's achievement and demonstrates how difficult a sub 2 hour marathon is.

