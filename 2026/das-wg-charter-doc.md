# Disposition of Comments for the Devices and Sensors Working Group Charter

This document is the disposition of comments received during the review
of the [Devices and Sensor Working Group draft charter](https://w3c.github.io/charter-drafts/2026/das-wg-charter.html).

Comments were received through:

- [w3c/strategy #530](https://github.com/w3c/strategy/issues/530) — Strategy funnel issue (horizontal reviews)
- [w3ctag/design-reviews #1187](https://github.com/w3ctag/design-reviews/issues/1187) — TAG review
- [Issues](https://github.com/w3c/charter-drafts/issues?q=is%3Aissue+[wg%2Fdas]) and [pull requests](https://github.com/w3c/charter-drafts/pulls?q=is%3Apr+%5Bwg%2Fdas%5D) (PRs) in [w3c/charter-drafts](https://github.com/w3c/charter-drafts/) repository

## Executive summary

The charter refinement phase for the Devices and Sensors Working Group charter triggered substantive discussions between the Working Group, the TAG, other Members and the Team. This disposition of comments only tracks high-level comments. Please check the above channels for details. Of the 16 high-level comments received:

* 4 were Accepted and the proposed text integrated in the draft charter;
* 4 were Accepted with amended text or partially accepted;
* 6 were Noted, without leading to further charter changes;
* 2 were Declined.

Some of the accepted changes do not have Working Group consensus. In general, the Chairs of the DAS Working Group note that the group strictly follows Process requirements, and that some of the proposed changes would better be brought to the Process document, within the Process Community Group and the Advisory Board, to ensure cohesion, separation of concerns and broad membership support for the procedures that govern Working Groups.

Other changes such as the inclusion of 5 peripheral API specifications as tentative deliverables trigger additional concerns, about the right venue for the development of the specifications and support across implementers. The specifications were added to the draft charter to give the Advisory Committee the opportunity to weigh in during their review.

## Horizontal reviews

### Accessibility - Noted

> no comment or request from APA.

by Ruoxi Ran, [w3c/strategy #530 comment](https://github.com/w3c/strategy/issues/530#issuecomment-3848060439)

### Security - Noted

> hi, we have one comment from security, as the charter is focused on privacy and security, have you already a list of the main threats, and have you evaluated to put them in the charter itself?

by Simone Onofri, [w3c/strategy #530 comment](https://github.com/w3c/strategy/issues/530#issuecomment-3848628218)

**Response:** No changes were made to the draft charter. The DAS Working Group does not maintain a single list of main security and privacy threats. While there are some common themes among APIs (e.g. there are some threats common to sensor APIs that are captured in the [Generic Sensors specification](https://w3c.github.io/sensors/#security-and-privacy)), putting something together that covers all the specifications under the charter (e.g. [Contact Picker](https://www.w3.org/TR/contact-picker/#privacy), which has a very different set of considerations than sensor APIs) would risk creating overlap with W3C-level security and privacy guidance such as the [Threat Model for the Web](https://www.w3.org/TR/threat-model-web/) and the TAG's [Security and Privacy Questionnaire](https://www.w3.org/TR/security-privacy-questionnaire/). To the extent where it would be valuable to collect common security and privacy guidance in a single place, the Generic Sensors example is a good compromise between not duplicating high-level web platform design guidance and gathering domain-specific considerations.

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

**Response:** Internationalization WG was added to the Coordination section through [w3c/charter-drafts PR #804](https://github.com/w3c/charter-drafts/pull/804).

## TAG review 

The TAG raised 5 main points of concerns ([w3ctag/design-reviews #1187 comment](https://github.com/w3ctag/design-reviews/issues/1187#issuecomment-3889788860)), and provided pull requests for 4 of these points.

*Note:* A number of intermediary issues, pull requests and comments were made while attempting to resolve these concerns. This disposition of comments sticks to high-level comments for readibility. Please check the [Strategy issue](https://github.com/w3c/strategy/issues/530), [TAG design review issue](https://github.com/w3ctag/design-reviews/issues/1187) and [draft charter repository](https://github.com/w3c/charter-drafts) for details.

### Specifications with one implementation - Accepted with amended text, no WG consensus

> We're concerned to see the Chromium-only Accelerometer, Gyroscope, and Orientation Sensor specifications in the charter, now that the [Device Orientation and Motion](https://www.w3.org/TR/orientation-event/) spec is in Baseline. It makes sense to maintain non-consensus specifications while websites switch over to equivalent consensus APIs, but the charter should commit to only adding new features to the consensus versions. If there's not enough consensus on the new features to incorporate them into the core [Device Orientation and Motion](https://www.w3.org/TR/orientation-event/) spec, this WG could develop an extension specification that allows websites to mostly use the Baseline feature, with a few engine-specific extensions.

The TAG provided [w3c/charter-drafts PR #806](https://github.com/w3c/charter-drafts/pull/806) to address this concern.

**Response:** Expected progress for the deliverables was added to the charter. The "Status of this Document" sections of these deliverables were also updated to clarify the implementation status for developers and implementers. Additionally, the proposal from the TAG was integrated in the draft charter, with amended text to call out the possibility to work on security and privacy enhancements, through [w3c/charter-drafts PR #818](https://github.com/w3c/charter-drafts/pull/818). This update does not have consensus in the DAS WG.

### Involvement of multiple implementers - Accepted with amended text, no WG consensus

> We want to ensure that the other specifications fill clear user needs and are making appropriate tradeoffs between those user needs and any potential abuse of the APIs. In many WGs, we can rely on all 3 browser engines to check this, but since this WG does not currently include participation from all major browser engines, we're more concerned here. Could you add this goal to the charter for each of the specifications in that class? We see, for example, https://github.com/w3c/vibration/issues/45 to do this for Vibration, but it would be good to use the charter to ensure it gets done.

The TAG provided [w3c/charter-drafts PR #808](https://github.com/w3c/charter-drafts/pull/808) to address this comment.

**Response:** The proposal from the TAG was integrated in the draft charter (with minor text adjustments), through [w3c/charter-drafts PR #821](https://github.com/w3c/charter-drafts/pull/821). This change does not have consensus in the DAS WG though. The WG chairs note that the WG is committed to making appropriate tradeoffs between use cases and risks of abuse, as demonstrated by productive collaborations with privacy and security researchers and horizontal groups, and as codified in the Motivation and Background section in the draft charter, and that the WG continues to engage with non-participating browser engines as appropriate per the W3C Process.

### Vibration API council concern - Accepted with amended text, no WG consensus

> The [Vibration Council recommended](https://www.w3.org/2025/08/vibration2-council-report.html#recommendations) that "the WG document the plan [to ship in multiple major browser engines] it thinks is best, whether or not that plan includes implementation in multiple browser engines, and a compelling rationale to help any reviewers decide whether the plan is acceptable." We couldn't find such a plan in this rechartering effort, and we encourage the WG to write such plans for each single-engine specification, in order to head off this possible formal objection.

Similar comments were made in the Strategy issue, including
[comment](https://github.com/w3c/strategy/issues/530#issuecomment-3917515554), 
[comment](https://github.com/w3c/strategy/issues/530#issuecomment-4206018777),
and [comment](https://github.com/w3c/strategy/issues/530#issuecomment-4210649633) by Marcos Cáceres. 

The TAG proposed [w3c/charter-drafts PR #809](https://github.com/w3c/charter-drafts/pull/809), which goes beyond the Vibration API specification to cover all deliverables shipping in a single browser engine.

**Response:** The proposal from the TAG was integrated in the draft charter, with amended text to making transition back to incubation possible for specifications that could end up being published as discontinued, through [w3c/charter-drafts PR #819](https://github.com/w3c/charter-drafts/pull/819). The WG disagrees with this change. The WG Chairs note that the WG follows all W3C Process requirements when transitioning its deliverables from one maturity stage to another, and that the proposed changes would better be brought to the Process document itself through the Process Community Group and the Advisory Board.

Also note that a new implementation report was created for the Vibration API specification, as recommended by the Council, through [w3c/vibration PR #55](https://github.com/w3c/vibration/pull/55).

### Support level in status section of specification - Accepted

> We would like the WG to find a way to signal the expected support level for each specification. There's some discomfort on the TAG with using the same spec status "Candidate Recommendation" for all of:
> * deprecated specs that are being maintained while websites migrate to a consensus replacement;
> * features that are stable in one engine but opposed by the others;
> * "living" consensus specs that never intend to advance to Recommendation; and
> * consensus specs that are intended to advance to Recommendation.
> 
> At the same time, we recognize that this is the only status the Process defines for patent protection of these kinds of specifications. At a minimum, each document's support level should be in its SotD section, but ideally the WG would find a way to ensure that _developers reading a specification can tell at a glance which kind of document they're reading_.

Several comments and associated pull requests were raised on similar grounds in the discussion that followed in the TAG review issue, the strategy issue, and the draft charter's repository, including [w3c/charter-drafts PR #770](https://github.com/w3c/charter-drafts/pull/770) by Reilly Grant, and [w3c/charter-drafts #780](https://github.com/w3c/charter-drafts/issues/780) by Marcos Cáceres.

The TAG prepared [pull requests](https://github.com/w3c/strategy/issues/530#issuecomment-4544003815) to add implementation status notes to the Status of this Document sections of individual specifications.

**Response:** The pull requests prepared by the TAG to update the specifications were merged. The draft charter was also updated through [w3c/charter-drafts PR #770](https://github.com/w3c/charter-drafts/pull/770) to convey the implementation status of the group's deliverables (see also the response from the previous comment).

Implementation status and standard positions of the different specifications are also maintained in [the WG's wiki](https://www.w3.org/wiki/DAS/Implementations), which also links to [wpt.fyi](https://wpt.fyi/) for test results. These resources are referenced from the specification headers, as proposed by the TAG.

### Web Serial in tentative deliverables - Declined

> We're concerned by the appearance of Web Serial in the [Tentative Deliverables](https://w3c.github.io/charter-drafts/2026/das-wg-charter.html#tentative). At least Mozilla seems inclined to start implementing that API, and we want it to live in a WG that all implementers are comfortable joining, to ensure that all of their potential concerns about engine/platform capabilities, privacy, and security can be easily raised. That said, its presence in this charter doesn't prevent it from being adopted by another WG instead.

The concern about the venue for this spec was also raised as W3C Member by Marcos Cáceres both in [the Strategy issue]((https://github.com/w3c/strategy/issues/530#issuecomment-4380513758)) and the [draft charter repository](https://github.com/w3c/charter-drafts/issues/783).

**Response:** Additional peripheral APIs were proposed for addition in the meantime by Mozilla, see below for details. Also these APIs do not have support from all implementers, multiple implementers expressed support for them. No change were made for Web Serial, which is still listed as a tentative deliverable in the draft charter.

### Flagging design review concerns - Noted

In parallel to 5 points of concerns, the TAG made a comment in the same post as:

> The following concerns don't affect the charter, but we want to flag a few issues that are likely 
to come up in future design reviews for the individual specifications:
> 
> * We will always look more critically at specifications developed by WGs without members from all major browser engines, since we want there to be [One Web](https://www.w3.org/TR/ethical-web-principles/#multi) in the long run, and the fact that some browsers decide not to implement, inherently means there are concerns with the design. The WG should be prepared to explain how the non-members' critical feedback has been sought and considered.
> * The Generic Sensor architecture seems overcomplicated overall. In reviews of features that use it, we'd appreciate some justification for why that architecture is better than defining APIs in a single layer, as [Device Orientation and Motion](https://www.w3.org/TR/orientation-event/) does.
> * Are the signals in the Battery API still the right ones to help websites help users achieve their goals? Would a "please reduce power use" signal be sufficient, with the UA in charge of deciding how the precise battery level and charging state contribute to that signal?

**Response:** These comments were noted by the DAS Working Group.

## Feedback provided to w3c/charter-drafts

### Peripheral APIs - Accepted

Mozilla noted [support for Web Serial](https://github.com/w3c/charter-drafts/issues/771), and requested the [addition of WebUSB](https://github.com/w3c/charter-drafts/issues/772) and the [addition of Web Bluetooth](https://github.com/w3c/charter-drafts/issues/773) as [Tentative Deliverables](https://w3c.github.io/charter-drafts/2026/das-wg-charter.html#tentative). In parallel, Mozilla also proposed the creation of a [Peripheral APIs WHATWG workstream](https://github.com/whatwg/sg/pull/264/) with the WebNFC and WebHID specifications. The possible creation of the workstream at WHATWG is still under consideration as this disposition of comments is written.

**Response:** Following discussions with implementers, the DAS WG and Web Applications WG co-chairs who indicated that the Web Applications WG is unable to accept any more specifications at this time, the draft charter now lists all 5 peripheral APIs (Web Bluetooth, WebHID, WebNFC, Web Serial, WebUSB) as tentative deliverables (to be developed solely by the DAS WG). Should the WHATWG workstream be created, the expectation is that the WG would not adopt these tentative deliverables. The peripheral APIs do not have support from all implementers, and Marcos Cáceres noted in particular [in a PR comment](https://github.com/w3c/charter-drafts/pull/786#issuecomment-4348603681) that WebKit has published *oppose* positions on Web Serial, WebUSB and Web Bluetooth.

### Implementation across platform families - Noted

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

**Response:** Proposals from the TAG that were integrated in the draft charter add constraints on deliverables shipping in a single browser engine. Additional support for some of the deliverables mentioned was provided during the charter refinement period. No further changes were made to the draft charter.


### Potential security risk on sandbox escape via device APIs - Noted

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

**Response:** The specifications were added as tentative deliverables to the draft charter. These attack scenarios are largely acknowledged by the "Security Considerations" sections of these specifications. Wide review on these specifications may also help detect and address more security risks.

### Implementation report and WG plan for Vibration API - Partially accepted

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

**Response:** The implementation report part was resolved through [w3c/vibration PR #55](https://github.com/w3c/vibration/pull/55). Integration of the text proposed by the TAG to address a similar councern (see TAG Vibration API council concern above) creates a plan for the Vibration API and other WG deliverables. There is no WG consensus on the plan though.

### Wrong listing of geolocation specification - Accepted

> GeoLocation is under active development, so it should be moved out of the maintenance section into the normative specs section.

by Léonie Watson, [w3c/charter-drafts #811](https://github.com/w3c/charter-drafts/issues/811)

**Response:** Error fixed by [w3c/charter-drafts PR #813](https://github.com/w3c/charter-drafts/pull/813)

### Adding Haptics to the DAS charter - Declined

A proposal was made by Microsoft to add the [Web Haptics API](https://github.com/w3c/charter-drafts/pull/795). Other related comments were made to drop or clarify the scope of the DAS WG charter with regards to haptics, which is already in scope of the Web Applications WG, see [comment by Marcos](https://github.com/w3c/charter-drafts/issues/782), and [pull request by Anssi Kostiainen](https://github.com/w3c/charter-drafts/pull/816).

**Response:** The Web Haptics API [was **not** added to the draft charter](https://github.com/w3c/charter-drafts/pull/795#issuecomment-4502569096), pending further incubation and discussion on the appropriate venue(s) for this proposal. Also, the draft charter no longer contains any reference to haptics.
