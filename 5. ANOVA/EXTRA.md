# ANOVA Extraly 
Here, I will be noting down the stuff that I have learnt from this amazing [video series](https://www.youtube.com/watch?v=0Vj2V2qRU10&list=RDCMUCFrjdcImgcQVyFbK04MBEhA&start_radio=1&rv=0Vj2V2qRU10&t=135). That has all videos concentrated to ANOVA from first introduction to the calculation for its types. 

Let's understand ANOVA again.
___
<font size=6><b>W</b></font>e are comparing the **variances** in ANOVA. And the `f` it self is the ratio. 
- ANOVA allows us to compare beyond just 2 populations
- We can investigate how 2 groups interact with each other quantatively. 

**Reason of Not using `t test`:**
With the pairwise approach, the ***error COMPOUNDS with each t-test***.

### When question arises
We have (let's say) 3 samples.

![enter image description here](https://i.imgur.com/mXUQ8xk.png=200x200)![enter image description here](https://i.imgur.com/VwzXi2g.png=200x200)![enter image description here](https://i.imgur.com/QkXi6vu.png=200x200)

**So, generally we question that**: 
> Do all three of these means come from a common population?

**The general possibilities can be**:
1. One distribution's mean is so far from the other two then, that is likely not from the same population.
2. Or all three means are so far apart that all of them are from distinct population

Now, we take **all data points** and make the ***single*** distribution:
![All to One](https://i.imgur.com/n58NHcV.png)
Now, try to understand. We have ***clubbed*** all samples in to single data and then we have tried to get the common mean. The common mean is the dashed `--` line in the middle.

Recall from the ANOVA Base, we did the same by calculating the mean of all individual samples and then tookout the mean of those means. That operation is done just below ↓

## Variability Between Groups
![Among Variance](https://i.imgur.com/f8HzhoN.png)

We can see that we are looking at the **SSG** the sum of squared of groups. Here ↑ we are measuring the distance of individual samples to the mean of all samples combined.

![Oddball](https://i.imgur.com/4CxQXY8.png)
Here ↑ if one of the samples is so far from the mean, the SSG will be larger. *Which means the $\bar x_3$ belongs to its own population.*
___
Now, we will make a Null Hypothesis.
Which always is "All Samples are the same ~ All belong to the same population".

$H_0 = \text{All samples come from the same population}$
$\therefore H_0 : \bar X_1 = \bar X_2 = \bar X_3$

We are not asking if they are **exactly** equal. But we are asking whether or not are the **likely to come** from the larger overall population.

><font size=6> It is called "Variability <B>BETWEEN / AMONG</B> the sample means" </font>

Which I call the **Group Variability** — **SSG**.


## Variability Within Groups
><font size=6> It is called "Variability <B>WITHIN / AROUND</B> the samples" </font>

It is what I call **"Internal Variability"** — **SSI**.

## ANOVA is a Variability Ratio
It has the core formula to find `f` which in turn a ratio!
### $$ F = \frac{\text{Group Variability}} {\text{Internal Variability}}$$

![Variability Ratio](https://i.imgur.com/n1CM2mc.png)

### Combine 2 variances
If we try to combine 2 types of variances *(Group Variability + Internal variability)* then we get the **Total Variance**.

$$\text{Group Variability} + \text{Internal Variability} = \text{Total Variance}$$

> It is called "Partitioning" — Separating total variance into its component parts.

### The consequences of magnitude in $F = \frac{\text{Group Variability}} {\text{Internal Variability}}$
- If the numerator is high $\frac{\text{LARGE}}{\text{small}}$, then **Reject $H_0$**
	- At least one mean is an outlier
	- Distribution is narrow
	- All distinct from each other

- If the numerator is small $\frac{\text{small}}{\text{LARGE}}$, then **Fail to Reject $H_0$**

	- Means are very close to overall mean
	- Distributions melt together

- If the numerator is small $\frac{\text{similar}}{\text{similar}}$, then **Fail to Reject $H_0$**
	- Fairly close to overall mean
	- Samples overlap a bit, hard to distinguish

The overall process:
![Summary](https://i.imgur.com/AuYJeQH.png)
___
# One Way ANOVA
Wai, 1 Way? Yess, it is one of the types of ANOVA. Not a big fuss, let's check it out. *(I just realized that in this sentence I have used 7 punctuations!)*

It is also called:
> <font size=6> One Way ANOVA = "Single Factor ANOVA"


<u>**Quick Example**:</u>
- 21 students selected from FY, SY and TY in college (7 from each)
- They gave the exam of 100 marks

We want to see if there is the significant difference in their scores based on their level ie. F, S, T?

**This is the One - Way ANOVA** because the there is ***only one property*** by which we are selecting the student — "The Study Year". If there were 2, then it would be 2 way ANOVA (which is the topic of another section).

Now, data:
$\text{FY} = \#_1,~\#_2,~\#_3,~...,~\#_{21}$
$\text{SY} = \#_1,~\#_2,~\#_3,~...,~\#_{21}$
$\text{TY} = \#_1,~\#_2,~\#_3,~...,~\#_{21}$

The same procedure is followed:
1. Get the **means** $\bar x_1,~ \bar x_2,~ \bar x_3$
2. Get the **total mean** $\bar x_\text{total}$
3. Find the **SSG**
4. Find the **SSI**
5. Here **SSG + SSI = Total Variance**
6. Total Variance can be found by *Getting difference between each individual data points from all samples and subtracting them from the $\bar x_\text{total}$*. 
7. But we **don't** have to find that Total Variance as SSG + SSI will give us the same.
8. Calculate the **degree of freedom for Groups**
9. Calculate the **degree of freedom for Internals**
10. Get the F score
11. **Reject** or **Fail to Reject** the Null Hypothesis based on the check. *(If calculated F score is less than the critical value then we Fail to Reject and conclude that "There is no significant difference between the sample means and they are likely to come from the same population.")*

> And calculating the example of students, we came to know that ***we fail to reject the null hypothesis*** and as their means are same, their level of study doesn't affect the score. The scores are relatively same no matter what is their level of study.

*Not a single change in formulae is there compared to the ANOVA taught by Jose in `1. ANOVA` and `2. ANOVA Example` files. Here I am just laying out the steps and not describing it  as they are the same.*

Now in this video series, just in `F` formulae the tags are given which we directly put values to in the Jose's version. Things are the same, just differ in the terminology.

Here,
$$F = \frac{MSC}{MSE}$$

Where,
$$ MSC = \frac{SSG}{df_\text{groups}} ~~~~~~~ MSE = \frac{SSI}{df_\text{internals}}$$


In Jose's version, we directly put the numbers without calling the MSC and MSE.
There,
$$F = \frac{\frac{SSG}{df_\text{groups}}}{\frac{SSI}{df_\text{internals}}}$$

**Fine!**

See,
**Sum of Squares** is the foundational component of ANOVA. We just do sum of square and avoid taking average as we do in calculation of variance. *(SSG / SSI)*.

