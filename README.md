This repository is intend to scrub the internet for potential pursuits. In addition to running a search through the internet,
the agent will search through the procurement sites where we have accounts. Combining the internet-wide search and the information generated from our procurement portals,
we will receive a synthesis of information through an email blast. That same synthesis will connect to the opportunities dashboard and populate it with information. 

##PSEUDOCODE##

Order of Functions
1) Scraper--> first part of function will scrub the internet, second part of function will scrub portals,
   a) for each procurement portal, use username and password env file to login to procurement portals
   b) scraper engine:
       factors important to consider:
         x geography (city, county, state, region)
         y mission statement words ()
         z studio specific keywords ()
         aa pgh specific keywords()
         ## what other keywords should be considered?
         ## among the types of keywords (factors), which ones are a priority? --> make a scoring dictionary/matrix for each'
      gemini call to read RFP
      create a list of the RFPs have x, y and z and scores they have + a brief description of what the RFP entail
        ensure that rfp gets information that can be mapped onto the table (list fields)
      if there is redundancy between list from a previous week to current, strike out. 
   
3) Airtable Integration --> Based on brief description, link field (keywords) to content (key values)
   def send_to_airtable(project_data):
    payload = {
        "records": [{
            "fields": {
                "Project Name": project_data['title'],
                "Full Description": project_data['description'],
                "Source": "URA Portal"
5) Zapier--> Weekly Blast text formatting
   a) use end product of scraper engine + tell zapier to reformat these in the form of an email blast-- send to (provide list of emails)
