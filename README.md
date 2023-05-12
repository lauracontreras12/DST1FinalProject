# Data Tools 1 Final Project - Gun Violence
Final Project for Data Science Tools 1. 
# Dataset
Our search on GitHub led us to James Ko's repository (https://github.com/jamesqo/gun-violence-data) that incorporated data from the Gun Violence Archive. James felt like the database was incompleted, so he included scripts on web-scrapping on filling in the crucial fields for each incident. His dataset is 260k gun violence incidents in the US between January 2013 to March 2018, inclusive.

The dataset contained the following 29 attributes:

* incident_id: (int) gunviolencearchive.org ID for incident
* date: (str) date of occurrence
* state: (str)
* city_or_county: (str)
* address: (str) address where incident took place
* n_killed: (int) number of people killed
* n_injured: (int) number of people injured
* incident_url: (str) link to gunviolencearchive.org webpage containing details of incident
* source_url: (str) link to online news story concerning incident
* incidents_url_fields_missing : (bool) ignore, always False
* congressional_district: (int)
* gun_stolen: (dict[int, str]) key: gun ID, value: "Unknown" or "Stolen"
* gun_type: (dict[int, str]) key: gun ID, value: description of gun type
* incident_characteristics: (list[str]) list of incident characteristics
* latitude: (float)
* location_description: (str) description of where incident took place
* longitude: (float)
* n_guns_involved: (int) number of guns involved
* notes: (str) additional notes about the incident
* participant_age: (dict[int, str]) key: participant ID
* participant_age_group : (dict[int, str]) key: participant ID, valuue: description of age group, e.g. 'Adult 18+'
* participant_gender: (dict[int, str]) key: participant ID, value: 'Male' or 'Female'
* participant_name: (dict[int, str]) key: participant ID
* participant_relationship: (dict[int, str]) key: participant ID, value: relationship of participant to other participants
* participant_status: (dict[int, str]) key: parrticipant ID, value: 'Arrested', 'Killed', 'Injured', or 'Unharmed'
* participant_type: (dict[int, str]) key: participant ID, value: 'Victim' or 'Subject-Suspect'
* sources: list(str) links to online news stories concerning incident
* state_house_district: (int)
* state_senate_district: (int)
You can run the scripts to download the dataset, or just download the csv file. Both Laura and I tried to run the scripts to get additional data past March 2018, but they didn't work for us.

We downloaded the csv file and selected 16 columns. Due to the lack of federal definition of mass shooting, we have defined a mass shooting as an incident with three or more fatalies. This definition significantly cut down the dataset of 260k+ incidents to just over 800 incidents.
