# 08 · Privilege, Discovery and Legal Process

**Status:** [✓ final] · v1.0.0 · 11 July 2026

⚠ This entire file concerns questions requiring external counsel in the relevant jurisdictions. It maps the terrain; it does not resolve it.

## A. Privilege, by jurisdiction

**United States.** Attorney-client privilege protects confidential communications between counsel and client for the purpose of legal advice, and is waived by disclosure to third parties outside the privileged circle. Two live questions. First, is the agent a third party? Routing privileged communications through a vendor's model, where content is retained on vendor servers per the DPA, invites the argument that confidentiality was not maintained; the better analogy (privileged material in a cloud email system, where privilege survives because the vendor is a conduit) is available but untested for a system that *reads, remembers and independently redeploys* the content. The conduit analogy weakens precisely where the product's features begin. Second, and worse: the agent may itself effect the disclosing act. If channel memory absorbs legal advice from one thread and reflects it in another thread with different membership, privileged content has been communicated beyond the privileged circle by a system the client deployed. Waiver by autonomous agent is a novel fact pattern; no one should volunteer to be its test case.

**European Union.** Under Akzo Nobel (C-550/07 P), legal professional privilege in European Commission competition investigations does not extend to in-house counsel communications at all. For organizations exposed to EU competition process, the Slack channels where in-house counsel work were already unprotected; the agent's memory now aggregates and organizes that unprotected material into a more discoverable form. Member-state privilege rules vary for other proceedings, but the Akzo baseline alone justifies the control below.

**Korea.** Korean law recognizes no general attorney-client privilege in the US sense. An attorney's duty of confidentiality and a testimonial refusal right exist, but there is no settled doctrine allowing a client to shield documents from seizure or compelled production on privilege grounds, and prosecutors' offices have historically obtained in-house legal communications in investigations. Legislative efforts to introduce an attorney-client privilege (byeonhosa-uiroe-in bimil-bohogwon) have recurred without enactment; current status should be verified before reliance: Unknown / Insufficient data as of this version. Practical consequence: for a Korean entity, the channel-memory problem is not waiver of a privilege (there is little to waive) but the creation of an organized, searchable, vendor-held compilation of legal communications available to investigating authorities through lawful process.

**Control that follows from all three:** the agent is excluded from any channel in which counsel gives or discusses legal advice, in every jurisdiction, without exception. This is the cheapest control in the study and the least likely to be adopted, because legal channels are where people most want a summarizing agent.

## B. Discovery and legal hold

Channel memory is plausibly a record: a stored compilation of organizational information, held by a vendor as processor. Three unresolved operational questions. Preservation: when a legal hold issues, can the deployer suspend memory expiry or modification for identified channels? Production: can memory contents be exported in reviewable form? Deletion in the ordinary course: does routine agent removal destroy what a reasonable-anticipation-of-litigation standard required be kept? All three are Unknown / Insufficient data (`12-open-questions.md`) and all three are questions a litigation opponent will eventually ask before the deployer has answers. In US practice, Rule 37(e) spoliation analysis turns on reasonable steps to preserve; "the vendor's memory system had no preservation interface" is an argument, not a defense, when the deployer chose the system.

Separately: agent outputs posted in channels are ordinary Slack records and are discoverable on the same basis as any message. The novel object is the memory, not the transcript.

## C. Regulated-records regimes

For financial services deployers, supervision and record-keeping rules (SEC 17a-4, FINRA supervision, and analogous regimes elsewhere) apply to business communications in Slack today; an agent that generates business communications at scale multiplies the retention surface, and an ambient agent that initiates communications creates records no human decided to make. Whether existing archiving connectors capture agent-initiated messages identically to human messages should be verified per deployment, not assumed. ⚠

Final Liability rests with the Human.
