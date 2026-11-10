# Knowledge Architecture Overview

## Purpose

PP School uses an explicit real-world knowledge structure instead of treating a curriculum outline or an LLM-generated syllabus as the authoritative knowledge model.

## Domain backbone

The backbone represents knowledge through stable domain structures such as:

- phenomena and problems people try to explain or solve;
- concepts, objects, models, laws, and constraints;
- methods, skills, practices, tools, and representations;
- evidence, assumptions, validity boundaries, and common misconceptions;
- applications and connections to other domains and future learning.

This structure is intended to remain meaningful even when a curriculum, school timetable, or assessment system changes.

## Curriculum as a mapping layer

Official education requirements are important, but they answer a different question: where and when an education system expects particular learning to occur. PP School therefore maps curriculum and school information onto the domain backbone using:

- jurisdiction and authority;
- year or phase;
- subject or learning area;
- official code or statement;
- expected depth and route;
- school exposure or course progress.

The mapping does not make curriculum coverage equal to canonical knowledge, learner familiarity, or mastery. Missing school records mean that the layer is unrecorded; they do not prove that a school did not teach something.

## Five positioning layers

The same learner and knowledge object can have multiple valid positions:

1. **World knowledge:** the stable domain, cluster, and atomic path.
2. **Government coordinate:** jurisdiction, curriculum, year, official code, and requirement strength.
3. **School coordinate:** school or course exposure such as not recorded, not started, in progress, or covered.
4. **Learner declaration:** a private learner statement such as know, learning, not yet, or unsure.
5. **Direct evidence:** an observation produced by a defined action, representation, condition, and assessment basis.

The layers are related but not interchangeable. In particular, learner declaration does not create direct evidence, and a single practice result does not automatically create a stable mastery claim.

## Forward and real-world development

The structure can include forward anchors that introduce later study, university-level ideas, professional concepts, or real-world scientific and technical applications. These are presented as bounded exposure or context. They do not silently alter a learner's verified route or claim that the learner has mastered the concept.

## Authority boundary

The explicit knowledge model is not generated or governed solely by an LLM. Models can assist with research, extraction, comparison, or review, but canonical knowledge requires source evidence, traceable mapping, review, and human-controlled publication.

## Evidence anchors

The original repository evidence is represented in the public package through [selected implementation evidence](SELECTED_IMPLEMENTATION_EVIDENCE.md) and [the evidence map](EVIDENCE_MAP.md). The historical records `38dab44` (2026-08-03) and `fdac754` (2026-08-23) are described as historical presence of the direction, not as proof of the complete later system.

## Limitations

This overview describes a distributed set of contracts and projections. It does not claim that all five layers are stored in one unified persisted data model, that every domain claim has complete scientific coverage, or that the current remote deployment contains every documented capability.
