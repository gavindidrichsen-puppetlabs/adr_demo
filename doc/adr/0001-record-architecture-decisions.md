# 1. Record architecture decisions

Date: 2024-03-20

## Status

Accepted

## Context

Have you ever worked on a codebase and wondered why you were using a particular library/framework, applying a pattern, or deploying a particular way? If you ask a teammate and they also have no idea because that was defined before them as well.  Software evolves, especially software products that can have a very long lifespan. Decisions are made by developers and/or architects that may no longer be involved in the product/project. Or perhaps they no longer even work at the company anymore

A lot of this is institutional knowledge that is lost, leaving you guessing:

* Is the decision still relevant for the current context?
* What was the context when the decision was made?

Instead, capture Architecture Decision Records along with your code in the same repository. It’s a log of all the decisions made along the course of a project/product.

## Decision

We will use Architecture Decision Records, as [described by Michael Nygard](http://thinkrelevance.com/blog/2011/11/15/documenting-architecture-decisions).

## Consequences

See Michael Nygard's article, linked above. For a lightweight ADR toolset, see Nat Pryce's [adr-tools](https://github.com/npryce/adr-tools).  When a new ADR is created with, e.g., ``adr new 'deciding to do this and such'`, then a template is created with 3 questions to answer:

* **Context**: The issue motivating this decision, and any context that influences or constrains the decision.
* **Decision**: The change that we're proposing or have agreed to implement.
* **Consequences**: What becomes easier or more difficult to do and any risks introduced by the change that will need to be mitigated.
