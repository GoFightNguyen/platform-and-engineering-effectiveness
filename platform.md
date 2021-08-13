# [Mind the Platform Execution gap (Platform Prerequisites)](https://martinfowler.com/articles/platform-prerequisites.html)

- a platform can manage the cognitive load of engineering teams and decrease time to new features
- There are baseline capabilities that orgs must cultivate in order to successively execute on a platform strategy
- the platform team needs to think of the platform as a software product, needing dialog with users, attention to reliable operations, and a healthy team environment


Ways to enable engineers to spend time on value-adding activities:
- use SaaS to outsource functionality that is not part of the org's core business
- consolidate infrastructure capabilities required by many teams and services into a digital platform
  - a platform is usually a curated combination of internally developed and externally procured capabilities

> A digital platform is a foundation of self-service APIs, tools, services, knowledge and support which are arranged as a compelling internal product

- An internal platform team usually takes tools and services [offered by cloud providers and other vendors] and hosts, adapts or extends them to make them conveniently available to their software developer colleages
  - The aim is to bridge the gap between what you can buy and what is really needed, such as a simplified k8s experiences taking advantage of infrastructure assumptions/constraints/guardrails

Platform includes any internally provided tooling that promotes developer effectiveness
- take (and promote) a what-it-is-for view over a how-it-is-made view when it comes to experience, documentation, and support

There is a gap between the platform-hype and execution, this must be navigated
- more than provisioning infrastructure for services
- there are foundational competencies that are prerequisites for sustainable success
  - not all of them have to be mature before embarking on the platform journey
  - must have appetite and resolve to develop them along the way

## Foundational Competencies
### Business Value
- will efficiency, quality and time-to-market benefits exceed the financial, talent and opportunity costs incurred in the construction and evolution of the platform?
- if you cannot articulate the business case for the platform, do NOT adopt a platform
- to deliver the promised value to the organization:
  - the platform team must plan for a greater proportion of continuous improvement vs product innovation
  - operability-related items must be a priority so that the platform is kept manageable and costs under control
  - know that deprecation is a fundamental part of the platform product lifecycle; expect to deprecate features for new products, internally built successors, or even devolving responsibility back to individual teams
  - users expect consistency, stability and dependability over a stream of new features

### Product Thinking
- the platform is a product, treat is as such
  - market it
  - customer empathy
  - product ownership
  - intelligent measurement
  - communicate roadmap
  - accept feedback
  - harvest experiences
- product development teams are the customers
  - anything preventing them from smoothly using the platform threatens the successful realization of the business value of the platform
- prioritize developer experience (DX)
- harness enthusiasts as early adopts and champions of the platform
- maintain goodwill; be transparent and apologize for outages
- __resist the temptation to rely on managerial mandates as an adoption strategy__
  - we want a productive relationship, not "this is supposedly for your own good"

### Operational Excellence
- adopting an internal platform is __asking engineers for trust__
  - the platform is now a key dependency of the systems the org uses to fulfill its function
  - worse than breaking trust, is not know that you broke it
- do we have the operational competence to justify that trust?
  - infrastructure
  - networking
  - scaling
  - DR
  - understanding of the underlying tech
  - SRE practices like observability and monitoring
  - alerting
  - on-call
- migrations must be graceful to minimize downtime

### Software Engineering Excellence
- must be able to sustain the pace of evolution your development teams' changing needs will demand
 - things written for the platform (custom applications, scripts, templates and config files) will rapidly accumulate complexity
 - to retain the ability to quickly and safely change the platform, it requires software engineering excellence

### Healthy Teams
- sustaining excellence over the long term requires strong team-level disciplines
- when your platform is depended upon by the rest of the business, it is NOT acceptable for th expertise to maintain them to be held by only a few busy individuals
- for a platform team to productive:
  - mature systems for planning
    - work is described in terms of value
    - processes for prioritization
    - avoid the urgent overwhelming the important
  - does not manage too many platform products at once
  - most of the time spent investing in the improvement of the platform, not toil such as incidents and unplanned work
  - reduce context switching

## Getting Started
__Start within your capabilities__
- even without all these capabilities (foundational competencies) in your org, you can still be successful
> the secret is not to compromise on the quality of your execution, but to be modest in the scope of your ambition - at first.
- no matter how small, a platform initiative should produce business value, be guided by product thinking, be implemented with operational and software engineering excellence and be backed by a team structure that can sustain the new platform service

- __First question__: what is the smallest thing we can build that would help the product teams?
  - gauge your capabilities, and determine what you can achieve based on the maturity of your capabilities

- __Second question__: how could we upgrade or migrate away from this when the time comes?
  - factor in realistic lifetimes (3-5 years) of technologies and architectural seams for replacing solutions

__Let adoption of the platform be voluntary__
- product teams should have the ability to opt out of platform services
  - encourages the platform team to keep their services loosely coupled
  - when your platform org is dependent on product teams' appreciation of the platform's benefits, it pressures the platform org to keep customer delight at the forefront

__Utilize a simple classification system__
- doing so can set expectations about the maturity of new platform features
- provides the platform team freedom to experiment and to validate their assumptions about the product before making a strong (and long-term) commitment to it

> If you are able to keep the above in mind...your platform teams will manage small portfolios of very effective products.
Their cognitive load will be small and their focus will be able to stay on continuously reducing the development teams' time to market instead of just on keeping the lights on.

## Conclusion
Digital platforms are portfolios of technical products.