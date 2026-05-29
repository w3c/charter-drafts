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

**Response** The DAS WG appreciate the comment, and described situation in 
[w3c/strategy #530 comment](https://github.com/w3c/strategy/issues/530#issuecomment-4569236084), that these are 
[captured in Generic Sensors specification](https://w3c.github.io/sensors/#security-and-privacy) for sensor API specifications.

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

**Response** The TAG opened a PR [w3c/charter-drafts PR #806](https://github.com/w3c/charter-drafts/pull/806), 
the WG discussed on additional change over the PR but did not reach WG consensus. 

**Resolution** The draft charter has been updated following TAG proposal with adding amended text 
as `including for security and privacy enhancements`
to enable modification of adding new feature specifically related to security and privacy enhancements, 
at [w3c/charter-drafts PR #818](https://github.com/w3c/charter-drafts/pull/818), 

#### Involvement of multiple implementers - XXX (not Accepted, not Won't fix, ???)

> We want to ensure that the other specifications fill clear user needs and are making appropriate tradeoffs between those user needs and any potential abuse of the APIs. In many WGs, we can rely on all 3 browser engines to check this, but since this WG does not currently include participation from all major browser engines, we're more concerned here. Could you add this goal to the charter for each of the specifications in that class? We see, for example, https://github.com/w3c/vibration/issues/45 to do this for Vibration, but it would be good to use the charter to ensure it gets done.

**Response** The TAG opened a PR [w3c/charter-drafts PR #808](https://github.com/w3c/charter-drafts/pull/808), 
the WG discussed on additional change over the PR, but did not resolved. 

**Resolution** The draft charter has been updated following TAG proposal with integrating a change suggested by Anssi 
to remove specifically mention to WebApps, and with adding links to the Process for making maturity level used in text clear, 
by [w3c/charter-drafts PR #821](https://github.com/w3c/charter-drafts/pull/821).

#### Vibration API council concern - XXX

> The [Vibration Council recommended](https://www.w3.org/2025/08/vibration2-council-report.html#recommendations) that "the WG document the plan [to ship in multiple major browser engines] it thinks is best, whether or not that plan includes implementation in multiple browser engines, and a compelling rationale to help any reviewers decide whether the plan is acceptable." We couldn't find such a plan in this rechartering effort, and we encourage the WG to write such plans for each single-engine specification, in order to head off this possible formal objection.

**Response** The TAG opened a PR [w3c/charter-drafts PR #809](https://github.com/w3c/charter-drafts/pull/809) 
to add text not limited to the Vibration specification, but even further in relateion to TAG point 1, 
the WG did not reached a concensus to accept or reject the PR.

**Resolution** The draft charter has been updated following TAG porposal 
with adding amended text to enable bringing specifications into CG as incubation along with publication as Discontinued Draft, 
for making path clearer to continue incubation but not as completed end state, 
by [w3c/charter-drafts PR #819](https://github.com/w3c/charter-drafts/pull/819).

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

## Feedback provided to w3c/charter-drafts

### Peripheral APIs

Before submission by Mozilla to [whatwg/sg PR #264](https://github.com/whatwg/sg/pull/264/), 
three specifications (out of five listed in whatwg/sg PR #264) has been proposed to be included into tentative deliverables. 

#### Proposals raised by Mozilla - Accepted

**Resolution** The draft charter has been updated to include all three specifications proposed by issues to w3c/charter-drafts, 
and extended to 2 additional deliverables to allow the AC to weigh in, 
by PRs [w3c/charter-drafts PR #786](https://github.com/w3c/charter-drafts/pull/786) and 
[w3c/charter-drafts #820](https://github.com/w3c/charter-drafts/pull/820). 
We note disagreement from Apple on this resolution. 

##### Web Serial API

> Can Web Serial be moved from “tentative deliverable” to “deliverable” given Mozilla has announced an intent to prototype which would make two implementations?
> 
> Here's Mozilla’s intent to prototype: https://groups.google.com/a/mozilla.org/g/dev-platform/c/EDLTASS4Zik/m/LXJRL6yFCQAJ
> 
> We prefer to keep the existing note in the listing of the deliverable: "Note: This work may turn into a joint deliverable with the Web Applications Working Group."

by Haik Aftandilian, [w3c/charter-drafts #771](https://github.com/w3c/charter-drafts/issues/771)

##### WebUSB

> We (Mozilla Firefox) are considering the WebUSB API ([Firefox bug 2022432](https://bugzilla.mozilla.org/show_bug.cgi?id=2022432)) and thus request adding the WebUSB API in the DAS WG charter "Tentative Deliverables" as follows:
> 
> [WebUSB API](https://wicg.github.io/webusb/)
> An API for reading and writing from a USB device through script.
> Draft state: Draft Community Group Report
> Adopted Draft: [Adopted from WICG](https://wicg.github.io/webusb/)
> Note: This work may turn into a joint deliverable with the [Web Applications Working Group](https://www.w3.org/groups/wg/webapps).

by Haik Aftandilian, [w3c/charter-drafts #772](https://github.com/w3c/charter-drafts/issues/772)

##### Web Bluetooth

> We (Mozilla Firefox) are considering the Web Bluetooth API ([Firefox bug 2022433](https://bugzilla.mozilla.org/show_bug.cgi?id=2022433)) and thus request adding the Web Bluetooth API in the DAS WG charter "Tentative Deliverables" as follows:
> 
> [Web Bluetooth API](https://webbluetoothcg.github.io/web-bluetooth/)
> An API to discover and communicate with devices over the Bluetooth 4 wireless standard using the Generic Attribute Profile (GATT).
> Draft state: Draft Community Group Report
> Adopted Draft: [Adopted from Web Bluetooth Community Group](https://webbluetoothcg.github.io/web-bluetooth/)
> Note: This work may turn into a joint deliverable with the [Web Applications Working Group](https://www.w3.org/groups/wg/webapps).

by Haik Aftandilian, [w3c/charter-drafts #773](https://github.com/w3c/charter-drafts/issues/773)

#### Concern raised to Web Serial in tentative Deliverables - Rejected

> **Context:** This issue tracks a concern raised in the TAG review of the 2026 DAS WG charter (w3ctag/design-reviews#1187).
> 
> The TAG review states *(charter-affecting section, verbatim)*:
> 
> > "We're concerned by the appearance of Web Serial in the Tentative Deliverables. At least Mozilla seems inclined to start implementing that API, and we want it to live in a WG that all implementers are comfortable joining, to ensure that all of their potential concerns about engine/platform capabilities, privacy, and security can be easily raised. That said, its presence in this charter doesn't prevent it from being adopted by another WG instead."
> 
> Issue #771 proposes moving Web Serial from Tentative Deliverable to full Deliverable based on Mozilla's intent to prototype. However, the TAG's concern is specifically about **venue** — which WG is the right home for this work — not solely about the number of implementations. Moving it to a full DAS deliverable without resolving the venue question does not address the TAG's concern; it reinforces it.
> 
> Before this charter proceeds to AC review, the charter should either:
> 1. Document that the venue question has been discussed with the Web Applications WG and record the outcome, or
> 2. Explicitly state that Web Serial will not advance to full Deliverable in DAS until the venue question is resolved, and commit to a process and timeline for making that decision.
> 
> Related: #770, #771, w3ctag/design-reviews#1187

by Marcos Cáceres, [w3c/charter-drafts #783](https://github.com/w3c/charter-drafts/issues/783)

**Response** Five specifications of Peripheral APIs has been kept within the draft charter, to allow AC to weigh in. 
We note this disagreement on this resolution. 

#### Implementation across platform families - Deferred 

> Posting as W3C Member (not TAG Member).
> 
> The [DAS WG 2026 charter](https://w3c.github.io/charter-drafts/2026/das-wg-charter.html) includes a number of specifications that are not implemented on all major platforms. The charter does not address whether these specifications are expected to be portable across platform families, or what cross-engine support means when some platforms do not implement them.
> 
> **Existing sensor specifications and the Generic Sensor architecture**
> 
> Accelerometer, Gyroscope, Magnetometer, Ambient Light Sensor, Proximity Sensor, and Orientation Sensor each extend the [Generic Sensor](https://www.w3.org/TR/generic-sensor/) API. Per MDN Browser Compat Data: Accelerometer, Gyroscope, and Orientation Sensor ship in Chrome (67+) only; Magnetometer and Ambient Light Sensor are in Chrome behind a flag; Proximity Sensor has no implementation in any browser (no BCD entry exists). None are implemented in Firefox or Safari.
> 
> Meanwhile, [Device Orientation and Motion](https://www.w3.org/TR/orientation-event/) covers the primary orientation and motion detection use cases with multi-engine support: per BCD, DeviceOrientationEvent ships in Chrome 7+, Edge 12+, Firefox 6+, Safari 17+ (including iOS Safari 4.2+). DeviceMotionEvent ships in Chrome 31+, Edge 12+, Firefox 6+, Safari 17+ (including iOS Safari 4.2+).
> 
> The Generic Sensor stack provides additional capabilities beyond Device Orientation (raw sensor readings, standalone Magnetometer access, Ambient Light, Proximity), but the charter does not explain which use cases require these additional capabilities, or why both architectures need to continue receiving new features given that the higher-level API has achieved broader cross-engine adoption.
> 
> The TAG's review ([design-reviews#1187](https://github.com/w3ctag/design-reviews/issues/1187)) raised this concern directly:
> 
> > "We're concerned to see the Chromium-only Accelerometer, Gyroscope, and Orientation Sensor specifications in the charter, now that the Device Orientation and Motion spec is in Baseline."
> 
> **Tentative and proposed new deliverables**
> 
> Web Serial is a tentative deliverable. [PR #786](https://github.com/w3c/charter-drafts/pull/786) proposes adding Web Bluetooth and WebUSB as new tentative deliverables alongside Web Serial (which was already listed and is repositioned in the PR). These APIs expose raw transport protocols that are hardware-dependent by design. Per BCD, they ship only in Chromium-based browsers: Web Bluetooth (Chrome 70, Chrome Android 56), WebUSB (Chrome 61, Chrome Android 61), Web Serial (Chrome 89, Chrome Android 138), WebHID (Chrome 89, no Android support). Safari and Firefox do not implement them (Firefox BCD shows Web Serial at version 151, which is currently in beta, not yet in stable release).
> 
> The W3C [Ethical Web Principles](https://www.w3.org/TR/ethical-web-principles/#multi) (§2.11) state:
> 
> > "We will not create web technologies that encourage the creation of websites that work only in one browser, or only on particular hardware."
> 
> Does the charter expect these specifications to be portable across platform families? If not, how does the WG reconcile this with the principle above?

by Marcos Cáceres, [w3c/charter-drafts #799](https://github.com/w3c/charter-drafts/issues/799)

**Response** The DAS WG describes current implementation situation for sensor APIs, and demonstrated possibility of 
implementation accross multiple platforms like over CPUs and SoCs.

#### Potential security risk on sandbox escape via device APIs - Noted

> Posting as W3C Member (not TAG Member).
> 
> The [DAS WG 2026 charter](https://w3c.github.io/charter-drafts/2026/das-wg-charter.html) states the WG is committed to "security and privacy focused" specification development and that:
> 
> > "APIs in scope that expose sensitive data will define normative mitigations to address any known security and privacy threats."
> 
> ["Peripheral Instinct: How External Devices Breach Browser Sandboxes"](https://misc0110.net/web/files/peripheralinstinct_www25.pdf) (Trampert et al., CISPA Helmholtz Center for Information Security and Universität des Saarlandes; WWW '25, ACM ISBN 979-8-4007-1274-6/25/04) is a peer-reviewed paper studying WebHID, WebUSB, Web Serial, and Web MIDI. From the abstract:
> 
> > "we build several full-chain exploits, leading to arbitrary code execution on the victim system, circumventing the browser sandbox."
> 
> Of the four APIs studied, Web Serial is a tentative deliverable of this WG, and WebUSB is proposed as a tentative deliverable via [PR #786](https://github.com/w3c/charter-drafts/pull/786). WebHID and Web MIDI are not in the charter but belong to the same class of device browser APIs.
> 
> Findings relevant to this charter:
> 
> **Web Serial** (tentative deliverable): the paper identifies "several potential threats that can be exploited by a malicious actor that can control a modem via the Web Serial API" (§7). These include: dialing or sending SMS to premium-rate numbers; accessing "sensitive information such as two-factor authentication codes or passwords" contained in SMS messages which "can even be intercepted by forwarding SMS messages and calls to the attacker's number" (§7); GPS tracking ("many modems contain a GPS module that allows the modem to determine its location, which allows tracking a user's location"); and permanent SIM card lockout ("PIN and PUK are entered using AT commands, which allows an attacker to perform a permanent DoS that locks the SIM card").
> 
> **WebHID**: "We investigate the features of 22 devices from 15 vendors" and found "reprogrammable on-board macro functionality supported by 14 devices" (§5.1.1). Configuration of the shortest malicious payload takes as little as ~20 ms (Table 2, Logitech G500s). The researchers built full exploit chains achieving arbitrary code execution on Windows (§6.1), macOS (Appendix D.2), and Linux (Appendix D.1).
> 
> **WebUSB**: the researchers "flash custom firmware on peripheral devices, such as the blink(1)" (a USB RGB LED notification light), "completely overtaking and repurposing the device" (§4.1). The paper describes the general attack pattern: "a non-input device can be maliciously repurposed as a keyboard, allowing attackers to inject arbitrary keystrokes into the system."
> 
> **Web MIDI**: "we can flash firmware on MIDI devices to repurpose them for malicious use cases" (abstract), demonstrated on the Launchpad MK2 MIDI controller where they "successfully patch the firmware achieving arbitrary code execution on the device" (§4.1).
> 
> **Permission model**: the paper cites Hazhirpasand et al. (2020), who "convinced up to 95 % of users into granting permissions leveraging a browser game" (§3.3). The paper notes: "Once permitted, the site can interact with the device without further consent on future visits" and that "an attacker can leverage permissions granted to another site via a Cross-Site Scripting (XSS), website compromise, or domain re-registration" (§3.3).
> 
> The paper concludes:
> 
> > "browser security should not rely on the secure implementation of third-party hardware"
> 
> and notes that the API specifications:
> 
> > "shift the responsibility to (unprepared) device vendors"
> 
> These findings suggest the current mitigation approach (permission prompts and blocklists) is insufficient for the threat model these APIs create, in which the host is a potentially malicious website rather than a trusted operating system. The charter does not acknowledge this changed threat model or explain how the WG's security approach addresses the class of attacks described above.
> 
> For reference, WebKit's published positions on the affected APIs:
> - WebUSB: [oppose](https://github.com/WebKit/standards-positions/issues/68) (privacy, security, device independence)
> - Web Bluetooth: [oppose](https://github.com/WebKit/standards-positions/issues/570) (privacy, security, device independence)
> - Web Serial: [oppose](https://github.com/WebKit/standards-positions/issues/199) (privacy, security, device independence, use cases, venue)
> - WebHID: [no position issued](https://github.com/WebKit/standards-positions/issues/510) (venue concern noted)

by Marcos Cáceres, [w3c/charter-drafts #798](https://github.com/w3c/charter-drafts/issues/798)

**Response** In specifications in CG space, these attack scenarios are largely acknowledged by the 
"Security Considerations" sections of these specifications.

**Resolution** Five specifications of Peripheral APIs has been kept within the draft charter, to allow AC to weigh in. 
We note this disagreement on this resolution. 


#### Remove potential joint deliverables for three Peripheral APIs - Accepted

> Update the notes that indicate Web Bluetooth, Web Serial, and Web USB may become joint deliverables with the WebApps WG, since WebApps is unable to accept any more specifications at this time.
> 
> @himorin , @anssiko, @reillyeon, @w3c/marcomm, @siusin  

by Léonie Watson, [w3c/charter-drafts #810](https://github.com/w3c/charter-drafts/issues/810)

**Response** The draft charter has been updated by [w3c/charter-drafts PR #812](https://github.com/w3c/charter-drafts/pull/812) to align with this comment. 

### Comments related to implementation status and language

#### Revise DAS WG charter with clearer implementation status - Accepted

> Each deliverable gets an "implementation status" and "expected progress" section to document the current state as of the time of chartering and the work the group will do to advance each deliverable.

by Reilly Grant, [w3c/charter-drafts PR #770](https://github.com/w3c/charter-drafts/pull/770)

**Resolution** Although this change does not satisfy concerns of the TAG, this change has been integrated into 
the draft DAS charter for better explanation. 

#### Support level of specification in each status section - Accepted

> **Context:** This issue tracks a concern raised in the TAG review of the 2026 DAS WG charter (w3ctag/design-reviews#1187).
> 
> The TAG review states *(charter-affecting section, verbatim)*:
> 
> > "We would like the WG to find a way to signal the expected support level for each specification... At a minimum, each document's support level should be in its SotD section, but ideally the WG would find a way to ensure that *developers reading a specification can tell at a glance which kind of document they're reading*."
> 
> PR #770 adds implementation status text to the charter itself, which is a welcome step. However, the charter currently makes no commitment to reflect that status in the specifications that developers actually read.
> 
> The charter should include language along the following lines *(proposed in [#770 (comment)](https://github.com/w3c/charter-drafts/pull/770#discussion_r2881370853))*:
> 
> > The Working Group will ensure that each specification clearly communicates both its implementation status and its intended trajectory along the W3C Recommendation Track. At a minimum, the Status of This Document section of each specification will describe the current level of implementation support and whether the specification is expected to advance toward widely implemented Recommendation status.
> >
> > For specifications with limited or single-engine deployment, the Working Group will ensure that the specification clearly signals its role and intended direction — for example, whether it is an experimental abstraction, a transitional design that points developers toward a consensus alternative, or work with limited deployment serving as documentation.
> >
> > The Working Group will review specifications with limited implementation support at least annually to evaluate their progress, relevance, and intended trajectory, and will document the outcome of those evaluations publicly.
> 
> Related: #770, w3ctag/design-reviews#1187

by Marcos Cáceres, [issue raised as w3c/charter-drafts #780](https://github.com/w3c/charter-drafts/issues/780)

**Response** Referenced PR [w3c/charter-drafts PR #770](https://github.com/w3c/charter-drafts/pull/770) has been integrated into the draft charter.

#### Implementation report and WG plan for Vibration API - Won't fix

> **Context:** This issue tracks concerns from both the W3C Council report and the TAG review of the 2026 DAS WG charter.
> 
? **W3C Council recommendation** (https://www.w3.org/2025/08/vibration2-council-report.html#recommendations, verbatim):
> 
> > "We recommend that the WG document what implementation experience the API currently has (issue 33). In the next rechartering process for the DAS WG, we anticipate that some W3C members will object to keeping a deliverable without a concrete plan and timeline for shipping in multiple major browser engines. We... recommend that the WG document the plan it thinks is best, whether or not that plan includes implementation in multiple browser engines, and a compelling rationale to help any reviewers decide whether the plan is acceptable."
> 
> **TAG review** (w3ctag/design-reviews#1187, charter-affecting section, verbatim):
> 
> > "We couldn't find such a plan in this rechartering effort, and we encourage the WG to write such plans for each single-engine specification, in order to head off this possible formal objection."
> 
> The current PR #770 adds the following "Expected progress" text for Vibration:
> 
> > "The Working Group will update the specification to modern web platform design principles and device haptics capabilities and continue to solicit feedback."
> 
> This does not constitute the plan the Council recommended. It contains no rationale, no criteria, and no timeline. Additionally, w3c/vibration#33 ("Update implementation report"), cited directly in the Council report, remains open as of this writing.
> 
> Before this charter proceeds to AC review, the charter should:
> 1. Reference a publicly available document describing the WG's concrete plan for Vibration, with the rationale the Council requested.
> 2. Commit to resolving w3c/vibration#33 (implementation report) before or during the charter review period.
> 
> *Note: The plan document itself need not appear in the charter — as discussed in PR #770, a reference to a published document is sufficient.*
> 
> Related: #770, w3ctag/design-reviews#1187, w3c/vibration#33

by Marcos Cáceres, [issue raised as w3c/charter-drafts #781](https://github.com/w3c/charter-drafts/issues/781)

**Response** Part of concern resolved by implementation report has been added by [w3c/vibration PR #55](https://github.com/w3c/vibration/pull/55).

### Other comments

#### Wrong listing of geolocation specification - Accepted

> GeoLocation is under active development, so it should be moved out of the maintenance section into the normative specs section.
> 
> @himorin , @anssiko, @reillyeon, @w3c/marcomm, @siusin  

by Léonie Watson, [w3c/charter-drafts #811](https://github.com/w3c/charter-drafts/issues/811)

**Response** Error fixed by [w3c/charter-drafts PR #813](https://github.com/w3c/charter-drafts/pull/813)

#### Mentioning Haptics in DAS charter - Accepted

> **Note:** This concern is raised by @marcoscaceres in his personal capacity as a W3C member, not on behalf of the TAG. The TAG review (w3ctag/design-reviews#1187) was published before PR #770 introduced this specific language.
> 
> PR #770 adds the following "Expected progress" text for Vibration:
> 
> > "The Working Group will update the specification to modern web platform design principles and **device haptics capabilities** and continue to solicit feedback."
> 
> The phrase "device haptics capabilities" is problematic. The current Web Applications WG 2026 charter (https://www.w3.org/2026/01/webappswg-charter-2026.html) explicitly includes in its scope:
> 
> > "Haptic input devices and their emitted events and/or data."
> 
> And lists as a WICG deliverable:
> 
> > "Haptics — An API allowing web applications to interface with haptic actuators, such as vibration motors found on gamepad controllers, and potentially other devices that provide haptic feedback."
> 
> Haptics is not listed as a joint deliverable between DAS and WebApps in either the current WebApps charter or the DAS draft charter. WebApps and the Immersive Web CG are also actively exploring related work (see https://github.com/immersive-web/proposals/issues/92).
> 
> The DAS charter text must either:
> 1. Confirm that Vibration remains a minimal primitive and explicitly remove the "device haptics capabilities" language, or
> 2. Explicitly establish a joint deliverable arrangement with the Web Applications WG for any haptics-related work, with a clear statement of scope differentiation.
> 
> As written, the language signals unilateral expansion into an area that is already in scope of another WG, without a coordination model.
> 
> Additionally, the TAG review (charter-affecting section) specifically called out Vibration for needing better documentation of user needs and tradeoffs, citing w3c/vibration#45. That issue ("Create an explainer") remains open with no progress.
> 
> Related: #770, w3ctag/design-reviews#1187, w3c/vibration#45, https://github.com/immersive-web/proposals/issues/92

by Marcos Cáceres, [issue raised as w3c/charter-drafts #782](https://github.com/w3c/charter-drafts/issues/782)

**Response** The draft DAS charter has been updated by [w3c/charter-drafts #807](https://github.com/w3c/charter-drafts/pull/807). 

#### Clarify haptics scope - Rejected

Adding `semantic haptic feedback` into Scope, and `Gamepad haptics are out of scope for this WG` into Out of Scope

by Anssi Kostiainen, [w3c/charter-drafts PR #816](https://github.com/w3c/charter-drafts/pull/816)

**Resolution** This change has not been integrated into the draft DAS charter.

#### Adding Web Haptics API, Revise DAS WG charter with a new deliverable proposed by Microsoft - Deferred

Adding `Web Haptics API` into tentative deliverables.

by Anssi Kostiainen, [w3c/charter-drafts PR #795](https://github.com/w3c/charter-drafts/pull/795)

**Resolution** [Discussion has been postponed](https://github.com/w3c/charter-drafts/pull/795#issuecomment-4502569096), and 
this change has not been integrated into the draft DAS charter. 
And related issue `Venue and scope: Web Haptics API` has been filed at [w3c/charter-drafts 802#](https://github.com/w3c/charter-drafts/issues/802).


