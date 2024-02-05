# You Need to Know Everything

## Mathematics

Let's leave competence aside. I just want
to focus on what you have to _know_. But this is slightly difficult when it comes to maths.
There's a difference between knowing a proof or mathematical relationship or rule, 
and knowing how and why to apply them (and doing it).

Where does one draw the line between mathematics required specifically to
do data sciencey things and just basic stuff? I don't think I'd get away with complaining that
you have to Know the rules of addition to do machine learning. That doesn't seem right.

A good question to ask: what level of maths does mandatory schooling provide you with?
Theoretically. [In the UK](https://assets.publishing.service.gov.uk/media/5a7cb5b040f0b6629523b52c/GCSE_mathematics_subject_content_and_assessment_objectives.pdf)
this is basic number theory, algebra, what I would characterise as working with numbers,
geometry, probability, and statistics. Note that there is some variance amongst countries,
for example [students in Singapore do some linear algebra and set theory](https://www.moe.gov.sg/-/media/files/secondary/syllabuses/maths/2020-express_na-maths_syllabuses.pdf).

We ask this question to determine what core mathematical ability would someone looking to, say, make a career
switch when, say, AI has consumed some or all of their job, already have? And what do they need to add?

Additional specific mathematics required to do data science includes:

- (More advanced) Probability theory
- Linear algebra
- Calculus
- Optimisation

There are a few other niche pieces (such as information theory) that we use but these are certainly the core
concepts.

## Science

Defined here as theoretical understanding, based on the laws of mathematics and logic, that has
been empirically validated.

The most obvious place to start is statistics which is, sort of, built on the mathematics of
probability theory. You need to know about classical statistical techniques. Even though these
are being super-ceded by contemporary ML, they can be still useful. Correlation, Central Limit
Theorem, Law of Large Numbers, Maximum Likelihood Estimation, A/B testing, Linear Regression,
Statistical Significance, Time Series Modelling, and muuuuuuch more.

Then you have to know the theory behind classical machine learning techniques. How does
ML work at a high level? What are the algorithms? How does gradient descent work? What are
hyperparameters and how do we optimise them? How do we measure how "good" a model is? How do
we ensure correct fitting?

Make sure you know about the cutting-edge stuff, too. Neural networks. XGBoost. Transformers. Etc.
Because some new way of doing things can _easily_ make your current approach suboptimal. 

Footnote: do you really _have_ to know all of this stuff? Not really (to what extent to you
_have_ to know anything?) It would all be professionally useful to know. But I suppose the exact
things you should know depends on your exact role. More on that later. I think at a minimum
everyone should know 1) where the gaps in their knowledge are and 2) to apply caution and
know the dangers of messing around with things in areas of knowledge gaps.

## Engineering

There's no point in knowing the theory behind data science without the ability to
use it. Obviously. And also obviously, this requires knowledge of computers so that we
can leverage their processing power to perform lots and lots of mathematical operations.

We tell computers what to do via code that it can understand. But fortunately we don't have to
code individual transistor operations - lots of smart people have invented ways to
abstract these instructions so that we can input them in a way that is easier for us write.

At a minimum you should know a language for building models.
Python, R, C++, Julia, whatever. Know everything about data structures and 
manipulation to make data transformations easy. And the packages or wrappers for ML-specific
functionality for these languages. Such as scikit-learn in Python, visualisation libraries,
TensorFlow, PyTorch, JAX, etc.

Once you have the ability to create a model, there is additional engineering knowledge
required to create the infrastructure that surrounds it. Where is the data coming from
and how are you getting it? This might be via APIs, which you need to be familiar with.
Or it might be via a relational database. In which case you need SQL.
Additional RDBMS knowledge is needed to write data to the DB (and maybe even create and manage it).

Then we combine the model code and data to train the model. Although this is simple locally
using CPUs, things start to get more complicated when we have a large amount of data
and want to do this in the cloud. Or maybe on a(some) specific GPU(s), in which case you'll
need to know some things about hardware.

Once the model has been created, how are people or services going to access it?
This probably means hosting in a cloud provider like AWS. So knowledge of data storage,
compute clusters, service maintenance, etc. is required. As is implementing checks on model
performance and pipelines for re-training when this performance dips below a certain threshold.

_To be fair, all of this engineering ability probably isn't required for most roles.
There are a few different things you can do within the data science space, all with
different required skill-sets. An ML engineer might not need to know much about the business,
but will need to have strong engineering abilities. Some data scientists
won't need to know much about engineering. AI Researchers will be mostly focused on theory._ 

## Business

But you can't just use your theoretical knowledge and engineering skills to grab some data,
create a model, and deploy it. From a purely modelling perspective, data quality and understanding
is vital. You must understand what the data is, where it's coming from, how it's collected, and other
such intricacies. This requires specific knowledge about the subdomain you're working in/with.

And of course, there's no point in doing any of this modelling if the business doesn't care.

AI must be pitched and sold and delivered continuously and consistently otherwise
your work is going in the bin. Understanding the needs of the business and 
catering to them. This is easier with some understanding of how the business
functions and the industry it operates in.

And to least some extent you'll need to do all the things necessary to make sure that the
team, as a team, is successful. Management, mentorship, hiring, strategy, team PR. All
required to ensure data science succeeds.
