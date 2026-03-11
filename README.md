This repository is intend to scrub the internet for potential pursuits. In addition to running a search through the internet,
the agent will search through the procurement sites where we have accounts. Combining the internet-wide search and the information generated from our procurement portals,
we will receive a synthesis of information through an email blast. That same synthesis will connect to the opportunities dashboard and populate it with information. 

##PSEUDOCODE##

a) Geography: Priority zones (Hazelwood, Uptown, Larimer).

b) Mission: Keywords like "Sustainability," "Equity," "Inclusion."

c) Sectors

d) PGH Specifics: "Climate Action Plan 3.0," "2030 District."

e) Theme: "Passive House," "Mass Timber," "Net-Zero."

f) Govt Classification: City, County, URA, Housing Authority.

g) Certifications: MWDBE/WBE requirements.

h) Team Reqs: PHIUS, LEED AP, specific PM experience.

i) Deadlines: AI calculates "Due Date - Today's Date" to ensure it’s within the 10-60 day window.

k) Roles: AI identifies if the RFP asks for a "Lead Architect" (Prime) or a "Sustainability Consultant" (Sub).

1) Automated Scraper (Headless Agent)

a) Trigger: Weekly scheduled "ping" via Zapier.

b) Scrub: Gemini API visits links (No login needed if the portal is public-facing).

c) Scoring Engine: Factors a-k are applied by Gemini during the browse session.

d) Initial Mapping: New links/titles are pushed to Airtable "Inbox."

e) Strike Out: Automated redundancy check against existing Airtable URLs.

2) Human Credibility Review

Staff checks the "Approved" box in Airtable for high-quality leads.

3) Automated Synthesis

Checking the box triggers Gemini to do a "Deep Read" of that specific link.

Populates Airtable with Prime/Sub roles and certification requirements.

4) Automated Weekly Blast

Zapier bundles all approved data into a formatted email blast.
