---
title: 'genetic-selectR Package Development'
excerpt: "<img src='/images/ga_cover.png'><br/>Short description of portfolio item number 2"
collection: portfolio
---

## I Introduction
In this project, we created a R package implementing genetic algorithms for variable selection in regression
problems, including both linear regression and GLMs. We allow users to choose their own fitness functions
and by default it’s AIC. Several genetic operators, such as crossover and mutation are combined into this
whole selection process. We test all of our functions using different datasets and criteria. The results
implementing our package on the Boston dataset are shown below.

All code for this project can be found in GitHub repository: 
<a href="https://github.berkeley.edu/asjew/GA" style="color: black; text-decoration: none;">https://github.berkeley.edu/asjew/GA</a>

### II Algorithms
In order to implement this genetic selection algorithm, we partitioned each step of the algorithm into separate
helper functions and formatted our main select function such that it carries out the genetic algorithm by
calling each of our helper functions. Because each of our helper functions had a well-defined task, this also
allowed each of us to focus on building functions without having to consult each other about any minute
changes were being made. Each helper function is briefly described as follows:


#### Calculate Fitness and Find the Best Model
In the calc_fit function, we aim to obtain fitness values for the population. The user can specify their own
fitness function and regression type. For these two, the default are AIC and linear regression. Then we call
find_best_model function to pick out the gene which has best fitness score(eg:for AIC, it’s the lowest) in
the current generation.

#### Select Parents
In the select_parents function, we aim to select parents on the basis of their fitness scores. We offer two
selection methods in this function, one is “prop_rand” and the other one is “tournament”. “prop_rand”
method chooses one parent with probability proportional to the fitness functions and the other one at random
while “tournament” basically chooses the best one in different sections.

#### Crossover
In the crossover_p_split function, we aim to carry out the crossover operator and obtain offspring. Users are
allowed to choose the number of split points. We divide both parents into (p+1) parts. Then we randomly
choose whose piece of gene should be inherited by one offspring and the other offspring inherits from the
other parent’s piece.

#### Mutation
In the mutate_genes function, we aim to decide whether certain gene would mutate or not. As usual, we
let users choose the mutation rate(by default it’s 0.01). In the simplest implementation, each gene has an
independent probability, mu, of mutating, and the new allele is chosen completely at random from the genetic
alphabet.

#### Select
In the select function, we pool previous functions together to form this one. We first call gen_firstgen function
to generate the first random generation and then call above functions one by one. The max_iter default is 50
and also can be specified by users. Moreover, we use a scaled relative error between the best fitness score of
our current generation and the best fitness score of our previous generation to evaluate diversity. And if this
relative error is less than the diversity threshold for three consecutive times, we consider it as convergence.
When designing the output of our select function, we decided to only return sufficient information about the
best model, such as its fitness score, the generation it was created, as well as the average fitness score of that
generation. Additionally, our function also prints a plot that visualizes the changes that occur between the
average and best fitness scores throughout the generations of genes and highlights when our best model was
created.
3 Results
We decided to use the “Boston” dataset from the MASS library to illustrate our results because it is a linear
dataset that is commonly used. Under different conditions, it will all converge but with different rates. We
thus explore how different methods/parameters affect the rate of convergence.
3.1 The default
In this part, we use all the default methods/parameters to select variables. The result is shown as below:
