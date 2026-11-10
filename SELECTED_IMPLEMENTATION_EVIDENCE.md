# Selected Implementation Evidence

This file contains deliberately small excerpts and source references. It is not a copy of the product source code. The excerpts were inspected from the original repository; tests and builds were not executed while preparing this public package.

## 1. Learning-position separation

Source reference: `shared/knowledge-coordinates.ts:27-38, 1177-1190, 1233-1237`.

```ts
/**
 * A cluster is a stable navigation branch in the world-knowledge graph. It has
 * no year level: curriculum, school and learner positions are separate layers.
 */
export interface KnowledgeCluster {
  id: string;
  domainFamilyId: string;
  name: string;
  definition: string;
  example: string;
  atomicNodeIds: readonly string[];
}

export type LearnerDeclarationState = "know" | "learning" | "not_yet" | "unsure";

export interface LearningPositionLayers {
  schoolProgress: readonly SchoolKnowledgeProgress[];
  learnerDeclarations: readonly LearnerKnowledgeDeclaration[];
  directEvidence: readonly DirectKnowledgeEvidence[];
}
```

What this supports: curriculum, school, learner, and evidence positions are represented as distinct concepts. It does not prove that all conceptual layers share one persistence table or that every live screen displays them together.

## 2. Review-result contract

Source reference: `server/sub2-world-knowledge-review-agent.ts:23-32, 172-191`.

```ts
properties: {
  verdict: { type: "string", enum: ["support", "challenge", "abstain"] },
  confidence: { type: "number", minimum: 0, maximum: 1 },
  citedSourceManifestIds: { type: "array", items: { type: "string" } },
  citedExternalRecordIds: { type: "array", items: { type: "string" } },
  reasoningSummary: { type: "string" },
  risks: { type: "array", items: { type: "string" } },
}
```

The corresponding validation rejects an invalid verdict, non-finite confidence, missing source arrays, empty reasoning, or missing risks/actions before returning the review result. This supports strict review contracts and explicit challenge/abstention states. It does not prove that every knowledge item is independently reviewed.

## 3. Direct-evidence eligibility

Source reference: `server/practice.ts:1666-1681, 1703-1721`. The following is an abridged excerpt; the evidence-record fields have been omitted from the public package.

```ts
const atomicEvidence: LearnerEvidence[] = scored.results.flatMap((result) => {
  const publication = result.assessmentPublication;
  if (!publication) return [];
  const eligible = new Set(publication.eligibleTargetIds);
  return (result.assessmentTargets ?? []).flatMap((target) => {
    if (!target.targetId || target.evidenceUse !== "direct" || !eligible.has(target.targetId)) {
      return [];
    }
    return [{
      eligibilityBasis: "published_item",
      // additional evidence-record fields omitted from this public excerpt
    }];
  });
});
```

What this supports: direct evidence is conditional on a published assessment item, an eligible target, and `direct` evidence use. It does not prove that a live learner completed a task during the inspection.

## 4. Parent publication boundary

Source reference: `src/components/ChildAssignmentPanel.test.tsx:1071-1105`. The following is an abridged excerpt; setup and rendering details are omitted.

```ts
it("keeps generated questions as a draft until the parent publishes them", async () => {
  const draftSummary = assignmentSummary({ status: "draft", expiresAt: null });
  const published = assignmentSummary({ status: "assigned" });
  vi.mocked(createChildAssignment).mockResolvedValue(draftSummary);
  vi.mocked(publishChildAssignment).mockResolvedValue(published);

  // generate and preview the draft
  expect(screen.getByText(/草稿 · 未发布/)).toBeTruthy();
  expect(publishChildAssignment).not.toHaveBeenCalled();
});
```

What this supports: the repository test definition protects the parent-controlled draft/publication boundary. It does not establish that this test was executed or that the current remote release implements the same behavior.

## 5. Deterministic source-freeze assertions

Source reference: `scripts/w4-03-source-freeze.test.ts:30-40, 100-130`. The assertions below are selected from the source test.

```ts
expect(freeze.sourceSnapshots.every((item) =>
  item.retrievalVerification.downloadCount === 2 &&
  item.retrievalVerification.secondDownloadMatched &&
  item.retrievalVerification.matchingSha256 === item.contentHash.value
)).toBe(true);

expect(freeze.candidateProductionStarted).toBe(false);
expect(freeze.externalModelCallCount).toBe(0);
expect(freeze.registryMutationCount).toBe(0);
expect(freeze.publicationActionCount).toBe(0);
```

What this supports: the test definition includes byte/hash reproducibility and explicit no-publication safety assertions. It does not prove that the test passed during this public-package preparation.

## Source references

The selected excerpts are drawn from the original private repository and are intentionally limited to the evidence needed for portfolio inspection:

- `shared/knowledge-coordinates.ts`
- `server/sub2-world-knowledge-review-agent.ts`
- `server/practice.ts`
- `src/components/ChildAssignmentPanel.test.tsx`
- `scripts/w4-03-source-freeze.test.ts`
- `package.json` for the demonstrated TypeScript/React/Vite/Express/Zod/Vitest stack

The complete source repository, private deployment files, production data, and operational credentials are intentionally excluded from this public package.
