## Why ML in Finance Is Hard

It should be easy. Data is abundant, well-catalogued, clean(ish), and unambiguous.
Most people are data-literate and smart.
Companies are well-resourced. They are data-centric. They understand the 
importance of things like data pipelines and latency and other important
data stuff.

### Environment

Let's imagine it is for a second. Easy. Clean data is delivered to us on a plate,
with surrounding infrastructure already constructed, and patient stakeholders
who understand ML. All we have to do is train a model.

So we do. Let's say this model predicts what our clients should be investing in.
Doesn't sound too hard. And let's say our model is actually quite good.
We deploy it. Everything seems good.

But problems start to occur when we start to actually _use_ the model.

Deciding what to invest in, like many in finance, is a **high-stakes** example. Unlike Meta predicting
what ads I'll click or Spotify predicting what song I'll like, the consequences of
failure are severe. Not just the loss of a client, a loss of lots of AUM, 
or a severe hit to reputation. But a _real_ impact on someone's life.

**The more severe the consequences of failure, the less able we are to deploy ML
models.**

Humans still need to make the final decision and be able to explain it. I still
want my pilot to be able to fly the plane, even if autopilot is doing all the work.

Regulatory bodies also want an explanation. And as UK has some of the most mature financial
regulations in the world, there is a lot of explaining to do.
This is a consequence of the high-stakes environment we're operating in. "Because 
the accuracy on the test set was above 90%!" isn't going to satisfy the PRA. Fuck ups
could [cost the government billions of £££](https://researchbriefings.files.parliament.uk/documents/SN05748/SN05748.pdf).
Deploying cutting-edge models that 
aren't yet fully understood and/or difficult to interpret isn't going to sit well
with the regulators.

And they are right to be demanding, as we are dealing with an incredibly complicated
and complex environment. The use of **two** adjectives, which are apparently synonyms, resulting in 
redundancy in the previous sentence,
is deliberate.

Complicated and complex mean different things here.

Complicated systems are ones that we understand, that have known outputs given an input
and a set of initial conditions. A good example is a car. We know exactly how a car works.
We can build them from scratch. If I push my foot down on the accelerator, the car will
accelerate forward. Input --> output. Even though there are many components that interact
in _complicated_ ways, a car can be deconstructed to its constituent parts.

But some things can't. Think of the climate. There's a reason we can't forecast the weather
much more than 10 days in advance. Because small changes in initial conditions had huge consequences
on the system dynamics ([Edward Lorenz](https://en.wikipedia.org/wiki/Edward_Norton_Lorenz) noted 
this a while ago). Properties of the system are emergent: they can't be predicted by
studying individual components. Because components interact in intractable ways. It's very hard
to understand the system and what the generating function is (even _if_ it's simple, 
it might be [computationally irreducible](https://mathworld.wolfram.com/ComputationalIrreducibility.html)).

Now think of the type of systems we deal with in finance. Can we predict the price of
BP at close tomorrow? Do companies know what the interest rate on their mortgage products
will be a year from now? How about their derivative positions?

The reason we can't is because we are operating in
a [complex](https://arxiv.org/abs/1912.05088) environment.

This makes ML challenging because most algorithms work best in iid, thin-tailed, tractable, linear,
ergodic, statistically-stationary environments. Environments that are complicated but still machine-understandable if only we had the
compute and data storage capacities to do so. The reason we can't use ML (yet, and probably not ever)
to predict what the BoE will set as the interest rate a year from now is that this output is
an output of a complex system.

### Data

Another regulatory headache is the data itself.

Data often contains sensitive information that should only be accessed and used in a secure way.
No local training. No training on PII. No using GPT.

One thing that contributes to this is legacy systems. If the data was all in S3 with good access
management via IAM roles and other mechanisms, this would be less of an issue. But it's not.
Often to access this data means extraction from some type of cumbersome legacy system (that's
costing a fortune) where data can only be extracted in some obscure format after logging on
to a remote desktop (and only 17 rows at a time). Sure, this isn't as much of a problem in
FinTech. But the problem persists more than you would imagine - there simply aren't many good
modern tech solutions for much of the financial system.

The data team might be in high-demand at the organisation because of this. The data from
a plethora of systems has to be E, T, and L'ed. This takes a lot of work, especially if you
have to reconcile data from many different systems.

And this is a problem, because you can't do ML without data. _Clean_, preferably voluminous,
data is a pre-requisite. Hence a substantial amount of data infrastructure work is required before you can get to ML.

### Humans

It can be quite hard to
communicate what AI is and the benefits of implementing it. 
Everyone has pre-conceived notions.

_I'm going to have to do some departmental stereotyping here so please 1) forgive me 2)
know that this is tongue-in-cheek 3) don't [take it personally](https://www.youtube.com/watch?v=2t4RVg_Yq2g&ab_channel=BloopersTV) 4)
this is not representative
of everyone who holds these positions and 5) the views expressed below do not necessarily reflect
the views of my employer or my future or past employers or my Mum and Dad._

SWEs see it as just another API call. They (rightly) think in
engineering ways. They are accustomed to _data + rules = output_,
not _data + output = rules_.
They sometimes lack the in-depth or statistical
understanding of these systems and so can sometimes want to use them in slightly naive ways.

The data team can be just as bad. To some analysts, ML is just a notebook used to try out a few
models using Sklearn until one has precision of over 85%.
This is fine for ad-hoc analysis.
But what data people sometimes fail to realise is the sheer amount of ex-model components, development steps,
and monitoring and testing requirements that are needed to actually _deploy_ a model. Let alone
what it takes to build an ML _system_.

ML/AI teams are often trapped between these two slightly-wrong conceptions.

This confusion adds to the fact that financial institutions, more it seems than other companies in other industries, are 
constantly pulled in different directions by departments. Risk want to take no risks. Compliance want everything
documented and done slowly are carefully. Engineering want to build software. Data want to analyse
everything before and after decisions are made. Finance want to maximise expected revenue next quarter.

What's difficult is that they are all doing their jobs and are all kind of right.
