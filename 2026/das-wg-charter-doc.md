# Disposition of Comments for the Devices and Sensors Working Group Charter

This document is the disposition of comments received during the review
of the [Devices and Sensor Working Group draft charter](https://w3c.github.io/charter-drafts/2026/das-wg-charter.html).

Comments were received through:

- [w3c/strategy #530](https://github.com/w3c/strategy/issues/530) — Strategy funnel issue (horizontal reviews)
- [w3ctag/design-reviews #1187](https://github.com/w3ctag/design-reviews/issues/1187) — TAG review
- [Issues](https://github.com/w3c/charter-drafts/issues?q=is%3Aissue+[wg%2Fdas]) and [PRs](https://github.com/w3c/charter-drafts/pulls?q=is%3Apr+%5Bwg%2Fdas%5D) to [w3c/charter-drafts](https://github.com/w3c/charter-drafts/) repository

## Executive summary


* 5 were Accepted, and resulted in charter changes.
* 3 were Accepted with amended text, and resulted in charter changes.
* 6 were Noted, without requiring charter change.
* 1 was Deferred, to later discussion for entire W3C strategy and investigation during specification development.
* 1 was Declined, to allow the AC to weigh in.
* 2 were Rejected without change mage.
* 1 was Won't fix.

## Horizontal reviews

### Accessibility - Noted

> no comment or request from APA.

by Ruoxi Ran, [w3c/strategy #530 comment](https://github.com/w3c/strategy/issues/530#issuecomment-3848060439)

### Security - Noted

> hi, we have one comment from security, as the charter is focused on privacy and security, have you already a list of the main threats, and have you evaluated to put them in the charter itself?

by Simone Onofri, [w3c/strategy #530 comment](https://github.com/w3c/strategy/issues/530#issuecomment-3848628218)

**Response** The DAS WG appreciate the comment, and described situation in 
[w3c/strategy #530 comment](https://github.com/w3c/strategy/issues/530#issuecomment-4569236084).

> The group does not maintain a single list of main security and privacy threats. While there are some common themes among APIs (e.g. there are some threats common to sensor APIs that are captured in the [Generic Sensors specification](https://w3c.github.io/sensors/#security-and-privacy)) putting something together that covers all the specifications under the charter (e.g. [Contact Picker](https://www.w3.org/TR/contact-picker/#privacy), which has a very different set of considerations than sensor APIs) would risk creating overlap with W3C-level security and privacy guidance such as the [Threat Model for the Web](https://www.w3.org/TR/threat-model-web/) and the TAG's [Security and Privacy Questionnaire](https://www.w3.org/TR/security-privacy-questionnaire/). To the extend where it would be valuable to collect common security and privacy guidance in a single place, I think the Generic Sensors example is a good compromise between not duplicating high-level web platform design guidance and gathering domain-specific considerations.

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

#### Specifications with one implementation - Accepted with amendment made

> We're concerned to see the Chromium-only Accelerometer, Gyroscope, and Orientation Sensor specifications in the charter, now that the [Device Orientation and Motion](https://www.w3.org/TR/orientation-event/) spec is in Baseline. It makes sense to maintain non-consensus specifications while websites switch over to equivalent consensus APIs, but the charter should commit to only adding new features to the consensus versions. If there's not enough consensus on the new features to incorporate them into the core [Device Orientation and Motion](https://www.w3.org/TR/orientation-event/) spec, this WG could develop an extension specification that allows websites to mostly use the Baseline feature, with a few engine-specific extensions.

**Response** The TAG opened a PR [w3c/charter-drafts PR #806](https://github.com/w3c/charter-drafts/pull/806), 
the WG discussed on additional change over the PR but did not reach WG consensus. 

**Resolution** 
The Working Group has added expected progress status for these deliverables to the charter and 
updated the "Status of this Document" section to provide clarity for developers and implementers.

And the draft charter has been updated following TAG proposal with adding amended text 
as `including for security and privacy enhancements`
to enable modification of adding new feature specifically related to security and privacy enhancements, 
at [w3c/charter-drafts PR #818](https://github.com/w3c/charter-drafts/pull/818), 

#### Involvement of multiple implementers - Accepted with amendment made

> We want to ensure that the other specifications fill clear user needs and are making appropriate tradeoffs between those user needs and any potential abuse of the APIs. In many WGs, we can rely on all 3 browser engines to check this, but since this WG does not currently include participation from all major browser engines, we're more concerned here. Could you add this goal to the charter for each of the specifications in that class? We see, for example, https://github.com/w3c/vibration/issues/45 to do this for Vibration, but it would be good to use the charter to ensure it gets done.

**Response** The TAG opened a PR [w3c/charter-drafts PR #808](https://github.com/w3c/charter-drafts/pull/808), 
the WG discussed on additional change over the PR, but did not resolved. 

**Resolution**
The Working Group is committed to making appropriate tradeoffs between use cases and risks of abuse, as demonstrated by productive collaborations with privacy and security researchers and horizontal groups. This is codified in the Motivation and Background section.

The Working Group continues to engage with non-participating browser engines as appropriate per the W3C Process.

The draft charter has been updated following TAG proposal with integrating a change suggested by Anssi 
to remove specifically mention to WebApps, and with adding links to the Process for making maturity level used in text clear, 
by [w3c/charter-drafts PR #821](https://github.com/w3c/charter-drafts/pull/821).

#### Vibration API council concern - Accepted with amendment made

> The [Vibration Council recommended](https://www.w3.org/2025/08/vibration2-council-report.html#recommendations) that "the WG document the plan [to ship in multiple major browser engines] it thinks is best, whether or not that plan includes implementation in multiple browser engines, and a compelling rationale to help any reviewers decide whether the plan is acceptable." We couldn't find such a plan in this rechartering effort, and we encourage the WG to write such plans for each single-engine specification, in order to head off this possible formal objection.

Similar comments have been added to w3c/strategy #530, such as 
[comment](https://github.com/w3c/strategy/issues/530#issuecomment-3917515554), 
[comment](https://github.com/w3c/strategy/issues/530#issuecomment-4206018777),
and [comment](https://github.com/w3c/strategy/issues/530#issuecomment-4210649633) by Marcos Cáceres. 

**Response** The DAS WG resolved to add new implementation report for recently started Recommendation track specification 
from Candidate Resommendation Snapshot by [w3c/vibration PR #55](https://github.com/w3c/vibration/pull/55). 

The TAG opened a PR [w3c/charter-drafts PR #809](https://github.com/w3c/charter-drafts/pull/809) 
to add text not limited to the Vibration specification, but even further in relateion to TAG point 1, 
the WG did not reached a concensus to accept or reject the PR.

**Resolution**
The Working Group continues to follow the W3C Process when transitioning its deliverables from one maturity stage to another.

The process changes drafted by the TAG are in the purview of the Process CG and the Advisory Board, to be discussed therein as appropriate. The Working Group does not adopt the proposed changes to the charter to ensure cohesion, separation of concerns and broad membership support for the procedures that govern the Working Groups.

The draft charter has been updated following TAG porposal 
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

In addition to concern raised in TAG comment, several comments to w3ctag/design0reviews and w3c/strategy 
has been made along with PRs to the DAS WG repositories by Marcos Cáceres, 
([first](https://github.com/w3ctag/design-reviews/issues/1187#issuecomment-4159936835), 
and [second](https://github.com/w3ctag/design-reviews/issues/1187#issuecomment-4163174410) at w3ctag/design-reviews #1187, 
and the same text posted as 
[first](https://github.com/w3c/strategy/issues/530#issuecomment-4159912174) and [second](https://github.com/w3c/strategy/issues/530#issuecomment-4163144358)
at w3c/strategy #530), and PRs have been closed without merging. 

In parallel, issue [w3c/charter-drafts #780](https://github.com/w3c/charter-drafts/issues/780) has been raised by Marcos Cáceres to track this concern, 
and the draft DAS WG charter has been edited to include inplementation status and 
expected progress by [w3c/charter-drafts PR #770](https://github.com/w3c/charter-drafts/pull/770).

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


#### Web Serial in tentative deliverables - Declined

> We're concerned by the appearance of Web Serial in the [Tentative Deliverables](https://w3c.github.io/charter-drafts/2026/das-wg-charter.html#tentative). At least Mozilla seems inclined to start implementing that API, and we want it to live in a WG that all implementers are comfortable joining, to ensure that all of their potential concerns about engine/platform capabilities, privacy, and security can be easily raised. That said, its presence in this charter doesn't prevent it from being adopted by another WG instead.

In addition to this concern, 
[additional comment]((https://github.com/w3c/strategy/issues/530#issuecomment-4380513758)) made by Marcos Cáceres to expand 
concern over other newly added tentative deliverables, and 
issue [w3c/charter-drafts #783](https://github.com/w3c/charter-drafts/issues/783) has been opened by Marcos Cáceres 
which has [marked as not a TAG consensus comment by Jeffrey Yasskin](https://github.com/w3c/charter-drafts/issues/783#issuecomment-4171422602).

**Response** 
The group has consensus to take up Mozilla's proposal to add Web Serial and other related specifications as a Tentative Deliverable in this Working Group. We also note that Mozilla has also started a parallel effort to create a WHATWG workstream for peripheral APIs. This may offer an alternative path for a forum that all implementers are comfortable joining.

Conversation held in [email thread](https://lists.w3.org/Archives/Public/www-archive/2026May/0000.html), 
no conclusion has made. 

### Other feedbacks on TAG review

#### Address TAG review and Council recommendation feedback - Rejected

> This PR applies the charter text suggestions posted in #770 (comment), addressing outstanding TAG review and W3C Council concerns. It is intended to be merged into PR #770 or land alongside it.
> 
> ## Changes
> 
> **Success Criteria — SotD signaling commitment** (addresses TAG charter concern, w3ctag/design-reviews#1187):
> Adds three paragraphs committing the WG to: signal implementation status and trajectory in each spec's SotD; clearly label the role of single-engine specs; and review limited-support specs at least annually with publicly documented outcomes. Closes #780.
> 
> **Vibration — Expected progress** (addresses TAG charter concern + Council recommendation):
> Replaces the vague "device haptics capabilities" text with a concrete commitment to publish the Council-recommended plan before AC review, with a visible `<i class="todo">` placeholder URL that must be filled in before the charter proceeds to AC review. Also requires the updated implementation report (w3c/vibration#33) to be publicly available before AC review opens. Coordinates haptics work with the Web Applications WG. Addresses #781, #782.
> 
> **Generic Sensor — Expected progress**:
> Removes "infrastructure for future sensor APIs" framing. Adds commitment not to charter new Generic Sensor-derived deliverables without first documenting the architectural rationale relative to single-layer API alternatives. HTML comment in source notes the grounding and TAG context.
> 
> **Ambient Light Sensor + Proximity Sensor — Expected progress**:
> Replaces vague "collect feedback and may publish a WD" with: proactively seek published implementer positions from non-participating engines, publish a summary of responses (including non-responses), and document a trajectory decision publicly.
> 
> ## Tracking issues
> 
> - #780 — SotD signaling commitment
> - #781 — Vibration Council plan before AC review
> - #782 — Vibration haptics scope conflict with WebApps WG
> - #783 — Web Serial venue (not addressed in this PR — tracked separately)
> 
> cc @reillyeon @jyasskin @anssiko @himorin

by Marcos Cáceres, [w3c/charte-drafts PR #784](https://github.com/w3c/charter-drafts/pull/784)

**Resolution** Jeffrey Yasskin noted on this change that 
`Here are my current thoughts on the proposal in this PR. This is not TAG consensus—it's just me so far. 
We'll be discussing this in a TAG breakout later today, and hopefully we can report some more-unanimous position after that.`, 
and this change has been closed without integrating per other changes proposed by the TAG in consensus 
([w3c/charter-drafts PR #806](https://github.com/w3c/charter-drafts/pull/806), [w3c/charter-drafts PR #808](https://github.com/w3c/charter-drafts/pull/808)
and [w3c/charter-drafts PR #809](https://github.com/w3c/charter-drafts/pull/809)).

#### Flagging design review concerens - Noted

In parallel to 5 points of concerns, the TAG made a comment in the same post as:

> The following concerns don't affect the charter, but we want to flag a few issues that are likely 
to come up in future design reviews for the individual specifications:
> 
> * We will always look more critically at specifications developed by WGs without members from all major browser engines, since we want there to be [One Web](https://www.w3.org/TR/ethical-web-principles/#multi) in the long run, and the fact that some browsers decide not to implement, inherently means there are concerns with the design. The WG should be prepared to explain how the non-members' critical feedback has been sought and considered.
> * The Generic Sensor architecture seems overcomplicated overall. In reviews of features that use it, we'd appreciate some justification for why that architecture is better than defining APIs in a single layer, as [Device Orientation and Motion](https://www.w3.org/TR/orientation-event/) does.
> * Are the signals in the Battery API still the right ones to help websites help users achieve their goals? Would a "please reduce power use" signal be sufficient, with the UA in charge of deciding how the precise battery level and charging state contribute to that signal?

**Response** The DAS WG noted these comments and continue onversation during further design review over each specification.

## Feedback provided to w3c/charter-drafts

### Peripheral APIs

Before submission by Mozilla to [whatwg/sg PR #264](https://github.com/whatwg/sg/pull/264/), 
three specifications (out of five listed in whatwg/sg PR #264) has been proposed to be included into tentative deliverables. 

#### Proposals raised by Mozilla - Accepted

**Resolution**
The draft charter has been updated to include all three specifications proposed by issues to w3c/charter-drafts, 
and extended to 2 additional deliverables to allow the AC to weigh in, 
by PRs [w3c/charter-drafts PR #786](https://github.com/w3c/charter-drafts/pull/786) and 
[w3c/charter-drafts #820](https://github.com/w3c/charter-drafts/pull/820). 
We note disagreement from Apple on this resolution. 

These deliverables are not listed as joint deliverables with the Web Applications WG, 
by change made at [w3c/charter-drafts PR #812](https://github.com/w3c/charter-drafts/pull/812) following 
issue [w3c/charter-drafts #810](https://github.com/w3c/charter-drafts/issues/810) by Léonie Watson.

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

#### Implementation across platform families - Noted

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

**Response**
The DAS WG describes current implementation situation for sensor APIs, and demonstrated possibility of 
implementation accross multiple platforms like over CPUs and SoCs.

The draft DAS WG charter has been update to consider of single implementation status following change proposed by the TAG.

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


### Comments related to implementation status and language

#### Implementation report and WG plan for Vibration API - Won't fix

> **Context:** This issue tracks concerns from both the W3C Council report and the TAG review of the 2026 DAS WG charter.
> 
> **W3C Council recommendation** (https://www.w3.org/2025/08/vibration2-council-report.html#recommendations, verbatim):
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

No conclusion has been made in consensus for specification update plan of Vibration specification. 

### Other comments

#### Wrong listing of geolocation specification - Accepted

> GeoLocation is under active development, so it should be moved out of the maintenance section into the normative specs section.
> 
> @himorin , @anssiko, @reillyeon, @w3c/marcomm, @siusin  

by Léonie Watson, [w3c/charter-drafts #811](https://github.com/w3c/charter-drafts/issues/811)

**Response** Error fixed by [w3c/charter-drafts PR #813](https://github.com/w3c/charter-drafts/pull/813)

#### Mentioning Haptics in DAS charter

##### Remove `Haptics` from description of Vibration API - Accepted

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

##### Clarify haptics scope - Rejected

Adding `semantic haptic feedback` into Scope, and `Gamepad haptics are out of scope for this WG` into Out of Scope

by Anssi Kostiainen, [w3c/charter-drafts PR #816](https://github.com/w3c/charter-drafts/pull/816)

**Resolution** This change has not been integrated into the draft DAS charter.

##### Adding Web Haptics API, Revise DAS WG charter with a new deliverable proposed by Microsoft - Deferred

Adding `Web Haptics API` into tentative deliverables.

by Anssi Kostiainen, [w3c/charter-drafts PR #795](https://github.com/w3c/charter-drafts/pull/795)

**Resolution** [Discussion has been postponed](https://github.com/w3c/charter-drafts/pull/795#issuecomment-4502569096), and 
this change has not been integrated into the draft DAS charter. 
And related issue `Venue and scope: Web Haptics API` has been filed at [w3c/charter-drafts #802](https://github.com/w3c/charter-drafts/issues/802).


