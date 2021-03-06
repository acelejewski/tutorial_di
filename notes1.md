---
title: "bayesnotesI"
author: "Adam"
date: "May 27, 2018"
output:  
      html_document:  
        keep_md: true  
        
        
        
---



# The null hypothises signifcance testing controversy
NHST hypotheses testing is common to many disciplines, and has faced criticisms.Some have called for classical frequent inference to be abandoned (including NHST and CI in favor of non frequentist alternatives such as likelihood or Bayesian inference=)

The criticism of hypothesis testing can fall into 3 categories

1.  *Signficance testing is widly misunderstood*
2.  *NHST leads to serious prolbems when applied*
3. *NHSTs are the worng tool for the job*: NHST make probability calculations that are conditional on the null hypothesis $H_0$. It is a matter of philosophical debate as to whether $H_0$ can ever be true. 


Most of the misconceptions, involve diffuculites understanding or reasoning with conditional probabilities. 

**A  *p* value is the probability of a result as extreme or more extreme than the one observed when $H_0$ is true. ** It is *not* the the probability of $H_0$ being true (an unconditional probability)


**Lindley's paradox:**  No matter how small  the value $H_0$ can be be highly probable. Scenario: A mother's two children die months apart form each other. She is accused of murder, but the differnece is SIDS.  SIDS are 1/8543, so then the probability of two subsequent deaths is 1 in 73 million - This makes the assumption that the two results are independent. This is a conditional probability. It is the pros ability of the observed data on the assumption that both deaths are due to SIDS i.e.e ($H_0$) is true. The actual probability that both deaths were due to SIDS is larger that one in 73 million. The probability of either cause of death can be evaluated without considering the other. As there are two mutually exclusive outcomes, the probability of either hypothesis depends on the relative rarity of SIDS and murder. If they are equally rare, the ratio of the conditional probabilities is one, and the probability of either being correct is .5. Therefore the probability of either hypothesis cannot be evaluated by looking at the p value alone. 

###Take-home
**Statistical significance, or the p-value,  is a tool for detecting an effect (detecting the signal against the stastical noise). It is *not* a tool for assessing evidence or determingin the importance. **


##Some practical problems with signifcance tests
###NHSTs dont't fucntion properly when statsitcal power is set to low or too hight. 

If a statistical power is set to low or to high, NHSTs don't function properly. A CI is superior to statistical power alone, because the CI  width can provide and indication of precision whit which an effect has been measured.

###Multiple Testing
Type I error, is the probability of rejecting $H_0$ when it is true. The probability of Type I error is equivalent to the significance criterion. As each test has its own Type I error, the error rate rises rapidly with the number of uncorrected tests. Perhaps, a more vexing problem that emerges in research is that as data about a number of variables is collected, even when the original hypothesis is not supported by the data. 

I suspect that many low to mid level scientists survive though successful storytelling. Weaving stories that are interesting enough to warrent publication around their data. A clever explanation rooted in  for an unexpected finding is a key element to good story telling. This in itself is innocuous enough, but is compounded by the lack of replications. 

One way around the issue is by declaring the both hypothesis and the primary outcome measure in advance. Ignoring new interesting trends in data, simply due their unexpected nature  however, may be wasteful


###Stoping Rule
A *p*-value  calculated for a significance test is only accurate if an appropriate stopping rule is in place. 

Sometimes data is collected until $p < \alpha$, or optional stopping. With sufficient resources, this strategy guarantees $p < 0$ even if $H_0$ is true. Sometimes this issue creeps subtle ways e.g. a reviewer asks to collect more data. This is arguable more problematic than multiple testing, in part due to the fact that this is a less apperant problem. 

###Take home
In summary some issues with NHSTs. 

1. neglect of statistical power
2. multiple testing
3. optional stopping

###Simple stopping rules for NHSTs and CIs
This is especially important in clinical trials where it is important to stop early if needed. e.g. Treatment effective, treatment not effective, treatment harmful.

**COAST (composite opent adaptive sequencial test)** Frick proposed fixing an arbitrary min *N* ($N_1$) and a significance \alpha range at which to continue, collecting,  stopping when  $p < \alpha_{lower}$ or $p > \alpha_{higher}$. $N_1$ is incremented in small batches. In simulations it was shown, that a for two  sided *t* test,  a true $\alpha$ close to .05  was maintained when $p < \alpha_{lower} = .01$ and $p < \alpha_{lower} = 0.36$. COAST  is fairly robust to changes in $N_1$, sample size, and incremental increase in $N$. COAST tends to have greater statistical power than fixed-sample rule
**CLAST compostie limted adaptive sequential test** A more efficient version of COAST implementing a stop when $N = N_{max}$ rule. $N_{max}$ is determined according to the fixed sample rule ($N_{FSR}$) with $N_{min}$ set as  ($\frac{1}{2} N_{FSR}$) and $N{max}$ set as  $\frac{3}{2}N_{FSR}$. Data are added in increments of size $N_2$
**CI stopping rule** Keep collecting data until observed width is narrower than the desired width ($W$). Using this approach it important to select a value of W that will always exclude either ES expected under H0 or   effect size you wish to detect

##Can the null hypthesis ever be true?
* Type I errors probably cannot occur for most studies 
* nil hypothesis is always false (Cohen) given a large enough sample size.

The $H_0$ is a single point on a continuum, and therefore  and infinitesimally small point on a line. Therefore the probability of it being true is 0. However, much research serves to identify invariances, e.g. speed of light. For such invariances the $H_0$ might serve as a useful proxy. Therefore a point null hypothesis is plausible. 

There are two arguments as to why setting up a point null hypothesis might be reasonable.

1. While some non-zero effect is almost certainly true, you might not know the direction of the effect. (we can reject the $H_0$ with a 2-sided test)
2. $H_0$ is a reasonable proxy for a negligible effect

##Frequentist responses to the NHST controversy

## Strict Neyman-Pearons inference.
Many problems with application of the NHST arise from the confusion of Fisherian with Neyman-Pearson inference. Neyman and Pearson aimed to develop a description procedure controlling for the long-run Type-1 and Type-II error rates for sets of tests.


1. Desired levels of $\alpha$ and $\beta$ should be determined in relation to the cost of Type-I and Type-II errors. Much research sets an  $\alpha = .05$ for statistical power and arbitrary $\beta = 0.20$ is common (power $1-\beta=.80$)
2. Practices that distort calculated p values addressed: by by adjusting $\alpha$ or adopting a stopping rule)
3. The interpretation of the test: The outcome outcome as in accepting  or reject $H_0$ 



### Suplementing frequentist inference
There are potential fixes to classical frequentist inference.
1. Increased use of CIS as an informal method provides a way to augment or replace NHSTs and p values. This fits well with the philosophy in which formal inference i to understanding of  the data
2. Increased emphasis on effect size as a way to supplement or correct the difference in significance tests. However, this may also be misleading, as under powered studies may produces large effect sizes despite being non-significant. 
3. Meta-analysis and replications

###The statsitcs of replicaiton






#Bayes's therome 

Bayes' theorem as an equation for dealing with conditional probabilities:


$$Pr(A|B) = \frac{Pr(A|B)(Pr(A))}{Pr(B)}$$


This equation can also be expressed as

$$Pr(A|B) = Pr(B|A)\frac{Pr(A)}{Pr(B)}$$


Lets say that lie detector test is being evaluated. Event **A** is lying  and Event **B** is failing the lie detector test.

If lies  are detected 99% of the time, then $Pr(B|A) =  .99$. In other words the probability of B (detecting a lie) given that A (one is lying) is true. 

If there is 2% false postie rate (detecting a lie when there is no lie), the probability of **B** given that **A** is *not* true is not true is $Pr(B|\sim A) = .02$

If we define **A** as 0.001, that is $PrA$, then the probability of A not being true is $Pr(\sim A) =  1-.001 = .999$. Therefore the probability of failing the test is the probability of B when someone is lying plus the probability when they are are not lying


Given that there are 2 outcomes for lying (lying or not), the probability of  *B*, failing is the probability of B, when someone is lying plus the probability when they are not lying. (simple multiplication of probabilities) 

$$Pr(B) = Pr(B|A)Pr(A) +Pr(B|\sim A)Pr(\sim A)$$

So the overall probability of failing the test is:

$$Pr(B) = .99 \times .001 + .02 \times .999  = 0.0297$$


For rare events, such as finding the liar, the $Pr(B)$ is dominated by the false positive rate.

Now that we know what $Pr(B)$, the probability of failing the test is, we can determine Pr(A|B): the probability of lying given that one has failed the test.

$$Pr(A|B) = Pr(B|A)\frac{Pr(A)}{Pr(B)} =  .99 \times \frac{.001}{0.2097} \approx .0407$$

Whenever $Pr(B|A)$ the equation reduces to the ratio  these two base rates: Pr(A) and Pr(B). In the context here, the test is not sensitive enough to be used for this application. 

In the context of Bayesian statistical inference, $Pr(A)$ is the priothe posterior r: provides information about how likely the outcome is in the absence of other data. $Pr(B)$, sometimes termed the normalizing constant, because it scales the result into a probability between the 1 and 0. 


The *prior* is a probability or probaility distribution that refects the degree of uncertainity of existing knowledge. The outcome of Bayeseian infrence is also a probability distribution * the posterior*

##The Baysian model
Baysiean infrence invovles modeling the posterior probability distribution $\theta$ as a function of the evidence provided by the data and a prior distribution  The quantity $\theata$ can be a single parameter or a set of parameters. 


With $D$ represting observed data:

$$p(D|\theta) = p(D|\theta) \frac{p(\theta)}{p(D)}$$


Where the term $p(D|0)$ is: Likelihood of the data given the distribution of $\theta$, and evidence provided about the data about $\theta)$. Therefore $p(\theta)$ and $p(\theta|D)$ are the prior and posterior distributiosn of $\theta$. The probability distribution $p(D)$ takes the role of the normalizing constatat. The normalzing constant ($p(D)$) does not need to be evaulated exactly, provided that its value is know up to constant factor that does not change wiht paramters


Thus the equation can be re writent as
$$p(\theta|D) \propto \ell(\theta | D) p(\theta)) $$
 That is: the **posterior probability** ($\p(\theta | D)$) is proportinal  to the likelihiood of $\ell(\theta|)D$ times the **prior** ($p(\theta)$)
 
 This equation summarizes what baysian inference doee: it combines prior knowledge with evidence from new data in a mathamatically coheren and optiaml way.
 
 Both likelhood theorists and frequnetists prefer to leavce out the prior out of fromal statiscal inferences. this has a number of drawbacks including:
 
 1. it ignores rather than solves the problem of intergrating prior infomation with new evicedece.
 2. the goal o fsome research is not weight evicedence from a single study but to make a descision about the best or most likely aoutcome (for whch prior infomration is essential).
 3. merly focusing on the evidence ignores the complexity of the model. an important  propertly of bayesisan inference is that it penalizes complex thories relative to simple ones
 

$p(\theta)$ is a probability distribuiton for a paramter. This paramter must sum up to 1 but can be allcoated in differnt ways. If we assume that $\theta =  1$ than it can be represteted with a normal distribution. $\sigma$ for this distribution can fall between $0$ (maximally informative prior) and $\infty$ (difuse or uninfomrative prior). A reasonable choice would fall in between these to


Bayesian inferences uses the prior distrubiton to calculate the weighted avarage liklhood  $\ell(\theta | D) p(\theta))$  for the model. If the probability distribution of the the prior is thinly spread, over a wide range of paramterr values, this means that the wieghted liklhood usded to determine the posterior distribution is also thinly spread. This weakens the evidential support for any particuliari value.  If the priror falls into a narrow range, the liklhood is focused around those parter values, increasing the support for them. this property is somtimes refered to as a fully atuomatic Occams razor/. 


All oter things being equal, chaning the $\sigma$ affects the posterior. The greater the variance of the prior, the less infomative it is.


### Selecting a prior
The choice of a prior is central to any Bayesian analsis. If there is no prior knowledge, the prior is difuse spread over all possible values and the posterir distribution is determined entirley by likelhood. 

Two main philosophies on selecting a prior.

1. Subjective Bayes: selection of a prior as a mater of personal belife or judgement e.g. objective opionion
2. Objective Bayes: selecting a prior that have some evidentila basis. Sill has some subjectivilty. Lack of confidencfe in the prior can be incorporated by adnjusting the $\sigma$ upwards. 

The choice o fprior is not limtted to the normal distribution. 

###Normal distributions with know variance
Depending on the complexity of hte modle, the distribution of paramters and the number of paratmers, the intergral my hava know solution or not. if there is no known solution, monte carlo methods can be applied. 

If the prior and and liklihjood are both normal, the posterior is also normal. Provided the variance of hte samlpe is known, there is a simle analytic solution. if the variance is unkown, an anlatical solution exists usoing the t distribution. 

The liklhood funtion for a samle from a nomal distributio wiht known vairnce can be expressed as:
$$\ell (\theta|D) \sim N( \hat{\mu}, \hat{\sigma}_\hat{\mu} )$$
If the priro elicited for the analsis is a normal distribution with mean $\mu_{prior}$ and a standard deviation $\sigma_{prior}$ then the posterior wil als be normal, its mean and SD is a funtion of $\hat{\mu}$, $\mu_{prior}$ and $\sigma^2_{prior}$. The variance of a the posterior distriubiton is. 

$$o^2_{post} = \bigg(\frac{1}{\hat{\sigma}^2_{\hat{\mu}}} + \frac{1}{\sigma^2_{prior}} \bigg)^{-1}$$

The quanity $\hat{\sigma}^2_{\hat{\mu}}$ is the variance of the sampling distribution of the data and its recipircal is of termed the precesion of the the sample. the recipircal of the prior variance is the precission of the prior. The ifnal step is the wieght of the mean of the prior and the sample by their respecitve variances. 

$$u_{post} = \bigg(\frac {\sigma^{2}_{post}}{\hat{\sigma}^2_{\hat{\mu}}}\hat{\mu} + \frac{}{\sigma^2_{prior}} \bigg)^{-1}$$


As the posterior distribution is normal it can be used for prediciton or to dervie an inteval estimate.  




```r
mtcars
```

```
##                      mpg cyl  disp  hp drat    wt  qsec vs am gear carb
## Mazda RX4           21.0   6 160.0 110 3.90 2.620 16.46  0  1    4    4
## Mazda RX4 Wag       21.0   6 160.0 110 3.90 2.875 17.02  0  1    4    4
## Datsun 710          22.8   4 108.0  93 3.85 2.320 18.61  1  1    4    1
## Hornet 4 Drive      21.4   6 258.0 110 3.08 3.215 19.44  1  0    3    1
## Hornet Sportabout   18.7   8 360.0 175 3.15 3.440 17.02  0  0    3    2
## Valiant             18.1   6 225.0 105 2.76 3.460 20.22  1  0    3    1
## Duster 360          14.3   8 360.0 245 3.21 3.570 15.84  0  0    3    4
## Merc 240D           24.4   4 146.7  62 3.69 3.190 20.00  1  0    4    2
## Merc 230            22.8   4 140.8  95 3.92 3.150 22.90  1  0    4    2
## Merc 280            19.2   6 167.6 123 3.92 3.440 18.30  1  0    4    4
## Merc 280C           17.8   6 167.6 123 3.92 3.440 18.90  1  0    4    4
## Merc 450SE          16.4   8 275.8 180 3.07 4.070 17.40  0  0    3    3
## Merc 450SL          17.3   8 275.8 180 3.07 3.730 17.60  0  0    3    3
## Merc 450SLC         15.2   8 275.8 180 3.07 3.780 18.00  0  0    3    3
## Cadillac Fleetwood  10.4   8 472.0 205 2.93 5.250 17.98  0  0    3    4
## Lincoln Continental 10.4   8 460.0 215 3.00 5.424 17.82  0  0    3    4
## Chrysler Imperial   14.7   8 440.0 230 3.23 5.345 17.42  0  0    3    4
## Fiat 128            32.4   4  78.7  66 4.08 2.200 19.47  1  1    4    1
## Honda Civic         30.4   4  75.7  52 4.93 1.615 18.52  1  1    4    2
## Toyota Corolla      33.9   4  71.1  65 4.22 1.835 19.90  1  1    4    1
## Toyota Corona       21.5   4 120.1  97 3.70 2.465 20.01  1  0    3    1
## Dodge Challenger    15.5   8 318.0 150 2.76 3.520 16.87  0  0    3    2
## AMC Javelin         15.2   8 304.0 150 3.15 3.435 17.30  0  0    3    2
## Camaro Z28          13.3   8 350.0 245 3.73 3.840 15.41  0  0    3    4
## Pontiac Firebird    19.2   8 400.0 175 3.08 3.845 17.05  0  0    3    2
## Fiat X1-9           27.3   4  79.0  66 4.08 1.935 18.90  1  1    4    1
## Porsche 914-2       26.0   4 120.3  91 4.43 2.140 16.70  0  1    5    2
## Lotus Europa        30.4   4  95.1 113 3.77 1.513 16.90  1  1    5    2
## Ford Pantera L      15.8   8 351.0 264 4.22 3.170 14.50  0  1    5    4
## Ferrari Dino        19.7   6 145.0 175 3.62 2.770 15.50  0  1    5    6
## Maserati Bora       15.0   8 301.0 335 3.54 3.570 14.60  0  1    5    8
## Volvo 142E          21.4   4 121.0 109 4.11 2.780 18.60  1  1    4    2
```

```r
library(ggplot2)
ggplot(mtcars, aes(mpg, cyl)) + geom_point()
```

![](notes1_files/figure-html/unnamed-chunk-1-1.png)<!-- -->




