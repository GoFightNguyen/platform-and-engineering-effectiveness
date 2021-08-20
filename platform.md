# [Mind the Platform Execution Gap (Platform Prerequisites)](https://martinfowler.com/articles/platform-prerequisites.html)

Ways to enable engineers to spend time on value-adding activities:
1. use SaaS to outsource functionality that is not part of the org's core business ✅
2. consolidate infrastructure capabilities required by many teams and services into a digital platform.
simplify the experiences of our colleagues by taking advantage of infrastructure assumptions/constraints/guardrails

Number 2 is in progress.
Examples:
- ps-service chart
- default logging/monitoring capabilities in k8s created by cloud-engineering
- shared grafana instances
- standard ways of interacting with RabbitMQ
- gitlab helpers


What is a platform?
> A digital platform is a portfolio of technical products (self-service APIs, tools, services, knowledge and support) which are arranged as a compelling internal product.


Why?
- manage the cognitive load of engineering teams and decrease time to new features


Viewpoint
- take, and promote, a "what it-is-for" view over "how-it-is-made"
  - Action item for us: quit talking about backstage and start talking about what the dev-portal is for in terms of experience, documentation, and support


Creating a sustainable, successful platform requires the following foundational competencies. These do not have to be mature as long as we resolve to develop them along the way. Please refer to the foundational competencies listed below for more info:
- business value
- product thinking
- operational excellence
- software engineering excellence
- healthy team(s)


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


# [How to Build an Internal Developer Platform from Those Who Have Done It](https://www.infoworld.com/article/3611369/how-to-build-an-internal-developer-platform-from-those-who-have-done-it.html)

> Goal: To abstract away cumbersome infrastructure decisions for software developers, easing the operations burden on overstretched devops teams.

# [Service Catalogs Explained](https://humanitec.com/blog/spotify-backstage-service-catalog)
With a growing number of tools requested by different development teams and an ever-expanding base of services...setups are characterized by an increasing lack of transparency and visibility.

## What is a Service Catalog
Here, a service catalog is a means of centralizing all services and applications that are important within an organization.

Every service catalog has these 4 core elements:
- ownership info and other metadata
  - ownership, tech stack, repo, current version, last update, documentation, etc
  - enables anyone to discover whether a required service is already available and to then coordinate directly with the respective responsible team
- service templating
  - enables engineers to get started right away
- service usage
  - which service is consumed by which applications
  - enables the owning team to learn about usage
- service versioning
  - which versions of a particular service are used by which applications and in which environments
  - enables notifying dependent teams of issues and only the affected environments or apps can be handled

# [Backstage Software Catalog](https://backstage.io/docs/features/software-catalog/software-catalog-overview)
A centralized system tracking ownership and metadata for all software in the ecosystem (services, websites, libraries, data pipelines, etc).

Why:
- help teams manage and maintain the software they own by providing a uniform view of all their software (anything the team catalogs)
- makes all the software, and who owns it, discoverable

Any kind of software should be registered, even if not owned/maintained by your company; it is useful to still create components for tracking ownership.

> Teams are responsible for maintaining the metadata about their components

# [Strategies for Adopting](https://backstage.io/docs/overview/adopting)

The value of a dev-portal is realized when it becomes _THE_ dev-portal.

The central team owning the dev-portal has 4 primary objectives:
- maintain and operate the product
- drive adoption of customers (engineers)
- ensure organizational best practices for software development are encoded into a set of Software Templates
- evangelize it as a central platform (a platform of platforms) towards other infrastructure/platform teams

## Internal Evangelization

The dev-portal is a "platform of platforms," a marketplace between infra/platform teams and end-users.

Customers include end-users of the platform as well as _contributing teams_ of the platform.

_Contributing teams_ should be able to autonomously deliver value directly to their customers.
This is primarily done by building plugins.
Therefore, contributing teams should treat their plugins as, or part of, the products they maintain.

Some tactics for evangelizing to contributing teams:
- lunch & learns (seminars) showing how to build a plugin
- embedding knowledgeable plugin developers on the team just getting started
- hackathons
- show-and-tell for anyone to present their plugins
- provide metrics to contributing teams
- proactively identify new plugins and reach out to teams

## KPIs and metrics

Look at the doc for ideas of whether a dev-portal have had a successful impact on software engineers.

Some proxy metrics to validate the success of _the_ dev-portal:
- number of teams that have contributed at least one plugin
- number of total plugins
- % of contributions coming from outside the central dev-portal team
- traditional metrics such as visits and page views