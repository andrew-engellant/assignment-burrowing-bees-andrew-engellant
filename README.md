# Burrowing Bees

In this assignment, you're asked to simulate 
an experiment done by a biologist researching bees to see 
if the results the biologist saw are the results of chance.

The markdown file `burrowing_bees.rmd` holds the initial data
and the questions for you to answer. 

## Feedback 

You write: 
> This is lower than the actual proportion observed by the researcher, who found that all four bees burrowed in their own holes ‘r ones_actual * 100’% of the time.
>

But I think that's just showing up because of a formatting error, since the fraction is 18.9%. If you have the `scales` library installed, then you can write something like `r percent(ones_actual)` and get a properly formatted percentage. 

Your `result_table` DF looks, essentially, perfect. The use of "right-sided" threw me for a second, but once I read your code I understand what you're doing and I have no disagreements with the approach. Your commentary under the table is excellent. 

You ask
> Why might I be getting significance for both a higher proportion of 4,0,0,0 and 1,1,1,1?
>

I don't know much about bees, but from the data it appears the "all in one" or the "all different" is popular with the bees. What we're seeing in the data is a preference for these extreme cases over the "middle" ones. 

You then ask
> For the simulation, since the researcher performed 37 trials, should my simulation also use 37 trials and then whatever number of simulations I prefer? Or can I choose to use something like 100 trials?

I like what you did and I think simulating these groups of 37 is the best way to do this. I've also been fine with students just simulating thousands of releases to get the proportions, and then doing some sort of `prop.test`. But I think mimicking the "release 37 bees" is the cleanest way to do the analysis if you were trying to convince someone you were right. 

Finally, I much prefer using your simulations to estiamte a p-value than using the parametric approach with `pnorm`. In this case either will work fine, but you're making fewer assumptions by using the permutations. Great work on this!
