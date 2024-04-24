# Random Questions

Unfortunately outputs of some process X can't tell us much about if some process X is random or not.

We can't tell with certainty if something is random. Is this sequence random [1, 2, 3, 4]?
Did I get these number by adding 1 to subsequent steps starting at 1 or by just randomly selecting
numbers 1 to 10?

We can't even say with probability if something is random.
Another sequence: [1, 2, 7, 4]. What's the probability that this is random?

We have no idea. Without knowing the underlying generating function, we can't say
anything about the probability of randomness. Sequences that appear random might have a deep
underlying pattern that we can't detect.

Or maybe we can?
We do have mathematical techniques to attempt to determine this.
One can look at things like the frequency on integers and integer sequences
across multiple bases. Equally-frequent 1-10 (in base 10) and 0/1 (in base 2),
(1, 2), (2, 3), (3, 2, 9), etc. etc. etc. over a large number of observations would
seem to indicate that the outputs of the process are in fact random.

What about determining if a process is _not_ random?
Using similar reasoning: is the above sequence definitely not random?
Impossible to say just using the observations.

There is one saving grace, one way in which outputs can be useful.
They can tell us if some process is _probably_ not random.

Sequence in base 2:
[1, 0, 1, 0, 1, 0, 1, 0, 1, 0]

Sequence in base 10:
[1, 2, 3, 4, 5, 6, 7, 8, 9]

Selections from a category (animals):
[lion, lion, lion, lion, lion, lion]

In all these examples, there seems to be an explainable pattern that can be used to predict future
observations. This explanation is better (in probability AKA more likely) than simply referring to 
these sequences as random, and the
observations from these sequences are very unlikely without this non-randomness:
[1, 2, 3, 4] --> [5, 6, 7, 8]

I can explain this process by stating that to get the next observation one must add 1 to the previous
observation, and use this explanation to predict the next 4 values. If these next 4 observations occur, it
seems more likely that my explanation of the process is correct, rather than the purely random
explanation.

It's difficult to quantify/define this exactly, but it is real.

What's less clear is semi-random sequences: random processes:
[1, 1, 1, 1, 1, 1, 1, 1, 1, 1]

Here the best explanation seems to be that this sequence only contains 1s.
But we could just as easily say that this is a _stochastic process_, with 1s
being drawn from a distribution in which the probability of a 1 is very high.
You might say that the former is a better explanation invoking some Occamic
argument. But this can get us into trouble.

Trouble:
[2, 4, 1, 3, 2, 3, 2, 1, 3, 4]

The best-seeming explanation here could be that these observations come from a
process that equi-probably spits out numbers 1-4. But what if larger numbers
are possible just with low probability? We have no way of knowing if that's a possibility,
and can't be certain that it's not, even with a huge number of observations.
This is why understanding the underlying 
mechanism is vital, and relying purely on observations is troublesome.

But do we always need to do that? Contrast the above example with the following:
[2, 4, 6, 8, 10, 12]

What are the next 5 observations? In some sense we don't _need_ an explanation
(other than the sequence will continue). We just extrapolate purely from
past observations (as in literally draw a line through them and extend it).

And sort of by definition if something is predictable, it's not random.
Although note the opposite might not be true: if something is non-predictable, 
it might not be random.

An example is any process that Steven Wolfram has dubbed [computationally irreducible](https://mathworld.wolfram.com/ComputationalIrreducibility.html).
To figure out the output at time t, you need to "run" the "programme" until time t. There's
no other way of knowing/predicting what the output will be otherwise. Sounds like randomness, right?
But it's not - these processes are often based on simple deterministic rules.

But then even though the process itself isn't random, could the outputs be? Yes. They can be explained, _but not predicted_. Another example of this is pseudo-random
numbers: they are generated as the result of a deterministic mechanism but seem to have lots
of attributes of random numbers.

Another way of assessing randomness is compressibility: any sequence that can't be compressed - represented
in a smaller (like [Kolmogorov complexity](https://en.wikipedia.org/wiki/Kolmogorov_complexity)
smaller) way - is random. Relating to the above: computationally irreducible
processes can be generated via simple deterministic mechanisms, hence represented in a highly compressed way.
The same is true of pseudo-random numbers. But the way to get to the observation at time t can't be (compressed),
you still have to run the process until t. Hence incompressible. 

What about irrational numbers? Something like Pi or sqrt(2) can be _represented_ in a compressed way (by using symbols)...but
that's not really the same thing as compression. Pi's _calculation_ can
be expressed in a simple way 
(see [Euler](https://en.wikipedia.org/wiki/Euler%27s_identity), 
[Ramanujan](https://en.wikipedia.org/wiki/Ramanujan%E2%80%93Sato_series), etc.) 
And yet its digits seem random (i.e. it's [normal](https://en.wikipedia.org/wiki/Normal_number)).

This could be in some way related to intelligence. Intelligence is the ability to understand, abstract, explain, 
and apply across a variety of domains (my definition). Random processes are those which
we can't understand/explain, can't create abstractions or representations from, and can't learn to apply patterns or
behaviours to other processes. 

How about things in the physical world? Do CO_2 molecules move randomly
in our atmosphere? Could their movement be calculated if only we had enough compute and accurate-enough
measuring devices?

Maybe. Laplace, extrapolating from Newton, certainly [seemed to think so](https://en.wikipedia.org/wiki/Laplace%27s_demon).
But then Heisenberg and Schrödinger
cast doubt on that belief with the 
[uncertainty principle](https://en.wikipedia.org/wiki/Uncertainty_principle)
and [Schrödinger equation](https://en.wikipedia.org/wiki/Schr%C3%B6dinger_equation), 
respectively. 

Complexity science has shown how processes are at the same time intractably complex (clue's in the name) and yet
at some level in some way to some people compositionally and behaviourally explainable and, even, sometimes, gasp,
predictable.

Does true randomness exist? Is it a fundamental law of our universe like the finite maximum speed at which we can travel?

In some sense it doesn't matter. There is no practical difference between a random process and one for which we don't
understand the generating mechanism. And the randomness "washes out" a lot of the time too, due to statistical phenomena
like the law of large numbers. Things can also be "random" at one scale or dimension or level of
accuracy, and yet deterministic in another.

But in a deeper sense, it does. Matter. Randomness is something we can't predict, and have
difficulty explaining. But this is not true of non-random processes: we _can_ understand them if we work
at the problem long enough. And we will, eventually.

From a mathematical perspective, the answer is clearly yes. A random sequence can be generated quite easily from
a deterministic process, and they seem to exist everywhere in physics, nature, society, and even mathematics itself.

We can't prove this apparent randomness, but we can test for it, build arguments for it, and say things
about it in probability.

Was the mathematics of randomness only invented as a way to deal with processes we don't understand?
Or does its invention/discovery reveal the presence of true randomness in our universe?
