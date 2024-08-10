# 90% of Statistical Errors

Most people don't need to know statistics.

This is a good thing.

The world would be a very boring place if everyone knew what Markov's inequality was.

But everyone could do with a basic understanding of the most-common statistical traps.
Understanding of these will have practical consequences for you in every-day life.

Luckily, there aren't that many, and they aren't that hard to grasp.

### What do the numbers actually say?

Before letting data inform your decisions, it's good to know what the data actually is.

Sounds simple, right?

But journalists, scientists, salesmen, etc. have all figured out sneaky ways to massage data to
do their evil bidding.

There are some common places that these techniques are deployed:

Headline --> EATING RASPBERRIES INCREASES THE CHANCES OF THUMB CANCER BY 10%. Let's say this is true.
Ok. Fine. I never liked my thumbs that much anyway. But as we read on we discover that this type of
berry consumption increases our chances from 0.000001% to 0.0000011%. So the headline is technically
correct but kind of misleading. Or let's say this study was conducted on left-handed, 65-year-old women.
I would quite like to know that before declaring war on raspberries. Ignore the headline and try and focus on
the data in raw form.

Visualisations --> people choose the timeline, axes, colours, etc. to best sell whatever it is they are trying
to sell. There are many tricks here ([check out the wikipedia page!](https://en.wikipedia.org/wiki/Misleading_graph))
but the most common is probably the choice of
axes: magnifying axes to increase the perceived effect size and shrinking them to diminish it.

Something like this:

<img alt="Huge Spike in Average Home Prices" src="_posts/misleading_chart.png" />

_[Source](https://www.ck12.org/c/statistics/misleading-graphs-identify-misleading-statistics/lesson/Identification-of-Misleading-Statistics/)_

Apparently there is a "Huge Spike" - but is 250000 to 252000 really huge?
It certainly looks big. But look at the y-axis! It's been truncated such that the max is 252000
and the min is 249000. You can make any difference appear large by using this trick.

Numbers --> issues with numbers stated in the actual text are less obvious. The violations are harder to spot.
You usually have to ask yourself more nuanced questions such as where did the data come from? Does this apply to
me? What are they using as the definition of that? Was the experiment soundly designed?

### How much data?

The next thing to consider is how many observations people are drawing conclusions from.

Consider thumb cancer again - if this is based on a study of 3 people, I'm not likely to be that interested.
Why? Not because this means that the results, or even the conclusions drawn from them, are wrong, it's that
we have no reason to believe they are right.

This is a mistake of generalising from the particular, of assuming something will apply to everyone (including you)
because that was the effect observed for some other group. This is not always true, particularly if that group is small.
These errors happen all the time. Person of type X did this bad thing = everyone of type X is bad. This thing worked
for my friend = it will work for me. This person got rich doing this = I will get rich doing this.

We can explain using a weird hypothetical experiment.

Imagine your friend tells you that he ate a raw onion before bed last night and he slept like a baby - will
you sleep well if you do the same? We don't know. There are a whole host of explanations other than
onions cause good sleep. If he has been doing this for 20 years, with many different periods of eating and
non-eating, with precise ways to measure sleep quality I might
be more inclined to believe him. Similarly, if everyone on Earth did this experiment and slept well,
I might be more inclined to draw the same conclusion.

That's the idea of sample size. We have some [statistical definitions](https://en.wikipedia.org/wiki/Statistical_significance)
of what results are "significant" and how
many samples should be observed (for some things), but the general point is to be aware of how many samples/observations
are being used.

### Just because two things happened at a similar time, doesn't mean that they are in any way related

Not much explanation required here. I'll just list some random examples for fun:

- Lucky socks and passing exams
- Blowing on dice and winning craps
- Playing the left back higher up the pitch and going on a win streak
- The position of Jupiter's moons when you were born and your level of conscientiousness
- The price of Barclays Bank PLC and WTI Crude Oil
- Increase in sales in H2 after a digital marketing campaign
- Economic boom under Prime Minister X

Statisticians call this lesson _correlation is not causation_. Meaning that even if two things move in
conjunction with one another, this does not necessarily imply that one is in any way causing the other.

### Someone has to win

Let's say we have a lots of data. A big sample size. Plenty of numbers.

As discussed above, this is usually a good thing because we are usually more confident
aggregate outcomes are true, and we can test the robustness of individual outcomes.

But as one door closes, another opens. When the sample size is large, extraordinary outcomes
are likely to occur purely by chance.

Three specific ways this annoys me:

**What are the chances?!** Did you ever see someone from your school on holiday
and everyone completely lost their shit? Seemingly understandably - what are the chances
of seeing that person that I know from England here in this exact location here in Spain
at this exact time? Very low. But that's not what happened - you're seeing someone one of
you - in the family - has met before. This is a lot of people. You're bound to bump into someone that you know.
(Especially given that people you know read the same things, talk to the same people,
work in the same industries, send their kids to the same schools, etc. as you. There are only
so many popular destinations, recommended hotels within those locations, and convenient
weeks to go to those locations. So, Mum, what are the chances? Quite high, actually.
More on this later.)

**It can't be luck.** The chances of my flipping 5 heads in a row right now is very low.
If I bet you £30 that I can, and then proceed to do so, it's very likely that I have
skill in flipping heads (on this occasion skill being a biased coin).
But if you ask >16 people to do this, someone is
likely to flip 5 heads in a row just by chance. Or a real-world manifestation: if
500 companies are betting on which companies will succeed or not, a few of them are likely
to make good predictions over an extended period of time...just by pure luck.

**P-hacking.** When people are conducting experiments, they are often concerned about whether
their results occurred by pure chance, or if some type of significant effect
altered the outcome. If your experiment is well-designed, this statistical significance
is easy to calculate. But what if I do several experiments? My p-value (just a way
of measuring statistical significance) indicates that there is a 5% chance the
results would occur by luck (loosely speaking). Now what happens if I do the experiment >20 times? It's
likely I would get a "significant" result, even though a true effect is not present. You may not
think this is a problem but [consider](https://www.youtube.com/watch?v=42QuXLucH3Q&t=1s) 1) scientists
are massively incentivised to produce
significant results so that they can publish those results and 2) there are loaaaads of experiments
and studies going on all the time.

### What conditioner do you use?

_Note: awareness of [conditional probability](https://en.wikipedia.org/wiki/Conditional_probability)
required here. Skip at will._

Consider the sighting of the holiday friend again.

My Mum was considering the probability of seeing one exact person, not conditioning on anything:

P(Seeing Person X) = 1/population of planet Earth --> veeeeeeery small

Hence her shock. She wasn't taking into account the fact that this person was very similar:

P(SPX &#124; X is a very similar person) --> a loooooot higher

Or that she would have a similar reaction to anyone we knew (which is 1 - the probability
of not seeing any of those people):

1- [(1 - P(SPX &#124; X is a  very similar person)) * (1 - P(SPY &#124; Y is a very similar person)) * ...]

With 100 people where P(SPX) = 0.01, the chance of seeing someone is over 60%.

People make this type of error all the time. The other classic (and by classic I mean
makes me pull my hair out, hence my lack of hair now) is "more likely to" "facts":

"You're more likely to be struck by lighting than be attacked by a shark."

Apparently this is a fact.

And it is in some sense: it's based on the fact that more people **globally** get hit by lighting than attacked by a shark.
But this is a misleading, pointless, dangerous tidbit that doesn't explain anything and has no value
except as "fun fact" fodder.

Because it entirely depends on what circumstances you find yourself in. If I go swimming off the coast of South
Africa every day, my chances of shark attack go up substantially.

### Behave!

This last point is relatively technical. Some (relativity) high-level shit. If you understand this
you'll be more statistically aware than like 90% of the general pop. And probably more (suitably)
skeptical than 90% of the pop that uses data.

Due to my lack of imagination, let's re-consider a previous example again: flipping lots of coins.
Recall we could be very certain (in probability) of characteristics of our coin-flip experiment. We knew
five heads was unlikely, for example. Why and how do we know this?

Firstly it's because the distribution of outcomes is easy to work with. It is --TECHNICAL TERMINOLOGY ALERT--
bounded, with finite mean and variance. These are nice properties that are handy to have when
performing calculations.

Implicit in this calculation also is the idea that the coin will not change in its distribution of outcomes.
If we changed the coin for one that had heads on both sides, the chances of flipping head 5 times in a row changes
quite a bit.
