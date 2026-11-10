# Knowledge Governance Overview

## Purpose

Knowledge governance defines how a research or content candidate can be evaluated, challenged, verified, and eventually published without allowing model output alone to become authority.

## Source evidence

The governance approach starts with source records and immutable snapshots. A source snapshot carries provenance and identity information such as source type, authority, version, retrieval details, validity, and a content hash. A later source change becomes a new candidate or revision instead of silently rewriting the old evidence.

## Mapping and release stages

The intended evidence path is:

```text
source snapshot
  -> reviewed mapping
  -> local summary and boundaries
  -> content or assessment candidate
  -> review and validation gate
  -> human-controlled publication
```

Direct anchors, contextual reach, and unreached areas are kept distinct. A semantic relationship can suggest useful context; it cannot be upgraded into official coverage merely because the nodes are connected.

## Independent review roles

Review results have explicit outcomes:

- `support`: the reviewer finds the candidate adequately supported within the allowed evidence;
- `challenge`: the reviewer identifies a problem, missing support, risk, or required correction;
- `abstain`: the allowed evidence is insufficient for a responsible conclusion.

These outcomes are not a vote-counting mechanism. The design preserves the reason for challenge or abstention, the cited source records, risks, and required actions. A disagreement is information to resolve, not noise to hide.

## Deterministic verification

Source-freeze and release checks use stable revisions, manifests, byte-level comparisons, and SHA-256 content identity. The purpose is reproducibility: a reviewer should be able to distinguish the exact source and release basis used for a decision.

## Human publication authority

Models may assist with research or review. They do not independently:

- create canonical knowledge without an evidence and review path;
- turn contextual reach into official coverage;
- convert learner exposure into mastery;
- publish a formal knowledge release;
- override a challenge or abstention without an explicit human decision.

## What the evidence supports

The public package includes selected source excerpts and references showing strict review-result validation, source-freeze assertions, direct-evidence eligibility, and workflow boundaries. These support the existence of the design and implementation mechanisms.

They do not establish that every knowledge item passed independent review, that the approach is more accurate than another method, that all documented governance applies universally, or that the current remote deployment is healthy.
