This repository is intend to scrub the internet for potential pursuits. In addition to running a search through the internet,
the agent will search through the procurement sites where we have accounts. Combining the internet-wide search and the information generated from our procurement portals,
we will receive a synthesis of information through an email blast. That same synthesis will connect to the opportunities dashboard and populate it with information. 

##PSEUDOCODE##

Order of Functions
1) The Scraper (Discovery via Gemini Auto Browse)
Instead of a script, you use the Gemini Side Panel in Chrome.

Part A (The Links): You provide Gemini with a "Master List" of URLs (URA, Beacon, PennBid).

Part B (The Scrub): You give Gemini a System Instruction-> "Every Monday, use 'Auto Browse' to visit these x URLs. Look for new headlines or links added since [Last Date]. Only pull the URL of the new posting; do not download the PDF yet."

a) Geography: Priority zones (Hazelwood, Uptown, Larimer).

b) Mission: Keywords like "Sustainability," "Equity," "Inclusion."

c) Sector: "Adaptive Reuse," "Urban Infill," "Municipal."

d) PGH Specifics: "Climate Action Plan 3.0," "2030 District."

e) Theme: "Passive House," "Mass Timber," "Net-Zero."

f) Govt Classification: City, County, URA, Housing Authority.

g) Certifications: MWDBE/WBE requirements.

h) Team Reqs: PHIUS, LEED AP, specific PM experience.

i) Deadlines: AI calculates "Due Date - Today's Date" to ensure it’s within the 10-60 day window.

k) Roles: AI identifies if the RFP asks for a "Lead Architect" (Prime) or a "Sustainability Consultant" (Sub).

Part C (The Initial List): Gemini generates a table in the side panel showing the Link, the Score, and the Rationale.

1d) Human Review (The Safety Valve)
You review the table Gemini just built.

If a link looks credible, you say: "Gemini, proceed with Step 2 for rows 1, 3, and 5."

2) Synthesis (The Deep Read)
Gemini then clicks those specific links.

Synthesis: It reads the page content (and any immediate text) to confirm if it meets your "Prime/Sub" and "Certification" requirements.

Strike Out: Gemini checks its own history. If it previously summarized a link for you, it will flag it as a duplicate.

3) Airtable & Zapier Integration
This is where the only "setup" happens.

Airtable: You use the Gemini "Google Workspace" Extension.

Action: You tell Gemini: "Now, take this finalized list and send it to my 'Pursuits' Airtable." * Zapier: Zapier monitors your Airtable. When it sees a new row, it triggers your Weekly Blast email automatically.
