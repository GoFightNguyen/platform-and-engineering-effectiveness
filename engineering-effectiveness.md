# [Why you should invest in good Developer Experience today](https://www.thoughtworks.com/insights/blog/why-you-should-invest-good-developer-experience-today)

> __Developer Experience (DX)__ encompasses all aspects of the developer's interaction with the organization, its tools and systems.

Engineers have a gap in the amount of time they want to spend on value-adding activities and the amount of time they actually do.
A portion of the gap is caused by operations, which has mostly been addressed through DevOps and Continuous Delivery.

Another portion of that gap is caused by poor DXs: poor DX => low engineering effectiveness.


## How bad DX looks
When engineers are bound to bad DXs, the gap is widened.

Here are common patterns of a bad DX:
- non-automatable (GUI) interfaces of provided tools and systems binding the engineers to manual, non-value-added activities
- hardware and infrastructure is often scarce and hard to get
- tedious onboarding and setup
- fragmented team structures: hand-offs
- a lack of enablement: APIs, libraries or platforms without guidance, examples, and shared knowledge


## How you can achieve a good DX
- adopt product thinking for technical products and platforms
- see engineers as customers
  - identify constraints and problems in the engineering journey as an opportunity to improve the DX; look for areas where the leverage of solving the problem is high
- identify and shorten feedback loops
- enable and encourage collaboration
- create a culture where team members feel safe to experiment and encouraged to innovate


# [Maximizing Developer Effectiveness](https://martinfowler.com/articles/developer-effectiveness.html)
- be cautious of introducing too many new processes, too many new tools and new technologies; this may lead to increased complexity and added friction in the everyday tasks

## Day in the life in a highly effective environment
The engineer is able to make incremental progress in a day.
Broken down, it looks like:
- clear about what to work on for the day
- CI/CD pipelines are green
- able to make incremental code changes that are quickly validated locally and using unit tests
- qualities of a dependency (such as a BC or InnerSource library)
  - documentation and API spec discoverable through a dev portal
  - dependency team has an engineer doing support, making it easy to get help
- focus for hours with an interruption
- ability to break the way one desires (ping-pong, drink, walk, etc)
- commits pass through a number of automated checks before being deployed to production
  - metrics

## Day in the life in a low effective environment
The engineer does not achieve much, leaves frustrated and unmotivated.
Broken down, it looks like:
- immediately dealing with alerts
- checks numerous systems to find error reports since there are no aggregated logs
- waiting upon other groups for a response about a feature previously completed
- many meetings, many of which are status meetings
- long CI/CD process
- qualities of a dependency (such as a BC or InnerSource library)
  - unable to find documentation
  - too long of a delay in getting help

## Developer Effectiveness
Engineering effectiveness is about delivering the maximum value to your customers.
It requires having an effective environment, or DX.
- as little friction as possible by allowing engineers to avoid unnecessary complexities, frivolous churn and long delays

## How to get started
The author recommends focusing on optimizing a number of key developer feedback loops, make them fast and simple.
Measure the length of the feedback loop, the constraints, and the resulting outcome.
When new tools and techniques are introduced, these metrics can show the degree to which developer effectiveness is improved or at least isn't worse.

| Feedback Loop | Low Effectiveness | High Effectiveness |
| --- | --- | --- |
| Validate a local change works | 2 mins | 5-15 seconds |
| Find root cause for defect | 4-7 days | 1 day |
| Validate component integrates with other components | 3 days - 2 weeks | 2 hours |
| Validate a change meets non-functional requirements | 3 months | 1 day - 1 week (depending on scope of change) |
| Become productive on new team | 2 months | 4 weeks |
| Get answers to an internal technical query | 1-2 weeks | 30 mins |
| Launch a new service in production | 2-4 months | 3 days |
| Validate a change was useful to the customer | 6 months or never | 1-4 weeks (depending on scope of change) |

These metrics are possible.
Not every feedback loop needs to be in the high effectiveness bucket, but they are goals to guide your strategy.

Observations about feedback loops:
- feedback loops are ran more often if they are shorter
- action will be taken based on the result of the feedback loops if they are seen as valuable and not purely bureaucratic overhead
- earlier, more frequent validation reduces rework later on
- feedback loops with simple-to-interpret results will reduce back-and-forth communications and cognitive overhead

## Introducing micro feedback loops
We have to nail the basics, the things done 10, 100 or 200 times a day.
These are micro feedback loops.

Address feedback loops that are long enough for an engineer to get distracted and lose their state of flow.
We want engineers to take breaks and clear their head intentionally, not because the environment makes them.

Inefficiencies in micro feedback loops compound to affect larger feedback loops and indicators.

Platform thinking considers how to optimize for the org, rather than an individual team.

## Organizational Effectiveness
> It starts with a recognition by leadership that technology - and removing friction from development teams - is vital to the business.

Ways to manifest this:
- technical leaders continually measure and re-examine effectiveness
- technical leaders create an open forum for engineers to present the problems they face (and ideas for solutions)
- embrace the DX as a product
- provide engineers with
  - ability to improve their day-to-day lives
    - policies for teams to make incremental tech improvements and manage tech debt
  - ability for engineers to innovate (they know their goals and bottlenecks)
  - ways for ideas to bubble to the top
- platform thinking: creating an internal platform focused on improving effectiveness
  - the team has technical product managers and success metrics related to the impact on consuming teams
  - governance: setting and communicating the guardrails, and then nudging teams in the right direction