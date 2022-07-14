# Architectural Decision Records (ADRs)

ADRs are a record of the arguments and decisions made to change process or software architecture.
The idea is for these records to be regularly reviewed, updated, and documented so that new people or external parties
 to a project can read along and understand the points of a decision, the context, 
 and in general can make educated decisions based on previous discussions.

ADRs provide a safer place for individuals who would rather not speak up in face to face communication 
 (which can feel confrontational) or would like to educate themselves on a topic before commenting.

## Documenting Architecture Decisions

In [Documenting Architecture Decisions](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions)
Michael Nygard explains the concept as small, easy to read and update documents which give context to a decision.

He further explains the alternative (when the context for decisions is lost) as "Blindly accept the decision." or "Blindly change it.".
We agree with this point and have thus generated our own process for implementing this concept.

### Architectural

Micheal defines "Architectural" as decisions which "affect the structure, non-functional characteristics, dependencies, interfaces, or construction techniques" for a project.
Our definition is a a bit less structured, essentially if it comes up in a design discussion we want to keep track of it.

### Versioning

Michael states that the file names give no context (are simply numbered) and 
are never altered once resolved, because "It's still relevant to know that it was the decision, but is no longer the decision.".
We are choosing to place our ADRs in a version control system where the history of the decision can be queried in the versions of the document itself. 
This is handy because it lowers the total number of docs that will accumulate and allows us to give the files contextual names.
Our file names can summarize the decision they contain so that readers can easily find and reference that decision.

### Status Types

Michael gives four potential statuses for an ADR: "proposed", "accepted", "deprecated", and "superseded".
Since we are versioning our ADRs and using PRs, we only need "accepted" or "rejected", affording us a simpler model.
Changes which are in review are handled in PRs, the review is finalized after a period of time with the status of "accepted" or "rejected".

## Tools

A command line tool for ADRs [is available](https://github.com/npryce/adr-tools) to help manage the complexity of altering or finding a decision.
Our model makes such tools a bit less useful, preferring the use of the tools built into the source code management system.

## Process

The process of preparing, documenting, and presenting a decision should be easy and straightforward,
we don't want this process to encumber our ability to change, but enable educated decisions.

### Issue

The goal of an issue _isn't_ whether or not to accept or reject a decision.
The goal of an issue is to decide whether or not a decision needs to be made.

Generate an Issue if:
   - you have a question or need context about a decision
   - you have a suggestion which might need a decision to be made
   - you believe additional context might change a decision

### Pull Request

Generate a PR if:
   - you have additional context for a decision
   - a decision was made and there is no ADR for it
   - you brought up a decision in a design discussion and a change was suggested

Pull requests are more closely tied to the file version than Issues,
 so we prefer conversations about the decision to be in the Pull Request,
 where it can more easily be found.
