# Insights Don't Matter

Value comes from action.

The only way to create value, is by doing something. By acting. 
Information can help you perform better actions, but information alone is useless.

Data functions are currently focused on how to extract, collate, and analyse
information, whereas we should be thinking about how data can lead
to valuable actions.

Build and maintain infrastructure, then do the things that result in
the most valuable actions for the business.

### The wrong way to think

People used to think that just collecting terabytes of data would magically
transform to increased profitability for their business.

We now know this is wrong - that data has to be organised and 
accessible. If we were just able to give ExCo all their required dashboards,
they could run the company perfectly form their evil lair. 
Data was to be a "product" that internal consumers would,
well, consume. The whole org would be "data-driven".

The problem is that this only works if people are using the data usefully and
intelligently. Dashboards upon dashboards might make people feel better,
but if they are used in the wrong way, they are useless.

Some people realised this and decided we shouldn't be data-driven, we should
be _insights_-driven. Rationale: data in the hands of the data-illiterate is
at-best pointless. People who know how to use the data usefully and intelligently should
be given control and allowed to investigate anything they think could be insightful.

But insights alone are useless, too. Sure, they may lead to some abstract
increase in knowledge about the business, but without actions resulting
from them, they aren't valuable.

Data isn't a product. If I'm selling a product, I don't care what people are using my 
product for, and how often they are using it, I just care if they buy it (or not).
The market will tell me how valuable it is.

But this isn't true for data - there is no market for determining value. What people say they want,
and how they are using data, are very different from the most valuable use of the data. 

### Maximise expected value

Here's an equation:

value = number of actions * value per action 

Which explains the following value hierarchy:

Models > Insights > Dashboards

Models (in production and as part of consequential pipelines) can perform actions
constantly. Insights usually don't result in any action at all, but they do at least
have the potential to result in high-value change. Dashboards don't even get looked at and 
when they do it's usually as a sanity check. They rarely result in action.

This is also a helpful way to think about which models to create: those that are part of
frequent and/or valuable processes.
