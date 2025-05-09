# Pure Statistical Inference Is Pointless

Imagine your boss sends you a CSV with a _y_ column and a bunch of _x_ columns. 
No context, just the columns and data within them.
The instruction is to give them a way to predict the values of some unknown _y_.

Easy, right?

Use the standard statistical methods, model the relationships, give them what they want.
Job done.

But what this won't tell your boss is how _good_ or _effective_ or _useful_ that information is.
Worse: you can't even tell how useful _it is likely to be_.

The _only_ thing we can get from _just_ data is the statistical attributes of that
sample data. That's it, everything else requires explanatory knowledge of the 
data and environment.

And those statistical attributes of the sample are, by themselves, pointless.

Because we only get a _sample_ from the true distribution, not the distribution
itself. We can't say much about it.
We are blind to the true generating function.

---

Imagine a very simple scenario: a column of all 1s.
Even here, we can't even say anything about
how likely it will be that an unobserved _y_ will have the value of 1 for that column
without extra-statistical information about that variable.

We need to have knowledge about the data itself and how it is generated.
We need to know what we're conditioning on. 
This is why a _purely_ frequentist approach to statistics doesn't make sense.
Even flipping a coin requires a huge amount of background knowledge about the possible
outcomes, the environment, the mechanism of flipping, etc. Statistics don't exist
in a vacuum.

Inference is only possible if the unobserved reflect the observed.
If the future resembles the past. The data itself cannot tell us this, we need
context knowledge to do it.

A trivial example could be daily turkey sales. Infer based on January-November data
and predict for December.

There are non-silly examples in reality, too.

Consider football analysis in which
it is advised to have more players in the box at a corner because, looking at the
data, there is an inferred relationship between this number and the probability of
scoring from a corner. But this misses the fact that teams can adjust to what you're doing.
This _might_ be a good tactic, but we only know if it is with domain knowledge.

One could imagine discovering a relationship between certain days of the month and
FTSE 100 performance. Fair enough. But we'll only know if this is worth using,
if it is likely to be true in the future, with an explanation using domain knowledge.

This is why domain expertise is essential. You can't do data science without it.
