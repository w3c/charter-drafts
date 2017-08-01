# Disposition of Comments - AC Review of Service Workers WG Charter
## Summary
* [Proposed charter](https://w3c.github.io/charter-drafts/sw-charter.html)
* [Review form](https://www.w3.org/2002/09/wbs/33280/swwg-2017/results)
 * 23 Members supported; 5 members with suggested changes 
 * 0 Formal Objections

* Changes since review: as below, we added greater clarity around the testing and implementation success criteria. 
* [Link to diff](https://services.w3.org/htmldiff?doc1=https%3A%2F%2Frawgit.com%2Fw3c%2Fcharter-drafts%2F299e9ab77071361f52956e640e82509fe26a0909%2Fsw-charter.html&doc2=https%3A%2F%2Fw3c.github.io%2Fcharter-drafts%2Fsw-charter.html)

## Suggested Changes:

**Mozilla Foundation**: "all normative specification changes are generally expected to have a corresponding change" should end with "corresponding *test* change", I think.

*Accepted.*

**Microsoft Corp.**:"Microsoft would like to see the Success Criteria more explicit. First, this group is being proposed in the belief that it will get more participation than was possible when Service Workers was in scope for the Web Platform WG. That rationale should be stated in the charter, perhaps "If a critical mass of key stakeholders and implementers of this technology do not join the group, its charter should be re-examined by the W3C."

*Added*: "If a critical mass of key stakeholders and implementers of this technology do not join the group, its charter should be re-examined by the W3C."

**Microsoft Corp.**: Also, we'd prefer that the Success Criteria duplicate much of the language in the Web Platform WG charter that stresses the need for real world implementations, not just proof of concept or prototype implementations. Something like:
"The group will be considered successful if its deliverables are widely used. In particular:

Production of stable documents addressing the work items listed in the Milestones section.
A test suite for each deliverable with conformance criteria that provides evidence to support the position that there is good (though perhaps not perfect) interoperability.
Availability of authoring tools and validation tools.
User-community and industry adoption of the group deliverables.
Availability of multiple, independent, interoperable implementations of each deliverable in shipping or planned products. ""

*Added*:
...and a test suite for each deliverable, sufficiently broad to demonstrate interoperability.</p>

Each specification should have implementation reports showing adoption, fostering the ready availability of multiple, independent, interoperable implementations, including in browsers, authoring, and validation tools, and usage on the Web.
	
**JS Foundation**: We echo the comments made by Microsoft around defining more explicit success criteria
	
*Addressed above*

**Apple, Inc.**: 
"This specification defines an API" needs to go and say "that enables the teleportation of small mammals" or something that scopes it a little more.

*Added*: "that enables applications to take advantage of persistent background processing, including hooks to enable bootstrapping of web applications while offline." (No small mammals were harmed in the crafting of this comment.)

**Apple, Inc.**: 
Really no Coordination with Ecma/JS needed?

*Added*: [ECMA TC 39](http://www.ecma-international.org/memento/TC39.htm)

**Apple, Inc.**: 
"The charter says that specs 'should' have a privacy and security considerations section. I think that is or is close to a general 'must' at the W3C level so either should be deleted to go with the general policy, or made 'must'.

The charter says that consensus on a call or meeting is provisional until confirmed online after publication in meeting minutes. I don't think it's acceptable to have controversial questions published in minutes, which are easily missed. I think a clear separate message 'Call for consensus: do X' is required. I commented this way on a related charter before, and almost made this a FO then. 

Communication: Is it clear *how* (e.g. an online form) an external IPR commitment is acquired? Could we link to the form or whatever tool is used? Ideally this is a separate section, as it's not exactly 'communication' that it is about."

*No change*: We are taking these suggestions into a broader review of Chartering process and Working Group modes of practice. As regards the privacy and security considerations, such a section (and its adequacy) is effectively a must at this point.



**Digital Bazaar**: The creation of a test suite should be mandatory for exiting CR.

*Addressed above with clarifications to success criteria.*

