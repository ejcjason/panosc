# Common Portal Use Cases

### Actors

|Actor|Description|
|--- |--- |
|Admin|IT Staff|
|Facility Management (FM)|Directors, PaNOSC stakeholders (requiring metrics, usage, KPI...)|
|Instrument Responsible|Scientist in charge of an instrument|
|Intra-Facility Coordinator (IFC)|Coordinates the integration of different facilities into the PaNOSC data analysis cluster|
|Open Access User (OAU)|Public member wanting to analyse open data (typically with an affiliation to a research institute or university)|
|Proposal Team Member (PTM)|External user and Instrument Responsible|
|Scientist|Regroups Proposal Team Member and Open Access User|

### Scientific Use Cases

#### Accessing and searching for data

|ID|Actor|Story|Description|Priority|
|--- |--- |--- |--- |--- |
|1|PTM|I need to log into the portal using my institute credentials| |1|
|2|Scientist|I want to be able to find data to analyse for an experiment at a given institute||1|
|3|PTM|I want to access my experimental data||1|
|4|OAU|I do not belong to an institute but want to log in to analyse open data|AAI will be provided by the work done in WP6 | 2|
|5|Scientist|I want to explore/search for public analysis results||2|
|6|PTM|I would like to know who has accessed my experimental data||3|
|7|IR|I would like to know who has accessed data for my instrument||3|
|8|PTM|I would like to know when a data file has been modified or created for my proposal|Maintain a history of modifications|4|

#### Machine management

|ID|Actor|Story|Description|Priority|
|--- |--- |--- |--- |--- |
|1|Scientist|I would like to request a machine that is capable of analysing the data.|The machine is created and presented to the user→ remote desktop presented to user→ the experimental data is mapped to the machine|1|
|2|Scientist|I want to be able to extend the lifetime of my machine||1|
|3|Scientist|I want to be informed when a machine is going to be suspended and archived||1|
|4|Scientist|When I disconnect and then connect back to the machine I want the machine state to be preserved from the previous session||2|
|5|Scientist|I would prefer not to log in again to the remote machine after creating it.||2|
|6|Scientist|I would like to request custom resources (CPU, Mem, etc) for my analysis machine||2|
|7|PTM|I want to be informed when a machine has been created to analyse my data (even if created by someone else)||3|

#### Analysing data

|ID|Actor|Story|Description|Priority|
|--- |--- |--- |--- |--- |
|1|Scientist|I would like the data to be mounted to the file system on the machine||1|
|2|Scientist|I would like to have software (applications and libraries) available to analyse the data|install any software system proposes software relevant to the datascientist (or other user) proposes software|1|
|3|Scientist|I need to store the results of the analysis|Where are the results stored?|1|
|4|Scientist|I would like to request new software to analyse my data||2|
|5|Scientist|I want to submit a job to a compute cluster (parallel processing cluster for example)||3|
|6|Scientist|I want to install software that is not available in the software repositories (or proposed by the system)||3|
|7|Scientist|I want to know if analysis is already in progress for the same proposal||3|
|8|Scientist|I want to be able to analyse data from 10 years ago. I need the system and software to be capable or reading and analysing the data files from this period||4|
|9|Scientist|I would like to have software proposed to me to analyse data for my proposal||5|

#### Collaborations

|ID|Actor|Story|Description|Priority|
|--- |--- |--- |--- |--- |
|1|Scientist|I want to be able to collaborate with a colleague to analyse data together|Screen sharing, Chat, Video|2|
|2|Scientist|While collaborating in a data analysis remote desktop session I would like to take control of the analysis (keyboard and mouse input)||3|
|3|PTM|I would like to invite someone to collaborate on data analysis who is not part of the proposal team|Grant access|3|
|4|Scientist|I would like to request to participate in the data analysis collaboration but I am not part of the proposal team|Request access|3|
|5|OAU|I want to be able to contact (email) the proposal team about their data or published results||3|

#### Recording/playback of data analysis

|ID|Actor|Story|Description|Priority|
|--- |--- |--- |--- |--- |
|1|Scientist|I have finished analysing my data and I want make my process and results discoverable|How? Generate DOI? Pushed to metadata catalogue? Landing page? Search engines?|3|
|2|Scientist|I would like to know which jupyter notebooks have been used for a particular proposal (associate it to the proposal with the data catalogue)||3|
|3|Scientist|I want to see the analysis (process and results) made by somebody else on data I can access|historical analysis, historical datafrom an analysis DOI? (machine, data, environment)replay?|4|
|4|Scientist|I would like to know what Remote Desktop analysis has been performed on a particular dataset previously and by whom||5|
|5|Scientist|I want to see the analysis performed on a particular dataset (eg watch a video or follow analysis actions)||5|
|6|Scientist|I want to be able annotate my analysis recording so that somebody can follow more easily what I have done or jump to a particular step in the analysis|Add video editing techniques to add text/links to specific parts of the video. Show a timeline of video segments.|5|
|7|Scientist|I want to be able to record my voice while recording analysis processes||5|
|8|Scientist|I want to follow the previous analysis performed on a particular dataset and then modify the actions or analysis parameters|nice to have!|5|

#### Quota

|ID|Actor|Story|Description|Priority|
|--- |--- |--- |--- |--- |
|1|Scientist|I want to know how much quota I have remaining||2|
|2|Scientist|I want to be able to increase my quota||2|
|3|Instrument responsible|I want to increase someone's quota||3|
|4|OAU|I want to be able to buy credits to increase my quota in order to access analysis machines||5|

#### Assistance

|ID|Actor|Story|Description|Priority|
|--- |--- |--- |--- |--- |
|1|Scientist|I require help using my machine and require support staff / local contact to guide me.|Support staff can access the running machine (like a collaborator) and take control|2|
|2|Scientist|I want to find data analysis examples and tutorials|Link to WP8|4|

### Administrative Use Cases

|ID|Actor|Story|Description|Priority|
|--- |--- |--- |--- |--- |
|1|Admin|I need to be able to deploy updates with minimal down time|eg new web servers, new code release|1|
|2|Admin|I need to be able to manually scale the compute resources when necessary (directly on the compute infrastructure)|ie increasing/decreasing the resources for a given machine (nodes)|1|
|3|Admin|I need to block users due to abuse||1|
|4|Admin|I want to monitor all activity (resources being used, number of connections) over all machines and on a particular machine|Dashboard overview and details on particular machines|1|
|5|Admin|I want to see the machines states (active, suspended, archived, deleted (soft & hard)…) of all machines created||1|
|6|Admin|I need to notify users that we will take analysis resources offline|Eg for maintenance or updates. Give notification time (eg 1 day, 1 hour…)|1|
|7|Admin|I want to be able to add and manage system images (ie distros, compute resources)||1|
|8|Admin|I want to manage quotas|eg limit cpu and memory per user, use tokens system|1|
|9|Admin|I want to manage user roles|eg admin|1|
|10|Admin|I want to see what is happening on a Remote Desktop in case of abuse|Connect to RD|2|
|11|Admin|I want machines to be automatically archived after a given number of days after their creation.||3|
|12|Admin|I want to restore a machine that has been archived||3|
|13|Admin|I want to be able to see analysis resources/state for all other facilities||4|
|14|Admin|I want to be able to specify and build a remote desktop or jupyter environment|eg specify a container software and hardware requirements|4|

### FM and IFC Use Cases

|ID|Actor|Story|Description|Priority|
|--- |--- |--- |--- |--- |
|1|Facility|I want to see how many resources have been used during a given period (eg number of machines created, CPU hours, DOIs minted)|KPIs|1|
|2|IFC|Another institute wants to participate in Data Analysis as a Service. I would like to add another facility to the service providers||1|

