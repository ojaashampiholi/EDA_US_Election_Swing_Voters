EXPLORATORY ANALYSIS ON SWING VOTERS IN US ELECTIONS

The thinktank Data for Progress collected survey data (in DFP WTHH release.csv) that represents the population of people registered to vote in the 2018 midterm elections. We wish to study swing voters. Deﬁne the following groups:

• Loyal Democrats: People who voted for Hillary Clinton in 2016 and a Democratic House candidate in 2018. 
• Loyal Republicans: People who voted for Donald Trump in 2016 and a Republican House candidate in 2018. 
• Swing voters: All other people who voted in 2018. In addition, deﬁne the following two subsets of swing voters: 
• Switch to D: People who didn’t vote for Hillary Clinton in 2016 but voted for a Democratic House candidate in 2018. 
• Switch to R: People who didn’t vote for Donald Trump in 2016 but voted for a Republican House candidate in 2018.

Note that some swing voters don’t fall into either of these two groups, i.e. some people didn’t vote for either a Republican or a Democratic House candidate in 2018.

Basic variables 
• presvote16post: 2016 Presidential election vote. 1 means Clinton, 2 means Trump, 3–7 or NA means voted for someone else or didn’t vote for President in 2016. 
• house3: 2018 House of Representatives vote. 1 means Democrat, 2 means Republican, 3 means other.
• weight DFP: survey weights. You should use these!

Issue variables
Respondents were asked to give their support for the following programs on a 1–5 scale, where 1 means strongly support and 5 means strongly oppose. (6 means “Not sure.”)
• M4A: Medicare for All 
• GREENJOB: A Green Jobs program 
• WEALTH: A tax on wealth over $100 million 
• MARLEG: Legalizing marijuana 
• ICE: Defunding Immigration and Customs Enforcement 
• GUNS: Gun control 1 The codebook (http://filesforprogress.org/datasets/wthh/WTHH_Core_and_DFP_modules. pdf) contains full question wording for all issue variables.


Populism variables
Respondents were asked to indicate their agreement with the following statements on a 1–5 scale, where 1 means strongly agree and 5 means strongly disagree. (6 means “Not sure.”)
• POP 1: “It doesn’t really matter who you vote for because the rich control both political parties.” 
• POP 2: “The system is stacked against people like me.” 
• POP 3: “I’d rather put my trust in the wisdom of ordinary people than in the opinions of experts and intellectuals.”

Questions to answer
First you need to create three subsets of the data: Switch to D voters, Switch to R voters, and Swing Voters. The code in DFP.Rmd does this (creating data frames switchD, switchR, and swingers), or you might prefer to do it yourself. Then answer the following questions:

1. How do Switch to D and Switch to R voters diﬀer on the issue variables? On which issue variables do Switch to D and Switch to R voters diﬀer a lot? On which issue variables are they reasonably similar? Describe these diﬀerences.

2. How do swing voters diﬀer from loyal Democrats and loyal Republicans on the issue variables? Some hypotheses might be:
• Swing voters are moderates, and tend to the in the middle of the distribution when Democrats are on one side and Republicans are on the other. 
• On most issues, swing voters are split, with some of them acting more like Democrats and others acting more like Republicans. 
• Swing voters think more like Democrats on some issues and more like Republicans on other issues. 
• Swing voters are ideologically incoherent and don’t have consistent patterns in their issue positions.
Which of these hypotheses (or which mixture of them) ﬁts the data best, and for which issues?

3. What predicts being a swing voter? Build two models to probabilistically predict whether a registered voter is a swing voter: 
• One model should use ONLY the issue variables as predictors. 
• The other model should use ONLY the populism variables as predictors.

Clearly display both models, showing how the predicted probability changes with each predictor you include. How well do your models do? Which of your models does better? If you had to guess, what factors are most important in determining what makes a voter a swing voter?

Note: You don’t have to ﬁt the best possible models, just sensible and interpretable ones. You should try to have some idea of how good your model is, although it may not be possible to improve classiﬁcation error if nobody has a suﬃciently high probability of being a swing voter.
