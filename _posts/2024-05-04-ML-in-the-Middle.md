# ML in the Middle

Basically it's about how and why it's tricky to introduce ML particularly to a medium-sized org,
with accompanying caveats and why that actually might be wrong at the end.

_Note one: when I'm talking about "ML",
I'm referring to the construction of an ML system that's integrated into the existing
business and technical infrastructure. Not some models in a NB. Not using ChatGPT to
write SQL query, or Perplexity to do some research._

_Note two: emphasis on introducing. If DS/ML/AI is a core component of your business proposition,
it doesn't matter what size you are. It's definitely going to be there, duh._

## Size Matters

Small companies, I'm talking really here about start-ups, these days have to answer this question overtly
and immediately: is ML going to be a core component of what we do, or not?

Predicting the outcome of cricket matches? ML is intrinsic.
Creating an app for companies to check employee mental health? ML not needed.

Large companies are in a surprisingly similar position: an ML system already exists
(and is probably a core part of what they do), or it doesn't. In the case of
the latter, they can easily ignore it (for now) and continue with the business
activities that are clearly working (we know they're working to some extent, otherwise they wouldn't be large).
Alternatively they can throw lots and lots of money and time at the problem.

Medium-sized companies are in a trickier situation (I'm talking mostly about
contemporary, tech-enabled, scale-ups). They usually have something that's kind of
working, that has been scaled to a certain extent. But this success can be a curse:
the preceding period of growth/funding/building stuff that worked means that
now systems and processes throughout the business may not be a good fit for the new scale.

## Specific Problems

I will now go through some general challenges associated with building an ML system,
and then tell you how these problems are more acute at medium-sized orgs.

### Costs

Building an ML system requires resources. Medium-sized companies
are often unable to commit these resources to something new that may or may not
be financially beneficial.

Compare this to large companies, who make a lot of money. They can afford to throw
these large piles of money at problems. This includes the problem of building an ML system.

Small companies aren't expected to be profitable.

### Time horizon

The reason MSCs are often looking for some
round of funding or exit in the near future. Hence a reluctance to invest in
long-term projects.

Both small and large companies have an advantage here. The big corps have a theoretically infinite time
horizon to play with. They 
can afford to invest in something now that will have benefits in the long term. Short-term
thinking is incentivised, sure, but at least they can justify long-term investment.

Start-ups have a definitively long-term view. It takes 10 years to build a really successful company, so although
they are strapped for cash, they sort of have to make long-term investments.

### Data

MSCs have _some_ data, but it's unclear if they have enough for the investment required
to properly utilise this data to be justified.

Large companies obviously have reams and reams of data so this isn't a problem.
And small companies have a plan to leverage the small amount (and usually niche) of data they have, use publicly-available
data, or not use ML at all.

### Platform

I can be hard to justify committing resources to work on platform issues given the potential tech debt 
work required to re-build/improve current infrastructure. People can be reluctant to introduce new components
to these systems.

Small companies, by contrast, are building from scratch so can design their systems with ML in mind.

At large companies, although their own systems are often antiquated, specific teams
of people are tasked with dealing with specific issues, so there's no risk of the data science team doing
(all the) infrastructural work.

### Expertise

They (large corps) can afford to hire these specific teams and *experts* to design and implement a system.
Because although the mission might not be as attractive, the technology not as cutting-edge, and the
use cases not as exciting, large corporations have multiple advantages, many of which I have mentioned.

Start-ups have the advantage of working on exciting problems, with equity in a potentially-very-valuable
business, and a chance to shape ML at the company in all the ways you want to.

Scale-ups can have trouble attracting top talent. They probably have some
already at the company, but it can be fairly raw/junior, and hence will take time to properly deploy.
Their big selling point is joining a fast-growing company.

## Other Thoughts

### Let's all work together

You can kind of see how all these things work in conjunction with each other (against MSCs).

Large corporations have something that's working, and, they assume, will continue to work in the future,
which gives them money and a long-term view.
They are able to hire a specific team to implement a system that has obvious (because of their
huge amounts of data) medium-to-long-term benefits.

Small corporations can attract top talent to build a system from scratch to solve a novel problem.
The system doesn't have to be immediately scalable or profitable, but has the potential to be
so in the future, allowing the founding participants to be the lead of a substantial ML team
at a successful company.

Medium-sized corporations are faced with a dilemma. They have a product/service that's kind of working,
although maybe not profitably. 
Fixing outstanding issues with the organisation, platform, and product, as well as focusing on
reducing costs and proving (at least potential) profitability can take priority over introducing new
components, that have questionable value-add because of a lack of 1) big data and 2) expertise to leverage 
this data effectively, that will have to be integrated with, and will add extra load to, the already-stressed infrastructure.
They have a medium-term view: they are driven by doing what's necessary to
earn their next funding round, or exit.

### It's not all bad

MSCs do have some advantages over other companies.

Start-ups have no data or existing infrastructure. They are also poor, so can't afford to make
non-critical investments in just about anything. Data science employees may end up doing a lot of things
that aren't data science.

Large companies (some) have old infrastructure that
few people in the global job market understand. They also have
big risk teams, and compliance, and many board members.

It's also not a binary problem. It's not like companies have a choice between building a full ML system, or
not. In reality, one (one as in literally one person. Me, for example) can get a basic system operational fairly 
quickly. Which can be iterated upon. And there's always the option to of course not create a system and
use ML for isolated projects.

So maybe it's not so bad for scale-ups after all?
