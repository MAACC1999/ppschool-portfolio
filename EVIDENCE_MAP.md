# Public Evidence Map

This map distinguishes owner-reported design origin, repository-corroborated implementation, live observation, historical evidence, and claims that remain unverified.

| Claim | Evidence class | Public evidence | Boundary |
| --- | --- | --- | --- |
| Parent-facing learning companion | Owner-reported direction + live observation | [Case study](CASE_STUDY.md); [`VISUALS/parent-overview-presentable.png`](VISUALS/parent-overview-presentable.png); [`VISUALS/learning-plan-presentable.png`](VISUALS/learning-plan-presentable.png) | Presentation captures show two parent UI states; synthetic labels replace redacted fields and do not establish the complete workflow |
| Learner-facing activity surface was explored historically | Historical repository artifact + owner-reported context | [`VISUALS/child-demo-activity.png`](VISUALS/child-demo-activity.png); [visual index](VISUALS/README.md) | Historical in-memory demonstration; not a current remote-release capture or a real learner result |
| Five-layer learning model | Owner-reported design origin + repository corroboration | [Knowledge architecture overview](KNOWLEDGE_ARCHITECTURE_OVERVIEW.md); [selected evidence, layer excerpt](SELECTED_IMPLEMENTATION_EVIDENCE.md#1-learning-position-separation) | Does not prove one unified persisted model |
| Five conceptual layers are intentionally kept distinct | Owner-reported design origin + explanatory diagram | [`VISUALS/knowledge-model.svg`](VISUALS/knowledge-model.svg); [knowledge architecture overview](KNOWLEDGE_ARCHITECTURE_OVERVIEW.md) | Diagram summarizes the contract; it does not prove a single database structure or live rendering |
| Official requirements mapped onto an independent domain backbone | Owner-reported design origin + historical/repository corroboration | [Knowledge architecture overview](KNOWLEDGE_ARCHITECTURE_OVERVIEW.md); [selected evidence, source references](SELECTED_IMPLEMENTATION_EVIDENCE.md#source-references) | Does not prove complete scientific coverage or priority over another external system |
| Learner declaration is not direct evidence | Repository corroboration | [selected evidence, layer excerpt](SELECTED_IMPLEMENTATION_EVIDENCE.md#1-learning-position-separation) | Tests were inspected, not executed for this package |
| Parent draft remains private until publication | Repository corroboration | [selected evidence, parent workflow excerpt](SELECTED_IMPLEMENTATION_EVIDENCE.md#4-parent-publication-boundary) | Does not prove the current remote release passes the test |
| Direct evidence is publication-gated | Repository corroboration | [selected evidence, direct-evidence excerpt](SELECTED_IMPLEMENTATION_EVIDENCE.md#3-direct-evidence-eligibility) | Does not prove a live practice submission occurred |
| Independent review preserves support, challenge, and abstain | Owner-reported governance design + repository corroboration | [Knowledge governance overview](KNOWLEDGE_GOVERNANCE_OVERVIEW.md); [selected evidence, review schema](SELECTED_IMPLEMENTATION_EVIDENCE.md#2-review-result-contract) | Does not prove universal coverage or measured superiority |
| Knowledge release preserves review disagreement and human authority | Owner-reported governance design + explanatory diagram + repository corroboration | [`VISUALS/governance-flow.svg`](VISUALS/governance-flow.svg); [knowledge governance overview](KNOWLEDGE_GOVERNANCE_OVERVIEW.md) | Diagram explains intended control flow; it does not prove every item followed it in production |
| Source verification and release controls are deterministic | Repository corroboration | [Knowledge governance overview](KNOWLEDGE_GOVERNANCE_OVERVIEW.md); [selected evidence, source-freeze assertions](SELECTED_IMPLEMENTATION_EVIDENCE.md#5-deterministic-source-freeze) | Assertions were inspected, not executed during this preparation |
| K0 knowledge-kernel direction existed by 2026-08-03 | Historical evidence | Git commit `38dab44`, dated 2026-08-03, recorded in the original repository history | Does not prove every later governance mechanism existed then |
| Private-trial preparation existed by 2026-08-23 | Historical evidence | Git commit `fdac754`, dated 2026-08-23, recorded in the original repository history | Does not prove current deployment health |

## Unverified claims

This public package does not claim:

- a complete live parent -> publication -> child -> direct-evidence journey;
- current remote release identity or production health;
- executed test or build success during this preparation;
- educational improvement, adoption, or accuracy improvement;
- universal application of the review governance;
- original authorship of every implementation detail or historical design decision.
