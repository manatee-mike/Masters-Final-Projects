This Bayesian final project was on Eliud Kipchoge’s sub 2 hour marathon.

Data: https://github.com/hmelberg/berlin-marathon

Eliud Kipchoge made history by running a marathon in less than 2 hours. However, this was not done during a normal marathon and Kipchoge had spotters to help him keep pace. This analysis explores how likely it would be for someone like Kipchoge to run a sub 2 hour marathon during a competitive race.

We decided to use the marathon times from the 2013 Berlin marathon.  

The dependend variable is netTime.

The independed variables of interest are:
- age
- region
- sex

A bayesian linear model was produced in the form $log(netTime) = \beta_0 + \beta_1\cdot log(age) + \beta_2\cdot region + \beta_3\cdot sex$.

The model was produced with the stan_glm function in the rstanarm library.
