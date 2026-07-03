# Disposition of Comments for the WebAssembly Working Group Charter

This document is the disposition of comments received during the charter-refinement review of the [WebAssembly Working Group draft charter](https://w3c.github.io/charter-drafts/2026/wasm-wg-charter.html). This is a recharter of the existing WebAssembly Working Group.

Comments were received through:

- [w3c/strategy#533](https://github.com/w3c/strategy/issues/533): Strategy funnel issue (charter review and horizontal-review requests)
- [w3c/a11y-request#160](https://github.com/w3c/a11y-request/issues/160): APA (Accessibility) horizontal review
- [w3c/i18n-request#309](https://github.com/w3c/i18n-request/issues/309): Internationalization horizontal review
- [w3cping/privacy-request#206](https://github.com/w3cping/privacy-request/issues/206): Privacy (PING) horizontal review
- [w3c/security-request#131](https://github.com/w3c/security-request/issues/131): Security horizontal review
- [w3ctag/design-reviews#1220](https://github.com/w3ctag/design-reviews/issues/1220): TAG review
- [w3c/charter-drafts#794](https://github.com/w3c/charter-drafts/pull/794) and [w3c/charter-drafts#814](https://github.com/w3c/charter-drafts/pull/814): Charter revision PRs addressing feedback

## Executive Summary

Of the substantive comments:

- **6 were accepted and resulted in charter changes**: missing deliverable metadata added; Success Criteria “will” language reverted to “should”; the CEPC reference updated to the Code of Conduct; the Patent Policy updated to the current (15 May 2025) version; Ethical Web Principles and Privacy Principles added to the guiding-documents list; and the “WebAseembly” typo fixed.
- **1 was addressed by a specification change**: the Privacy reviewer’s question about “fine-grained sandboxing” was resolved by expanding the Component Model goals document.
- **Several were noted or clarified** without a charter change: the WG’s intent to keep updating the CR Snapshots, the move away from spec levels/shortnames, and the deliberate “to Candidate Recommendation” wording were each explained in the thread.

One reviewer questioned the group’s intent to keep its deliverables in Candidate Recommendation indefinitely (the “living standard” approach) rather than advancing to Recommendation. The team contact resolved the comment by explaining the rationale, and clarified the IPR position. See comment 18.

## Horizontal Reviews

### 1. Accessibility (APA): Noted

> no comment or request from APA.

— ruoxiran, [strategy#533 comment](https://github.com/w3c/strategy/issues/533#issuecomment-4388755130) ([a11y-request#160](https://github.com/w3c/a11y-request/issues/160))

No action needed.

### 2. Internationalization (i18n): Noted

> No comment or request from i18n

— himorin, [strategy#533 comment](https://github.com/w3c/strategy/issues/533#issuecomment-4397946485) ([i18n-request#309](https://github.com/w3c/i18n-request/issues/309))

No action needed. Separately, himorin raised a set of cross-cutting review points on the strategy issue; those are dispositioned as comments 6 to 11.

### 3. TAG: Satisfied

> The TAG discussed this today in our breakout and we are satisfied with the charter (other than the dates).

— bkardell (TAG), [design-reviews#1220 comment](https://github.com/w3ctag/design-reviews/issues/1220#issuecomment-4608097145)

**Response:** No charter change requested beyond the Start/End dates, which are intentionally placeholders pending charter approval (see comment 17).

### 4. Privacy (PING): Satisfied

> My only comment was that “finely sandboxed” seemed a worthy goal but not
> one that I could find more detail on, even after looking at the proposal
> repository (sandboxed, without the modifier, is mentioned in the use
> cases). If the group means something specific by this in the deliverable,
> it should be a bit easier to determine what.

— hardie (PING), [privacy-request#206 comment](https://github.com/w3cping/privacy-request/issues/206#issuecomment-4711522558)

**Response:** The group explained that the Component Model enables finer-grained isolation between modules of user code, and lukewagner filed [component-model PR #663](https://github.com/WebAssembly/component-model/pull/663) to expand on what “fine-grained sandboxing” means in the Goals document.  The reviewer [confirmed this resolved the concern](https://github.com/w3cping/privacy-request/issues/206#issuecomment-4716137517).  No charter change required.

### 5. Security

[Chose not to respond]

## Charter Review Comments

The following were raised on the strategy issue. Comments 6 to 11 are the points in himorin’s consolidated review memo; dschuff and sideshowbarker responded.

### 6. Template-diff link points to the running charter: Noted

> (memo for HR reviewers) diff from charter template link is diff from charter template to current running charter

— himorin, [strategy#533 comment](https://github.com/w3c/strategy/issues/533#issuecomment-4262879696)

**Response:** Noted for reviewers. dschuff [provided a corrected diff](https://github.com/w3c/strategy/issues/533#issuecomment-4306629750) (template vs. proposed charter), and a diff against the current charter was [provided later](https://github.com/w3c/strategy/issues/533#issuecomment-4437195924).

### 7. Missing metadata for normative deliverables: Accepted

> lacking metadata for normative deliverables?

— himorin, [strategy#533 comment](https://github.com/w3c/strategy/issues/533#issuecomment-4262879696)

**Response:** The charter was [updated with the necessary deliverable metadata](https://github.com/w3c/strategy/issues/533#issuecomment-4438291176) in [commit 9ed82d6](https://github.com/w3c/charter-drafts/commit/9ed82d642d4eecb53b5828ced98991704fb4dda0).

### 8. Intent to keep updating the CR Snapshots: Clarified

> all three CR specs only have one (initial) CRS publication, followed by updates using CRD. does WG intend to update CRS before or during next rechartered period, per no intention to REC as in Success Criteria?

— himorin, [strategy#533 comment](https://github.com/w3c/strategy/issues/533#issuecomment-4262879696)

**Response:** dschuff [confirmed](https://github.com/w3c/strategy/issues/533#issuecomment-4306629750) that the WG does intend to update the Candidate Recommendation Snapshots.  No charter change needed.

### 9. Success Criteria “will” vs “should”: Accepted

> testing, security and privacy, and a11y ‘should’ conditions in success criteria are weakened as ‘will’, does this strong intention of the WG?

— himorin, [strategy#533 comment](https://github.com/w3c/strategy/issues/533#issuecomment-4262879696)

**Response:** The “will” phrasing had been introduced as an attempt to express stronger intent than the template’s “should.” To avoid any reading that it weakened the criteria, [all `will` instances in the Success Criteria section were reverted to `should`](https://github.com/w3c/strategy/issues/533#issuecomment-4437275404) in [commit 81f840b](https://github.com/w3c/charter-drafts/commit/81f840ba1764b18264d300c84ec3f4e561944a10).

### 10. CEPC reference → Code of Conduct: Accepted

> should update CEPC link and text to CoC in section 6.

— himorin, [strategy#533 comment](https://github.com/w3c/strategy/issues/533#issuecomment-4262879696)

**Response:** Updated from the Code of Ethics and Professional Conduct to the [Code of Conduct](https://www.w3.org/policies/code-of-conduct/) in [PR #794](https://github.com/w3c/charter-drafts/pull/794).

### 11. Patent Policy version: Accepted

> keeping Patent Policy 2020 is intention of the WG?

— himorin, [strategy#533 comment](https://github.com/w3c/strategy/issues/533#issuecomment-4262879696)

**Response:** An oversight; the group follows the latest. Updated to the Patent Policy version of 15 May 2025 in [PR #794](https://github.com/w3c/charter-drafts/pull/794).

### 12. Handling of the three Rec-track deliverables (levels / shortnames): Noted

> I think it would be useful if the charter clarified how the group intends to deal with its 3 existing Rec-track deliverables: they were published as Rec in 2019; the current latest TR are CRD, that use level 2 shortnames … but their abstract describe them as release “3.0” … the current hybrid set up is confusing, and rechartering is hopefully a good time to clarify and describe the intent.

— dontcallmedom, [strategy#533 comment](https://github.com/w3c/strategy/issues/533#issuecomment-4438094330)

**Response:** dschuff [explained](https://github.com/w3c/strategy/issues/533#issuecomment-4443347650) that the intent is to move away from levels and not keep the W3C level or shortname aligned with the spec’s internal version number. Explanation provided in-thread; no charter change made.

### 13. “to” vs “beyond” Candidate Recommendation: Noted (intentional)

> the success criteria are usually required to move “beyond Candidate Recommendation”, but this charter requires them to move “**to** Candidate Recommendation”. This is significantly different, and unusual. I suspect this is an unintended effect of just replacing “Proposed” with “Candidate”.

— pchampin, [strategy#533 comment](https://github.com/w3c/strategy/issues/533#issuecomment-4460165037)

**Response:** dschuff [confirmed this is intentional](https://github.com/w3c/strategy/issues/533#issuecomment-4511520149): the group does not intend to advance past CR, but still expects to meet these criteria when graduating proposals from the Community Group. No change made. See also comment 18.

### 14. Ethical Web Principles and Privacy Principles missing: Accepted

> the charter template suggests that WGs be guided by “Ethical Web Principles, Privacy Principles, TAG Web Platform Design Principles”. This charter proposal only mentions the latter. Any reason to ignore the first two?

— pchampin, [strategy#533 comment](https://github.com/w3c/strategy/issues/533#issuecomment-4460165037)

**Response:** No reason; an unnecessary divergence. Ethical Web Principles and Privacy Principles were added to the guiding-documents list in [PR #814](https://github.com/w3c/charter-drafts/pull/814), which also removed several other unnecessary deviations from the template.

### 15. “WebAseembly” typo: Accepted

> Typo: “WebAseembly Core” → WebAssembly Core

— caribouW3, [strategy#533 comment](https://github.com/w3c/strategy/issues/533#issuecomment-4508141755)

**Response:** Fixed in [PR #814](https://github.com/w3c/charter-drafts/pull/814).

### 16. Diff against the current charter: Noted

> Does anyone have a link for a diff against the current charter? All the links so far are against the template.

— annevk, [strategy#533 comment](https://github.com/w3c/strategy/issues/533#issuecomment-4415445025)

**Response:** Diffs against the current charter were provided: a [compare view](https://github.com/w3c/charter-drafts/compare/407e1ef..d7f1797) and an [htmldiff](https://github.com/w3c/strategy/issues/533#issuecomment-4495561506).  Logistics only; no charter change.

### 17. Charter Start/End dates and Charter History: Pending

> One nit I noticed is that Charter History needs to account for the current > charter extension and the end date should probably reflect the new > [dd monthname yyyy] start date.

— annevk, [strategy#533 comment](https://github.com/w3c/strategy/issues/533#issuecomment-4495561506); also flagged by bkardell (TAG): “The start and end dates are clearly wrong.”

**Response:** The Start and End dates are intentionally placeholders (`[dd monthname yyyy]`) that are filled in when the charter is approved and the Call for Participation is issued; the Charter History table row for this rechartering will be completed at the same time. To be resolved at AC approval.

## Candidate Recommendation vs. Recommendation

### 18. Keeping deliverables in CR rather than advancing to Recommendation: Noted; rationale provided

> Why not [move past CR]? Given that this is (in my opinion!) a W3C anti-pattern, I think it would be helpful to explain this position in the Charter, why you don’t think W3C-level consensus is important, and how you intend to support or encourage adoption in a wide variety of devices … there are a range of external-to-W3C specifications that may want to reference WebAssembly, but that may have challenges doing so absent a Recommendation.

— nigelmegitt, [strategy#533 comment](https://github.com/w3c/strategy/issues/533#issuecomment-4517032531)

The reviewer further argued that staying in CR raises IPR and stability risks for outside adopters (for example in the AV-media / HbbTV space), and that the “living standard” goal can be met without remaining in CR permanently. ([follow-up](https://github.com/w3c/strategy/issues/533#issuecomment-4518098951))

**Response:** The team contact [responded](https://github.com/w3c/strategy/issues/533#issuecomment-4517223447) that the Process permits a group to remain in CR, does not require justifying that choice, and does not treat it as an anti-pattern. On the specific IPR concern, annevk [noted](https://github.com/w3c/strategy/issues/533#issuecomment-4518327052) — and the team contact [confirmed](https://github.com/w3c/strategy/issues/533#issuecomment-4518440637) — that the group uses Candidate Recommendation Snapshots, which qualify as Patent Review Drafts and carry the same Royalty-Free IPR obligations as a Recommendation, addressing the royalty-free-licensing concern.

## Charter Revisions

The charter changes were made in the [charter-drafts](https://github.com/w3c/charter-drafts/) repository:

- [PR #757](https://github.com/w3c/charter-drafts/pull/757): initial update to follow the current charter template.  - [PR #794](https://github.com/w3c/charter-drafts/pull/794): review follow-ups: Code of Conduct reference, current Patent Policy version, and corrected Process-document section references (comments 10, 11).
- [PR #814](https://github.com/w3c/charter-drafts/pull/814): removed unnecessary deviations from the template: added Ethical Web Principles and Privacy Principles, minor boilerplate alignment, and the typo fix (comments 14, 15).
- Direct commits added deliverable metadata ([9ed82d6](https://github.com/w3c/charter-drafts/commit/9ed82d642d4eecb53b5828ced98991704fb4dda0)) and reverted Success Criteria `will` → `should` ([81f840b](https://github.com/w3c/charter-drafts/commit/81f840ba1764b18264d300c84ec3f4e561944a10)) (comments 7, 9).
