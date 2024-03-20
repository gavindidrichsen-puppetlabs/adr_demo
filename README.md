# adr_demo

The following is [Andy Dote's](https://andydote.co.uk/2019/06/29/architecture-decision-records/) summary of Architectural Design Decisions:

> Architecture Design Records are there to solve the main question people repeatedly ask when they view a new codebase or look at an older part of their current codebase:
>
> > Why on earth was it done like this?!
>
> Generally speaking, architectural decisions have been made in good faith at the time, but as time marches on, things change, and the reasoning gets lost. The reasoning might be discoverable through the commit history, or some comments in a type somewhere, and every once in a while, people remember the Wiki exists, and hope that someone else remembered and put some docs there. They didn’t by the way.
>
> Architecture Design Records are aiming to solve all of this, with three straightforward attributes: Easy to Write, Easy to Read, and Easy to Find. Let’s look at these on their own, and then have a look at an example.

To find out more about ADR, see the [References section below](#references).

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

### Initialize your repository to use ADR:

```bash
# cd into your repo root

# if not done already, then initialize the ADR document directory
adr init

# create an ADR record
adr new "Do whiteboard wednesday talks" 

# open the document and answer the questions: context? decision? consequences?
code doc/adr/0002-do-whiteboard-wednesday-talks.md
```

### Add decision 'table of contents'

To inject a decision table of contents, you need to add the following `adrlog` tags to a document of your choice.  For example, to add a table of contents to my top-level `README.md`, add something like the following:

```markdown
<!-- adrlog -->
<!-- adrlogstop -->
```

Then run the following command which will inject each ADR title as a hyperlink.

```bash
adr-log -i README.md -d doc
```

The [Design Decisions section above](#design-decisions) was generated using the `adr-log`.

## Contributing

When updating the code base and making design decisions, please record each design desision in similar fashion to the existing set beneath `./doc/adr`.  Please follow the steps below when creating a new design decision:

```bash
# create a new design decision
adr new "Title of your design decision"

# fill in the "Context", "Decision", and "Consequences" of the new doc

# update the `README.md` table of contents to include the newest design decision
adr-log -i README.md -d doc
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
* [Thoughworks Technology Radar: Lightweight Architecture Decision Records](https://www.thoughtworks.com/radar/techniques/lightweight-architecture-decision-records)
