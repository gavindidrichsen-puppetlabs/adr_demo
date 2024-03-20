# adr_demo

## Design Decisions

<!-- adrlog -->

* [ADR-0001](doc/adr/0001-record-architecture-decisions.md) - Record architecture decisions
* [ADR-0002](doc/adr/0002-do-whiteboard-wednesday-talks.md) - Do whiteboard wednesday talks

<!-- adrlogstop -->

## Setup

Before getting started make sure the following utilities are present:

* [adr-tools](https://github.com/npryce/adr-tools)
* [adr-log](https://github.com/adr/adr-log)

## Usage

To use this repo do the following:

```bash
# cd into this directory

# if not done already, then initialize the ADR document directory
adr init

# create an ADR record
adr new "Do whiteboard wednesday talks" 

# answer the questions: context? decision? consequences?
code doc/adr/0002-do-whiteboard-wednesday-talks.md
```

## References

### The command-line tools

* [npryce/adr-tools: Command-line tools for working with Architecture Decision Records](https://github.com/npryce/adr-tools)
* [adr/adr-log: Generate an architectural decision record log (adr-log) out of architectural decision records (ADRs)](https://github.com/adr/adr-log)

### Background information

* [Architecture Decision Records (ADR) as a LOG that answers "WHY?" - CodeOpinion](https://codeopinion.com/architecture-decision-records-adr-as-a-log-that-answers-why/)
* [Documenting Architecture Decisions](https://www.cognitect.com/blog/2011/11/15/documenting-architecture-decisions)
* [Architecture Decision Records (ADR) as a LOG that answers "WHY?" - YouTube](https://www.youtube.com/watch?v=6H6zfCNeqek)
* [Architecture Decision Records | Andy Dote](https://andydote.co.uk/2019/06/29/architecture-decision-records/)
* [Communicating and documenting architectural decisions - David Ayers](https://www.youtube.com/watch?v=rwfXkSjFhzc)

## Contributing

When updating the code base and making design decisions, please record each design desision in similar fashion to the existing set beneath `./doc/adr`.  Please follow the steps below when creating a new design decision:

```bash
# create a new design decision
adr new "Title of your design decision"

# fill in the "Context", "Decision", and "Consequences" of the new doc

# update the `README.md` table of contents to include the newest design decision
adr-log -i README.md -d doc
```
