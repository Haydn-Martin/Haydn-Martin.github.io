# Title

Most people don't need to be fully acquianted with statistics.

This is a good thing.

The world CHECK would be a very boring place if everyone knew what STATISTICAL THEORY was.

BUT everyone could do with a basic understanding of the most-common statistical traps.
Understanding of these will have practical consequences for you in every-day life.

Luckily, there aren't that many and they aren't that hard to understand.


### What do the numbers actually say?

This might sound utterly redundant to express but:

Before letting data inform your decisions, it's good to know what the data...actually...is.

Sounds simple, right?

But journalists, scientists, salesmen, etc. have all figured out sneaky ways to massage data to
do their evil bidding.

There are some common places that these techniques are deployed:

Headline --> EATING RASBERRYS INCREASES THE CHANCES OF THUMB CANCER BY 10%. Let's take this as true.
Ok. Fine. I never liked my thumbs that much anayway. But as we read on we discover that the type of
berry consumption increases our chances from 0.000001% to 0.0000011%. So the headline is technically
correct but kind of misleading. Or let's say this study was conducted on left-handed 65-year-old women.
I would quit like to know that before declaring war on rasberrys. Ignore the headline and try and focus on
the data in raw form.

Visualisations --> people choose the timeline, axes, colours, etc. to best sell whatever it is they are trying
to sell. There are many tricks here (check out the wikipedia page!) but the most common is probably the choice of
axes: magnifying axes to increase the perceived effect size and shrinking them to achieve the opposite effect.

Something like this:

![img.png](img.png)
_Source: https://www.ck12.org/c/statistics/misleading-graphs-identify-misleading-statistics/lesson/Identification-of-Misleading-Statistics/_

What did we learn about headlines? Apparently there is a "Huge Spike" - but is 250000 to 252000 really huge? Less than 1%?
Looking at the chart, it certainly looks big. But look at the y-axis! It's been truncated such that the max is 252000
and the min is 249000. Bastards. You can make any difference appear large by using this trick.

Numbers --> issues with numbers stated in the actual text are less obvious. The violations are harder to spot.
You usually have to ask yourself more nuanced questions such as where did the data come from? Does this apply to
me? What are they using as the definition of that? Was the experiment soundly designed?

### How much data?

The next thing to consider is how many observations people are drawing conclusions from.

Consider thumb cancer again - if this is based on a study of 3 people, I'm not likely to be that interested.
Why? Not because this means that the results, or even the conclusion drawn from them, is wrong, it's that
we have no reason to believe they are right.

This is a mistake of generalising from the particular, of assuming something will apply to everyone (including you)
because that was the effect observed for some other group. This is not always true, particularly if that group is small.
These errors happen all the time. Person of type X did this bad thing = everyone of type X is bad. This thing worked
for my friend = it will work for me. This person got rich doing this = I will get rich doing this.

We can explain using a simple hypothetical experiment.

Imagine your friend tells you that he ate a raw onion before bed last night and he slept like a baby - will
you sleep well if you do the same? We can't conclude much from this. There are a whole host of explanations other than
onions cause good sleep. If he has been doing this for 20 years, with many different periods of eating and
non-eating, with precise ways to measure sleep quality, and significant differences in sleep every time, I might
be more inclined to believe him. Similarly, if this was the whole world doing this experiment and relaying the
same result, I might be more inclined to draw a conclusion.

That's the idea of sample size. We have some statistical definitions of what results are "significant" and how
many samples should be drawn (for some things) LINK, but the general point is to be aware of how many samples/observations
are being used to make conclusions.

### Just because two things happened at the same time, doesn't mean that they are in any way related

Not much explanation required here. I'll just list some random examples for fun:

- Lucky socks and passing exams
- Blowing on dice and winning more DICE GAME
- Playing the left back higher up the pitch and going on a win-streak
- The position of jupyter's third moon and your level of concientousness CHECK
- The price of Barclays Bank PLC and WTI Crude
- Sales boost in Q4 after mandating return to office
- Economic boom under prime minister Y CHECK

Statisticians call this lesson _correlation is not causation_. Meaning that if the level of two things moves in
some way in conjunctions with one another, this doesn not necessarily imply that one is in any way causing the other.

### Someone has to win









