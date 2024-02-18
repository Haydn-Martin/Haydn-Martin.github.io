# Robots Suck

Why is AI at the human-equivalent of a fully-grown (literate) adult linguistically but a toddler physically?

AI can do all types of wonderful things. From creating art, to writing (bad) poems, to making super-human predictions.
But it can't, yet, perform basic physical tasks. And when it can, it's torturous or fragile or at-least over-fit to those task.

[Moravec's paradox](https://en.wikipedia.org/wiki/Moravec%27s_paradox): 
counter-intuitively, reasoning requires relatively small amounts of compute.
Perception and mobility require lots.

More generally: the earlier some process evolved, the harder it is to train computers to do. This could be associated
with training time. We've been walking, bi-pedal style, for ~6 million years, but only writing code for ~100.
Hence computers are much better at writing code. Example: it is much harder to develop a robot to hunt a 
warthog in southern Sudan than to drive a car around Seoul.

More biology: we aren't anywhere close to understanding the human body and how it works.
We're still just throwing darts, trying to reverse engineer the processes. This might not be a
[good](https://www.cell.com/cancer-cell/pdf/S1535-6108(02)00133-2.pdf)
[idea](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005268):
it's incredibly hard to do for subconscious systems. We understand very well how chess works, less so
how our brains function.

And then also these complex, highly-evolved, constantly-adapting systems, are interacting with an open, itself-complex,
non-stationary system: The Real World. Consider walking across a park. It might be raining. It might be muddier than usual.
Stepping on a soft bit of ground will change that bit of ground. There could be dogs running around.
Etc. And that's just a 2-D problem, don't get me started on operations in a 3Dims. Compare walking with
the finite number of words we use. You can literally slap
all of these words (or tokens derived from them) into a big ol' vector. Done.
Whereas try this: how many ways were there of moving your right arm in a 1M^3 space?
[hence why of course we have to focus on getting things
roughly right: heavily discretise time and space, do as much reductio dimensiono as pos, etc.]

Another problem with these robot<>environment interactions is the reward function.
First: non-monotonic loss. Although this isn't a new problem, it's amplified in this domain. Consider again
walking across a park - simply moving forward might not be necessarily a good thing (collapsing forward will give you that),
what you really want is the best combination of movements that drive you the most forward, and in a sustainable way.
You need a lot of search space exploration. And that's just for a simple task. Imagine cooking a pizza from
scratch - how exactly do we gradient descent here?

There are signs of improvement. [MuZero](https://www.nature.com/articles/s41586-020-03051-4.epdf?sharing_token=kTk-xTZpQOF8Ym8nTQK6EdRgN0jAjWel9jnR3ZoTv0PMSWGj38iNIyNOw_ooNp2BvzZ4nIcedo7GEXD7UmLqb0M_V_fop31mMY9VBBLNmGbm0K9jETKkZnJ9SgJ8Rwhp3ySvLuTcUr888puIYbngQ0fiMf45ZGDAQ7fUI66-u7Y%3D)
lays out a general-purpose algorthm that learns a model that
explains the environment, by learning its most important features.
Their [most-recent Robotics Transformers](https://deepmind.google/discover/blog/shaping-the-future-of-advanced-robotics/) 
also look promising (although it can be hard to tell with robotics how real
things are. Demos can be deceiving). Obviously other cool stuff from
Tesla, with [Optimus Gen 2](https://www.youtube.com/watch?v=cpraXaw7dyc&ab_channel=Tesla)
, and Boston Dynamics with their [Atlas model](https://www.youtube.com/watch?v=-e1_QhJ1EhQ&t=5s&ab_channel=BostonDynamics).

It seems RL is simply lagging behind other methods.
We haven't figured out a good way to program self-improvement, in complex environments, without
human feedback. There might be a sense in which we're optimising too much:
in some cases it's easier to train a model to optimise for a loss function than to define the loss function in the
first place. Life Philosophy Parallelism: START{_in some cases it's easier to get what you want out of life
than to figure out what you want in the first place_}END .

Even this whole loss function thing might be wrong. How, or, more importantly, _why_ do humans learn? It's not via pain, or loss.
We explore. We mess around. We play. We are attracted to what interests us. We don't really optimise, at all levels of biological complexity.
There's a reason you have 2 lungs (and 2 kidneys). Engineers would point out that we could greatly _optimise_ the _efficiency_
of the human body by removing this "superfluous" duplication. Optimisation = necessarily loss in robustness = exit gene pool (eventually).
And we over-fit, making quick-and-dirty inferences left right and Chelsea that are usually wrong. Because, again, we are not "designed"
to be correct/efficient/optimised/the best, just to survive (and pass on genes).  How this relates to learning, though, which is where
this point started (oops), is not clear.

But I get the feeling this still doesn't fully explain the fact that my fridge is more likely to be able to accurately predict
what food I want to buy next week and order it for me than for some robot thing to boil me an egg.

What's missing is socioeconomic stuff, specifically the concentration of talent working on these respective technologies.
Cast your mind back to the hunting vs. car-driving problem. If we had lots and lots of engineers working on the former, we might be
getting somewhere. General point: we are more interested in bits than atoms. People with
engineering and science degrees aren't working in labs or building machines. They're writing code.
Things that only require code to build, are far more likely to get built.