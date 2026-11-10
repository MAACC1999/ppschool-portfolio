# PP School Case Study

## Overview

PP School is a parent-facing learning companion for planning practice, reviewing learning signals, and keeping different kinds of educational evidence separate. The product is designed around a trust problem: a dashboard should not turn a curriculum label, a school record, a learner statement, or one practice result into an unsupported mastery verdict.

## The problem

Families need useful next steps, but educational systems often mix together at least four different questions:

- What does the domain of knowledge contain?
- What does an official curriculum require at a given year or jurisdiction?
- What has a school or course exposed the learner to?
- What has the learner actually demonstrated in a defined task?

PP School treats those as separate facts. It can therefore show context and uncertainty without pretending that incomplete signals are equivalent to stable mastery.

## Three connected design contributions

### 1. Product vision and learning model

The product gives parents a way to review learning position, recent observations, and next steps. Its learning model distinguishes:

1. world knowledge;
2. government or curriculum coordinates;
3. school exposure;
4. learner declaration;
5. direct evidence from a concrete action, representation, and condition.

This is a non-collapse rule. A learner may be positioned against a curriculum coordinate, have no school-exposure record, say they are still learning, and have no direct evidence. Those states can coexist without one automatically rewriting another.

### 2. Independent real-world knowledge architecture

The knowledge base is not treated as a generated syllabus. The domain backbone is organised around phenomena, concepts, objects, models, methods, evidence, constraints, applications, and links to continuing scientific and technical development.

Official education requirements then map onto that backbone through jurisdiction, year, subject, official codes, expected depth, and school coverage. Curriculum is a coverage and timing coordinate, not the complete ontology of knowledge. Forward anchors can expose later or real-world concepts without turning exposure into mastery.

The repository history gives this direction a dated presence: `38dab44` records the K0 knowledge-kernel boundary on 2026-08-03, and `fdac754` records private-trial preparation on 2026-08-23. These commits do not prove that every later governance mechanism already existed at those dates, and they are not evidence of priority over any external GPT proposal.

### 3. Knowledge governance

The governance model controls how knowledge can gain formal status:

- source snapshots preserve provenance and byte-level identity;
- reviewed mappings distinguish direct anchors from contextual reach;
- independent review roles can return `support`, `challenge`, or `abstain`;
- challenge and abstention preserve disagreement or insufficient evidence;
- deterministic verification checks source and release identity;
- human approval remains necessary for formal publication.

Models may assist research or review. They do not independently confer canonical authority, upgrade contextual material into official coverage, or publish knowledge without human control.

## Product experience

The packaged parent overview capture shows learner selection, a mathematics summary, recent observations, and a family note that separates observed facts from cautious interpretation. The weekly-plan capture shows learner selection, weekly organisation, plan limits, and parent-controlled preparation before sharing. A separate historical child demonstration capture shows the shape of a learner-facing activity card; it is documented as an in-memory demonstration, not a current remote-release session or a real learner outcome.

The two parent screenshots are live observations of authenticated UI states from 2026-11-07. The child route in that remote session was inspected only as an access boundary. No child credentials were entered, no invitation was opened, no assignment was published, and no practice result was submitted during the inspection. The knowledge-model and governance-flow visuals are explanatory summaries derived from the linked repository contracts; they are not claims that every step was observed in one live session.

## Implementation shape

The source project is a TypeScript, React, Vite, and Express application with Zod validation and Vitest/Testing Library coverage. The public package includes only selected implementation evidence, not the complete source tree.

The implementation boundaries represented by the selected excerpts are:

- distinct learning-position data structures;
- strict review-result validation;
- direct evidence gated by published assessment eligibility;
- parent draft and publication workflow;
- child self-practice separated from parent-assigned practice;
- deterministic source-freeze and no-publication safety assertions.

## Evidence and limitations

The evidence hierarchy is explicit:

- **Owner-reported design origin:** product direction, learning model, independent knowledge architecture, and governance concept.
- **Repository-corroborated implementation:** selected source excerpts, contracts, workflow tests, and release-control assertions.
- **Live observed behavior:** the two redacted parent-interface screenshots.
- **Historical evidence:** the two dated Git commits described above.
- **Unverified:** complete live child workflow, current remote release identity, current test/build status, educational outcomes, adoption, and historical authorship of every design decision.

The package intentionally makes no claim that all five conceptual layers are stored in one unified persisted data model. It also makes no claim of measured learning improvement, statistical superiority of the review approach, or current production health.
