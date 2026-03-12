

Portfolio Data Model

You will keep 4 lists:
	1.	Daily Signal
	2.	Issues
	3.	Decisions
	4.	Milestones

Use these exact standard values across all lists.

Standard Program values
	•	BWC
	•	ALPR-LPR
	•	Mobile Fortify
	•	Mobile Identify
	•	Cross-Portfolio

Do not create alternate spellings.

⸻

1) LIST: Daily Signal

Purpose

Daily leadership brief source and publishing trigger.

List Name

Daily Signal

Required Columns

Display Name	Internal Name	Type	Allowed Values / Notes	Required
Title	Title	Single line text	Example: 2026-03-12 Daily Brief	Yes
Brief Date	BriefDate	Date only	One row per day	Yes
Prepared By	PreparedBy	Person or Group	Usually you	No
Programs Covered	ProgramsCovered	Choice (multi-select)	BWC, ALPR-LPR, Mobile Fortify, Mobile Identify, Cross-Portfolio	No
Portfolio Status	PortfolioStatus	Choice	Green, Yellow, Red	Yes
BLUF	BLUF	Multiple lines text	1–2 sentence summary	Yes
Leadership Awareness	LeadershipAwareness	Multiple lines text	Bullet-style text	No
Emerging Risks	EmergingRisks	Multiple lines text	Bullet-style text	No
Field Operational Updates	FieldOperationalUpdates	Multiple lines text	Bullet-style text	No
Leadership Decisions Needed	LeadershipDecisionsNeeded	Multiple lines text	“None today” if none	No
Post to Teams	PostToTeams	Yes/No	Default = No	Yes
Posted	Posted	Yes/No	Default = No	Yes
Posted Timestamp	PostedTimestamp	Date/Time	Set by flow	No

Optional Columns

Display Name	Internal Name	Type	Notes
Audience Type	AudienceType	Choice	Leadership, CIO, Ops, Security
Source Notes	SourceNotes	Multiple lines text	Scratchpad / ugly notes
Teams Message Link	TeamsMessageLink	Hyperlink	Optional later

Validation Rules
	•	One row per day
	•	Use this list for today’s signal only
	•	Do not use it as an issue register

⸻

2) LIST: Issues

Purpose

Persistent problems, blockers, and material concerns.

List Name

Issues

Required Columns

Display Name	Internal Name	Type	Allowed Values / Notes	Required
Title	Title	Single line text	Short issue title	Yes
Issue ID	IssueID	Single line text	Example: ALPR-I01	No
Program	Program	Choice	BWC, ALPR-LPR, Mobile Fortify, Mobile Identify, Cross-Portfolio	Yes
Issue Type	IssueType	Choice	Security, Privacy, Funding, Operations, Governance, Contracting, Technical	Yes
Description	Description	Multiple lines text	Clear problem statement	Yes
Impact	Impact	Choice	Low, Medium, High, Critical	Yes
Status	Status	Choice	Open, Monitoring, Blocked, Resolved	Yes
Owner	Owner	Person or Group	Single accountable owner	Yes
Date Opened	DateOpened	Date only	Start date	Yes
Target Resolution Date	TargetResolutionDate	Date only	Planned resolution target	No
Current Update	CurrentUpdate	Multiple lines text	Latest short update	No
Leadership Relevant	LeadershipRelevant	Yes/No	Default = Yes	Yes

Optional Columns

Display Name	Internal Name	Type	Notes
Cause	Cause	Multiple lines text	Root cause
Consequence	Consequence	Multiple lines text	What happens if unresolved
Linked Decision ID	LinkedDecisionID	Single line text	Example: ALPR-D02
Linked Milestone ID	LinkedMilestoneID	Single line text	Example: ALPR-M04
Source Link	SourceLink	Hyperlink	Doc, email, ticket, note

Validation Rules
	•	Every issue must have:
	•	one owner
	•	one impact level
	•	one status
	•	If it is time-bound only, it may belong in Milestones instead

⸻

3) LIST: Decisions

Purpose

Decision memory, leadership approvals, and pending choices.

List Name

Decisions

Required Columns

Display Name	Internal Name	Type	Allowed Values / Notes	Required
Title	Title	Single line text	Short decision title	Yes
Decision ID	DecisionID	Single line text	Example: ALPR-D01	No
Program	Program	Choice	BWC, ALPR-LPR, Mobile Fortify, Mobile Identify, Cross-Portfolio	Yes
Decision Type	DecisionType	Choice	Approval, Direction, Deferral, Escalation, Exception	Yes
Decision Statement	DecisionStatement	Multiple lines text	What decision is needed or was made	Yes
Status	Status	Choice	Pending, In Review, Approved, Deferred, Rejected, Closed	Yes
Decision Owner	DecisionOwner	Person or Group	Who owns the decision process	Yes
Date Raised	DateRaised	Date only	When entered into log	Yes
Decision Due Date	DecisionDueDate	Date only	When leadership input is needed	No
Outcome	Outcome	Multiple lines text	Final outcome or current answer	No
Rationale	Rationale	Multiple lines text	Why it matters	No
Leadership Required	LeadershipRequired	Yes/No	Default = Yes	Yes

Optional Columns

Display Name	Internal Name	Type	Notes
Revisit Criteria	RevisitCriteria	Multiple lines text	What would reopen it
Linked Issue ID	LinkedIssueID	Single line text	Example: ALPR-I01
Authority Level	AuthorityLevel	Choice	Program, Branch, Division, CIO, Other
Source Link	SourceLink	Hyperlink	Supporting doc or note

Validation Rules
	•	If it does not require a choice, approval, or direction, it is not a decision
	•	Every pending decision should have either:
	•	a due date, or
	•	a next step in Outcome/Rationale

⸻

4) LIST: Milestones

Purpose

Dates, events, deliverables, and gates that matter to timing.

List Name

Milestones

Required Columns

Display Name	Internal Name	Type	Allowed Values / Notes	Required
Title	Title	Single line text	Milestone name	Yes
Milestone ID	MilestoneID	Single line text	Example: ALPR-M01	No
Program	Program	Choice	BWC, ALPR-LPR, Mobile Fortify, Mobile Identify, Cross-Portfolio	Yes
Milestone Type	MilestoneType	Choice	Review, Deliverable, Pilot, Deployment, Decision Gate, Meeting, Other	Yes
Description	Description	Multiple lines text	What the milestone is	No
Milestone Date	MilestoneDate	Date only	Real target date	Yes
Status	Status	Choice	Upcoming, On Track, Delayed, Complete, Cancelled	Yes
Owner	Owner	Person or Group	Accountable owner	Yes
Dependency	Dependency	Multiple lines text	What must happen first	No
Leadership Relevant	LeadershipRelevant	Yes/No	Default = Yes	Yes

Optional Columns

Display Name	Internal Name	Type	Notes
Linked Issue ID	LinkedIssueID	Single line text	Example: ALPR-I01
Linked Decision ID	LinkedDecisionID	Single line text	Example: ALPR-D03
Notes	Notes	Multiple lines text	Extra context
Source Link	SourceLink	Hyperlink	Supporting doc

Validation Rules
	•	If it has no date, it is probably not a milestone
	•	If it is a recurring problem, it belongs in Issues

⸻

Standard Choice Sets

Daily Signal — Portfolio Status
	•	Green
	•	Yellow
	•	Red

Issues — Issue Type
	•	Security
	•	Privacy
	•	Funding
	•	Operations
	•	Governance
	•	Contracting
	•	Technical

Issues — Status
	•	Open
	•	Monitoring
	•	Blocked
	•	Resolved

Issues — Impact
	•	Low
	•	Medium
	•	High
	•	Critical

Decisions — Decision Type
	•	Approval
	•	Direction
	•	Deferral
	•	Escalation
	•	Exception

Decisions — Status
	•	Pending
	•	In Review
	•	Approved
	•	Deferred
	•	Rejected
	•	Closed

Decisions — Authority Level
	•	Program
	•	Branch
	•	Division
	•	CIO
	•	Other

Milestones — Milestone Type
	•	Review
	•	Deliverable
	•	Pilot
	•	Deployment
	•	Decision Gate
	•	Meeting
	•	Other

Milestones — Status
	•	Upcoming
	•	On Track
	•	Delayed
	•	Complete
	•	Cancelled

⸻

Naming Convention for IDs

Use this pattern:
	•	Issues: PROGRAM-I##
	•	Decisions: PROGRAM-D##
	•	Milestones: PROGRAM-M##

Examples:
	•	ALPR-I01
	•	FORTIFY-D02
	•	BWC-M03

Recommended program prefixes:
	•	BWC
	•	ALPR
	•	FORTIFY
	•	IDENTIFY
	•	PORT

⸻

Minimum Views to Create

Daily Signal
	•	Today’s Brief
	•	Needs Posting
	•	Red/Yellow Days

Issues
	•	Open Issues
	•	Leadership Relevant Issues
	•	Blocked Issues

Decisions
	•	Pending Decisions
	•	Leadership Required
	•	Closed Decisions

Milestones
	•	Next 7 Days
	•	Next 30 Days
	•	Delayed Milestones

⸻

MVP Automation Logic

Daily Brief Flow source

Use Daily Signal as the trigger list.

Rollup sources

Flow can later pull:
	•	open leadership-relevant Issues
	•	pending leadership-required Decisions
	•	next 7-day leadership-relevant Milestones

For MVP, Daily Signal alone is enough.
Your 4-list structure gives you room to mature without rebuilding.

⸻

Final Governance Rules

Daily Signal
	•	one row per day
	•	short bullets
	•	operational signal only

Issues
	•	persistent problems only
	•	one owner
	•	one impact
	•	one status

Decisions
	•	only real choices/approvals
	•	must show current status
	•	log outcome when complete

Milestones
	•	must have date
	•	must have owner
	•	status reflects reality

⸻

Final Recommendation

This schema is approved for build and verification.

Do not restart.
Normalize what you already built to this schema.

Confidence

High

Next step is a gap-analysis worksheet where you compare your existing columns to this approved schema and mark:
	•	keep
	•	rename
	•	add
	•	remove
