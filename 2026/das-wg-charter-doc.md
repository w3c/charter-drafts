# Disposition of Comments for the Devices and Sensors Working Group Charter

This document is the disposition of comments received during the review
of the [Devices and Sensor Working Group draft charter](https://w3c.github.io/charter-drafts/2026/das-wg-charter.html).

Comments were received through:

- [w3c/strategy #530](https://github.com/w3c/strategy/issues/530) — Strategy funnel issue (horizontal reviews)
- [w3ctag/design-reviews #1187](https://github.com/w3ctag/design-reviews/issues/1187) — TAG review
- [Issues](https://github.com/w3c/charter-drafts/issues?q=is%3Aissue+[wg%2Fdas]) and [PRs](https://github.com/w3c/charter-drafts/pulls?q=is%3Apr+%5Bwg%2Fdas%5D) to [w3c/charter-drafts](https://github.com/w3c/charter-drafts/) repository

## Executive summary



## Horizontal reviews

### Acceccibility - Noted

> no comment or request from APA.

by Ruoxi Ran, [w3c/strategy #530 comment](https://github.com/w3c/strategy/issues/530#issuecomment-3848060439)

### Security - Noted

> hi, we have one comment from security, as the charter is focused on privacy and security, have you already a list of the main threats, and have you evaluated to put them in the charter itself?

by Simone Onofri, [w3c/strategy #530 comment](https://github.com/w3c/strategy/issues/530#issuecomment-3848628218)

### Privacy - Noted

> No concerns when discussed among chairs

by pes10k, [w3cping/privacy-request #192 comment](https://github.com/w3cping/privacy-request/issues/192#issuecomment-3986193782)

### Internationalization - Accepted

> [from i18n WG](https://lists.w3.org/Archives/Team/w3t-archive/2026Feb/0016.html)
> 
> [Contact Picker API](https://www.w3.org/TR/contact-picker/) potentially has scary I18N monsters in it (e.g. https://github.com/w3c/contact-picker/issues/63 as i18n-needs-resolution) because it will necessarily deal with personal names and might include sorting (including using pronunciation data e.g. yomi) and searching, transliteration, and the like. If physical address fields are included, that draws in that further level of complexity. 
> For the charter, if i18n WG can ask for early engagement/review and cite the additional need for coordination for the spec somewhere in section 5 that would probably be wise.
> Since the Contact Picker API specification is a joint deliverable between the DAS WG and the [WebApps WG](https://www.w3.org/groups/wg/webapps), so this comment should be applicable also to the WebApps WG charter.

by Atsushi Shimono, [w3c/strategy #530 comment](https://github.com/w3c/strategy/issues/530#issuecomment-4153917428)

**Response** Internationalization WG has been added to the Coordination section by [w3c/charter-drafts PR #804](https://github.com/w3c/charter-drafts/pull/804)

## TAG review 

### 5 points of concerns

TAG raised 5 points of concerns ([w3ctag/design-reviews #1187 comment](https://github.com/w3ctag/design-reviews/issues/1187#issuecomment-3889788860)), 
and provided PRs for 4 points.

#### Specifications with one implementation - XXX (not Accepted, not Won't fix, ???)

> We're concerned to see the Chromium-only Accelerometer, Gyroscope, and Orientation Sensor specifications in the charter, now that the [Device Orientation and Motion](https://www.w3.org/TR/orientation-event/) spec is in Baseline. It makes sense to maintain non-consensus specifications while websites switch over to equivalent consensus APIs, but the charter should commit to only adding new features to the consensus versions. If there's not enough consensus on the new features to incorporate them into the core [Device Orientation and Motion](https://www.w3.org/TR/orientation-event/) spec, this WG could develop an extension specification that allows websites to mostly use the Baseline feature, with a few engine-specific extensions.

The TAG opened a PR [w3c/charter-drafts PR #806](https://github.com/w3c/charter-drafts/pull/806), 
the WG discussed on additional change over the PR but did not reach WG consensus. 

**Response** The Team decided to override this concern by [w3c/charter-drafts PR #818](https://github.com/w3c/charter-drafts/pull/818), 
with adding `including for security and privacy enhancements` over a PR by the TAG 
to enable modification of adding new feature specifically related to security and privacy enhancements. 

#### Involvement of multiple implementers - XXX (not Accepted, not Won't fix, ???)

> We want to ensure that the other specifications fill clear user needs and are making appropriate tradeoffs between those user needs and any potential abuse of the APIs. In many WGs, we can rely on all 3 browser engines to check this, but since this WG does not currently include participation from all major browser engines, we're more concerned here. Could you add this goal to the charter for each of the specifications in that class? We see, for example, https://github.com/w3c/vibration/issues/45 to do this for Vibration, but it would be good to use the charter to ensure it gets done.

The TAG opened a PR [w3c/charter-drafts PR #808](https://github.com/w3c/charter-drafts/pull/808), 
the WG discussed on additional change over the PR, but did not resolved. 

**Response** The Team decided to override this concern by [w3c/charter-drafts PR #821](https://github.com/w3c/charter-drafts/pull/821), 
with including a change suggested by Anssi to remove specifically mention to WebApps and 
adding links to the Process for making maturity level used in text clear.

#### Vibration API council concern - XXX

> The [Vibration Council recommended](https://www.w3.org/2025/08/vibration2-council-report.html#recommendations) that "the WG document the plan [to ship in multiple major browser engines] it thinks is best, whether or not that plan includes implementation in multiple browser engines, and a compelling rationale to help any reviewers decide whether the plan is acceptable." We couldn't find such a plan in this rechartering effort, and we encourage the WG to write such plans for each single-engine specification, in order to head off this possible formal objection.

The TAG opened a PR [w3c/charter-drafts PR #809](https://github.com/w3c/charter-drafts/pull/809) 
to add text not limited to the Vibration specification, but even further in relateion to TAG point 1, 
the WG did not reached a concensus to accept or reject the PR.

**Response** The Team decided to override this concern by [w3c/charter-drafts PR #819](https://github.com/w3c/charter-drafts/pull/819), 
with adding bringing specifications into CG as incubation along with publication as Discontinued Draft, 
for making path clearer to continue incubation but not as completed end state.

#### Support level in status section of specification - Accepted

> We would like the WG to find a way to signal the expected support level for each specification. There's some discomfort on the TAG with using the same spec status?Candidate Recommendation?for all of:
> * deprecated specs that are being maintained while websites migrate to a consensus replacement;
> * features that are stable in one engine but opposed by the others;
> * "living" consensus specs that never intend to advance to Recommendation; and
> * consensus specs that are intended to advance to Recommendation.
> 
> At the same time, we recognize that this is the only status the Process defines for patent protection of these kinds of specifications. At a minimum, each document's support level should be in its SotD section, but ideally the WG would find a way to ensure that _developers reading a specification can tell at a glance which kind of document they're reading_.

**Response** Accepted through 10 PRs.

The TAG opened 10 PRs to specifications, and all merged by the WG, 
Christian Liebel confirmed [this point 4 has been resolved with set of PRs](https://github.com/w3c/strategy/issues/530#issuecomment-4549836034).

* https://github.com/w3c/sensors/pull/494
* https://github.com/w3c/magnetometer/pull/78
* https://github.com/w3c/device-posture/pull/173
* https://github.com/w3c/proximity/pull/63
* https://github.com/w3c/compute-pressure/pull/319
* https://github.com/w3c/accelerometer/pull/85
* https://github.com/w3c/vibration/pull/65
* https://github.com/w3c/gyroscope/pull/66
* https://github.com/w3c/orientation-sensor/pull/87
* https://github.com/w3c/ambient-light/pull/93


#### Web Serial in tentative deliverables - Deferred

> We're concerned by the appearance of Web Serial in the [Tentative Deliverables](https://w3c.github.io/charter-drafts/2026/das-wg-charter.html#tentative). At least Mozilla seems inclined to start implementing that API, and we want it to live in a WG that all implementers are comfortable joining, to ensure that all of their potential concerns about engine/platform capabilities, privacy, and security can be easily raised. That said, its presence in this charter doesn't prevent it from being adopted by another WG instead.

**Response** Conversation held in [email thread](https://lists.w3.org/Archives/Public/www-archive/2026May/0000.html), 
no conclusion has made. 

### Other feedbacks on TAG review

#### Flagging design review concerens - Noted

In parallel to 5 points of concerns, the TAG made a comment in the same post as:

> The following concerns don't affect the charter, but we want to flag a few issues that are likely 
to come up in future design reviews for the individual specifications:
> 
> * We will always look more critically at specifications developed by WGs without members from all major browser engines, since we want there to be [One Web](https://www.w3.org/TR/ethical-web-principles/#multi) in the long run, and the fact that some browsers decide not to implement, inherently means there are concerns with the design. The WG should be prepared to explain how the non-members' critical feedback has been sought and considered.
> * The Generic Sensor architecture seems overcomplicated overall. In reviews of features that use it, we'd appreciate some justification for why that architecture is better than defining APIs in a single layer, as [Device Orientation and Motion](https://www.w3.org/TR/orientation-event/) does.
> * Are the signals in the Battery API still the right ones to help websites help users achieve their goals? Would a "please reduce power use" signal be sufficient, with the UA in charge of deciding how the precise battery level and charging state contribute to that signal?

**Response** The DAS WG noted these comments and continue onversation during further design review over each specification.

#### Support level in status of specifications - Rejected

> Status update: to implement the TAG's request that "each document's support level should be in its SotD section," I opened 11 PRs adding `.advisement` boxes to the SotD of each DAS WG spec. They have since been closed without discussion:
> 
> - [w3c/sensors#492](https://github.com/w3c/sensors/pull/492) — Generic Sensor API
> - [w3c/accelerometer#84](https://github.com/w3c/accelerometer/pull/84)
> - [w3c/gyroscope#65](https://github.com/w3c/gyroscope/pull/65)
> - [w3c/magnetometer#77](https://github.com/w3c/magnetometer/pull/77)
> - [w3c/ambient-light#92](https://github.com/w3c/ambient-light/pull/92)
> - [w3c/orientation-sensor#86](https://github.com/w3c/orientation-sensor/pull/86)
> - [w3c/proximity#62](https://github.com/w3c/proximity/pull/62)
> - [w3c/compute-pressure#318](https://github.com/w3c/compute-pressure/pull/318)
> - [w3c/battery#70](https://github.com/w3c/battery/pull/70)
> - [w3c/device-posture#172](https://github.com/w3c/device-posture/pull/172)
> - [w3c/vibration#57](https://github.com/w3c/vibration/pull/57)
> 
> For charter-level text, [charter-drafts#770](https://github.com/w3c/charter-drafts/pull/770) is in progress. [charter-drafts#784](https://github.com/w3c/charter-drafts/pull/784) proposes specific text addressing the TAG's concerns on SotD signalling, Vibration, and Generic Sensor framing, intended to land alongside #770. The remaining concerns are tracked in [#780](https://github.com/w3c/charter-drafts/issues/780), [#781](https://github.com/w3c/charter-drafts/issues/781), [#782](https://github.com/w3c/charter-drafts/issues/782), and [#783](https://github.com/w3c/charter-drafts/issues/783).
> 
> The TAG's concern that each document's support level should be in its SotD section remains open at the spec level, pending WG discussion.

by Marcos Cáceres, in two comments ([first](https://github.com/w3ctag/design-reviews/issues/1187#issuecomment-4159936835), 
and [second](https://github.com/w3ctag/design-reviews/issues/1187#issuecomment-4163174410)) at w3ctag/design-reviews #1187.
Also the same text has been posted by the same person to w3c/strategy #530 at 
[first](https://github.com/w3c/strategy/issues/530#issuecomment-4159912174) and [second](https://github.com/w3c/strategy/issues/530#issuecomment-4163144358).

**Response** the DAS WG closed opened PRs without merging for ongoing discussion during continuing charter refinement phase

## Other Strategy Issue Feedback

### Vibration API single implementation issue - Deferred, Action taken within another Accepted comment

> From the Vibration Council's [recommendations](https://www.w3.org/2025/08/vibration2-council-report.html#recommendations): 
> 
> > We recommend that the WG document what [implementation experience](https://www.w3.org/policies/process/#implementation-experience) the [Vibration] API currently has ([issue 33](https://github.com/w3c/vibration/issues/33)). In the next rechartering process for the DAS WG, **we anticipate that some W3C members will object to keeping a deliverable without a concrete plan and timeline for shipping in multiple major browser engines.** ... we recommend that the WG document the plan it thinks is best, whether or not that plan includes implementation in multiple browser engines, and a compelling rationale to help any reviewers decide whether the plan is acceptable.
> 
> I don't believe this has been done yet. If the working group wants to avoid Formal Objections to the Charter, addressing the above would be a good start. Similarly, DAS should expect Formal Objections if the TAG's feedback also goes unaddressed. 
> 
> If you'd like to discuss how to address the above and avoid Formal Objections, happy to chat. 

by Marcos Cáceres, [comment at w3c/strategy #530](https://github.com/w3c/strategy/issues/530#issuecomment-3917515554)

**Response** Action has not taken directly to this comment, but implementation report has been published in other PR and also deffered to TAG concern point 3

### Vibration API implementation report - Accepted

> @plehegar @tidoust @himorin — a further development to flag.
> 
> [w3c/vibration#55](https://github.com/w3c/vibration/pull/55) is the implementation report the W3C Council recommended in its [August 2025 report](https://www.w3.org/2025/08/vibration2-council-report.html#recommendations):
> 
> "We recommend that the WG document what implementation experience the API currently has (issue 33)."
> 
> That PR was closed today by @anssiko without merging and without WG discussion, citing (1) EFL WebKit as additional implementation experience, and (2) the PR being "misplaced". Both are rebutted in [a comment on the closed PR](https://github.com/w3c/vibration/pull/55#issuecomment-4205989183): the ewebkit/webkit fork is a discontinued snapshot last updated July 2017 covering end-of-life hardware; w3c/test-results/vibration contains raw Chrome/Firefox data from 2014, not an implementation report.
> 
> As PR author I have pull-only access to w3c/vibration and cannot reopen the PR myself. The closure leaves [vibration#33](https://github.com/w3c/vibration/issues/33) open and the Council's condition unmet — which is tracked as a gate condition for this charter in [charter-drafts#781](https://github.com/w3c/charter-drafts/issues/781).
> 
> This follows the earlier pattern of [11 SotD PRs being closed without discussion](https://github.com/w3c/strategy/issues/530#issuecomment-4159912174). Can W3C staff weigh in on whether closing a PR that directly fulfils a Council recommendation, without WG discussion, is consistent with the process?

by Marcos Cáceres, [comment to w3c/strategy #530](https://github.com/w3c/strategy/issues/530#issuecomment-4206018777)

and

> Following up on the vibration#55 closure flagged in my [previous comment](https://github.com/w3c/strategy/issues/530#issuecomment-4206018777).
> 
> @anssiko's most recent response directs me to regenerate the report using the [w3c/test-results toolchain](https://github.com/w3c/test-results) and submit it there instead. I've responded in [the PR](https://github.com/w3c/vibration/pull/55#issuecomment-4210563389) explaining why that wouldn't meet the Council's requirement: the generated format produces pass/fail percentages, but [W3C Process §6.3.2](https://www.w3.org/policies/process/#implementation-experience) requires a document that addresses whether implementations are independent, publicly deployed, created by non-authors, and whether difficulties have been reported. A score on a given date answers none of those questions.
> 
> I've also filed [w3c/test-results#232](https://github.com/w3c/test-results/issues/232) proposing that the toolchain either be updated to include §6.3.2 narrative sections, or that its README be clarified to distinguish conformance testing from REC advancement implementation reports.
> 
> The substantive question for the Team remains: the PR fulfils a Council recommendation verbatim ("document what implementation experience the API currently has"), and it has been closed without WG discussion. Can the W3C Team advise on the path forward?

by Marcos Cáceres, [comment to w3c/strategy #530](https://github.com/w3c/strategy/issues/530#issuecomment-4210649633)

**Response** Vibration API Implementation Report has been implemented by [w3c/vibration PR #55](https://github.com/w3c/vibration/pull/55) merged.

### Web Bluetooth, Web Serial, WebUSB as tentative deliverables - Won't fix

> Posting as W3C Member (not TAG Member).
> 
> Update: [PR #786](https://github.com/w3c/charter-drafts/pull/786) (adding Web Bluetooth, Web Serial, and WebUSB as tentative deliverables) was merged on May 5. The wide review concerns listed above ([#798](https://github.com/w3c/charter-drafts/issues/798), [#799](https://github.com/w3c/charter-drafts/issues/799), [#771](https://github.com/w3c/charter-drafts/issues/771), [#772](https://github.com/w3c/charter-drafts/issues/772), [#773](https://github.com/w3c/charter-drafts/issues/773)) and the TAG's open review ([design-reviews#1187](https://github.com/w3ctag/design-reviews/issues/1187)) remain unaddressed.
> 
> @plehegar @tidoust @himorin — can the Team clarify how these concerns will be addressed during the refinement phase?

by Marcos Cáceres, [comment to w3c/strategy #530](https://github.com/w3c/strategy/issues/530#issuecomment-4380513758)

**Response** The Team decided to include all five peripheral APIs specifications to tentative deliverables.

### Unresolved comment by the commenter - Rejected

> @plehegar — thank you for the update.
> 
> Can you help me understand how this aligns with three things?
> 
> **1. Your own gate condition (2026-02-24):**
> 
> "I don't think that publishing additional explainers, use cases or demos address the comment. [...] Without such response, I don't think the charter should be sent to the AC for review."
> 
> The point-by-point response you required has not been provided. None of the issues listed above have received a formal response from the WG.
> 
> **2. [W3C Process §4.2](https://www.w3.org/policies/process/#charter-review):**
> 
> "All issues filed against the charter draft must be formally addressed, and their resolutions tracked in a disposition of comments highlighting any issues not resolved by consensus."
> 
> There is currently no disposition of comments, as far as I know. Issues [#798](https://github.com/w3c/charter-drafts/issues/798), [#799](https://github.com/w3c/charter-drafts/issues/799), [#780](https://github.com/w3c/charter-drafts/issues/780), and [#782](https://github.com/w3c/charter-drafts/issues/782) have received zero responses. The TAG's review ([design-reviews#1187](https://github.com/w3ctag/design-reviews/issues/1187)) remains open.
> 
> **3. Process §4.2 also requires:**
> 
> "When the Team initiates an Advisory Committee Review, they must include a disposition of comments received during the charter refinement process, highlighting any issues that were closed despite sustained objections."
> 
> The Team cannot initiate AC review without first producing this disposition. Given that multiple issues have received no WG response, what will that disposition say?
> 
> Can you clarify the intended path?

by Marcos Cáceres, [comment to w3c/strategy #530](https://github.com/w3c/strategy/issues/530#issuecomment-4384373803)

and 

> For the record: the TAG does have consensus on these concerns.
> 
> [design-reviews#1187](https://github.com/w3ctag/design-reviews/issues/1187) is a published collective review. Jeffrey re-opened it on April 8 confirming the concerns remain unresolved. At our April 7 meeting with DAS WG guests, Brian, Heather, and Jeffrey all voiced support for the signaling concern. The TAG appointed @christianliebel as deputy to work with the WG, documented in meeting minutes.
> 
> The decision to condition AC review on a response was the Team's (Feb 24): "Without such response, I don't think the charter should be sent to the AC for review." That was a Team decision, not a TAG request. The TAG asked for concerns to be addressed. That's our role per Process.
> 
> If the charter goes to AC with these concerns unresolved in the disposition, that's fine. But the disposition must accurately reflect that these are collective TAG concerns, not one individual's.
> 
> Also: [#798](https://github.com/w3c/charter-drafts/issues/798) and [#799](https://github.com/w3c/charter-drafts/issues/799) are W3C Member wide review concerns grounded in peer-reviewed security research, cross-engine implementation data, and WebKit's published [community positions](https://github.com/WebKit/standards-positions/issues/199). "One individual" is not an accurate characterization of concerns backed by a collective TAG review, a browser engine's community positions, and an academic paper from CISPA.

by Marcos Cáceres, [comment to w3c/strategy #530](https://github.com/w3c/strategy/issues/530#issuecomment-4397542820)

**Response** No action taken, just situation described against comments.
