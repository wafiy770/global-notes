#### Scope
###### Work with IT and cross functional teams to identify data sources, data collection and design aggregation mechanism

- current workflow - IT, HR connect us with their system vendors. 
- we'll directly discuss with their api/data team on how to configure the setup & what data we need. 
- Obviously, before this discussion happen will have a meeting with the specific departments on what kind of data they need, and how they want to see it
- The collection method, and how to aggregate the data is handled by us - as we are also the report builder
- some are very clear on what they want
- some are not aware of what they need
- usually my approach is to first understand what they want - to kind of assess their level of understanding
- follow up with asking how the data is going to help you with you task
- 

###### Act as a liason between the data science (Analytics) team and the data lake engineering team in building curated views required for reporting

- end to end development
- manage the extraction script, lake storage, database, orchestration method
- directly gather requirements from our different department
- wear the 2 hats - data engineering, analytics/report builder
- TO ASK - from this description, im assuming most of the pipelines in using the ELT framework?
- so I'll be responsible to handle the transformation, then serve the clean data to the report developer
- or, building the report is part of the job as well?
- and btw, the reporting scope consist of Malaysia team only? or?
###### Perform data quality checks and data clean up

- yeah so, since we are the one monitoring the pipelines daily - which include weekends as well
- of course we encounter some problems that range from 
- oh this is a bad practice from us - lets develop a better logic to fix this common issue
- to some random error that comes from the source itself - usually for this we'll feedback to the vendor to fix their error
- and include some quality check to reject the data before it flows into our database
- yeah of course there is case where unfortunately, the error flows inside
- for examples duplications of data - so i have to write a query to identify and remove them

###### Interface with business stakeholders in cross-functional teams to understand various applications and their data sets, including:
- manufacturing
- qa
- post-marketing surveillance
- yeah i'm already used to have a talk with other department managers & their team members both through formal meetings and informal/ad hoc talks to kinda see what their work flow and where the problem comes in
- even through previous job, where im a R&D engineer
- in product development/design, have to work together with QA team - procurement team - manufacturing team as well
- 60% of the manufacturing is in house factory
- so im already used to manufacturing environment, and have a good overview what their issue, and where their frustration comes in
- also back then when i was interning as process engineer Micron malaysia - i have experience in clean room manufacturing environment - as they are processing the semiconductor chips
- since my background in mechanical engineering - i have the capacity to quickly understand the data that they are working with

###### Develop data preprocessing tools as needed and data sets for the data scientists' consumption

- kinda similar to 2nd scope
- currently as a company we are in the beginning stage / demo to incorporate machine learning / modeling
- as F&B the resources in concentrated on operations side of things, very little budget is allocated for this type of development
- good time to share - our current data team consist of me and my other teammate, so 2 people
- previously i was the only one
- he is coming from data science experience, currently he's working 1 ML project
- i am working on another one which i did include in the resume
- so in terms of what is the ideal data sets that we want when working with ML project
- as mentioned involves a lot of preprocessing - especially for text data
- the current project im working on which is sentiment analysis from our customers' feedback
- there's a lot of messiness in the reviews
	- one quick example is how to handle emoji
	- convert it to text - i include this as a function in the preprocessing scripts
	- sometimes the reviews in chinese characters

###### Maintenance and understanding of the various business intelligence tools used to visualize and report team analytics result to the company

- very capable in power bi
- when speaking about maintenance, scaling is a big issue
- actually first few months into this job, the report size already exceeds our service limits
- so had to reoptimize the query - pushing the transformation upstream, removing unneeded columns when loading the dataset, and using a cheaper method to calculate the metrics inside the report
- sometimes this simple thing does not affect much when the building the report, but over time it adds up
- so i do introduce a standard method to keep it at minimum
- regarding the different tools -
- when i started my analytics journey, of course im considering the 3 most popular pbi, tableau & looker studio
- but back then from what i see a lot of malaysian companies are microsoft centric
- so pbi is best for integrating with all this microsoft products
- the various tools refer to what actually?!
- other part of maintenance is version control
- pbi on lower tier of subscription does not have a managed framework for version control
- so what did i do?!

#### Competencies

##### Required

###### Experience in data quality assurance, control, and lineage for large datasets in relational/non-relational databases
###### Experience managing robust ETL/ELT pipelines for big real-world datasets that could include messy data, unpredictable schema changes and/or incorrect data types

- add in - case where i need to identify the problematic rows first with SELECT, then manually DELETE AND INSERT
- emphasize on the early stages when i took over
- now there is a proper control in place
	- - eg: put additional column 'insertion method' - 'insertion time'
	-  always back up the DELETE query (save as SELECT first)
- with limited budget and resources - cant implement CI/CD pipeline for the database
- hands dirty on the manual stuff - but get the jobs done
###### Experience in implementing and maintaining BI tools linked to an external data warehouse or relational/non-relational databases is required
###### Demonstrated knowledge in SQL and relational databases is required
###### Demonstrated knowledge of managing large datasets in the cloud is required
 - the stack im using is microsoft azure based

###### Demonstrated coding abilities in Python or scripting language
- main is all the extraction scripts are built in python
###### Demonstrated familiarity with different data types as inputs (CSV, XML, JSON)
- POS system data is JSON
- manpower system is XML
- internal sharepoint documents is CSV
- reviews data stored as CSV
###### Demonstrated knowledge of database and dataset validation best practices
- clean, test, and version data
- dont have centralized platform to do this things (not using dbt cloud)
- small team - make a case to introduce new tools
- half medallion approach
- adls for our lake storage - straight ingestion from api / other sources - saved as csv
- temporary table before main table (gold standard?!) 
- not very rigid? important test that can break the pipeline or causes wrong ingestion?!
	- schema changes from the sources, additional columns / added columns in between
###### Demonstrated knowledge of software engineering principles and practices
- versioning using git
###### Ability to communicate effectively and document objectives and procedures
- leverage on frequent coms with department managers

###### Multi-language fluency preferred (English, Malay)


##### Good to Have

###### Knowledge in non-relational databases (MongoDB) is a plus
###### Experience with Salesforce data is a plus
###### Experience with Databricks and Spark is a plus
###### Experience in medical device, healthcare, or manufacturing industries is desirable
- leverage on past experience, design process always incorporate manufacturing method.
- experienced in product development cycle, so involves lots of discussions with in house manufacturing team & subcontractors manufacturing
- 80% on machining and injection molding process
- we do involves manufacturing team early in the design process
- so usually they'll share their pain points and what causes the parts to be defective, and we'll try our this cycle of parts design will benefit them as well
- throughout the development cycle, weekly meeting to discuss issues with QE team as well
- if theres issue we are responsible to investigate the root cause as well
- there's a lot of knowledge transfer between us 
- im more directly involved in the manufacturing process during my internship as a Process Engineering for wafer backgrinding (a subprocess to produce memory chips)
- project based internship - a lot of extracting data from the machine - very straightforward 
- back the the tools im using is just excel 
- leverage on statistical process control
  - catching outliers, trend, drift - investigate what influence this situation
  - for the wafer backgrinding, the requirement was for it to be on a range of specified thickness
  - there was like 8 machines. i extracted the monthly data for 3 months. and created a simple boxplots diagram to compare all the 8 machines
  - and the standard deviation for each of them is not statistically significant
  - but their mean is different
  - and we have a range of acceptable thickness for the final output
  - so you can imagine the machine is operating as it should, but the mean is very close to the lower end of the accepted thickness
  - the sd will increase as usage increase - since it is a physical cutter so wear and tear
  - so in the machine there is a function to vertically align the cutter, so the team is able to shift the whole distribution so that the mean is at the center of the control chart
  - so able to reduce the amount of non conforming part
  - 1 / 2 machine the horizontal alignment is not ideal so the variance is big
  - so by doing this boxplots comparison - i can suggest to them 2 control points. hey if the variance reach this threshold value - you guys should check the horizontal alignment
  - if the mean reached this figure - check the vertical alignment
  - during the period, theres a maintenance to change the cutter - so took the opportunity to analyse the variance before maintenance and after maintenance
  - ran a t-test, it is statistically significant. also suggest a base line of acceptable variance, and how the variance shift over time
  - make it a control point as well - consider replacing the cutter
###### HIPAA experience a plus
- safeguarding personal health data
- theres a built in hipaa-compliance manager in Azure services











- using all the context that i gain from the stakeholders
- and bring it together with new information gathered from the raw data

- add in - pair programming with my teammates
	- he's more experience then me in python & building model stuff
- have implemented a cleaner table what will be solely used for the machine learning stuff
	- having additional layer of transformation on top of our daily ETL pipeline

- introduced a standard naming convention and how we group the entities when building new pipelines and 
- even when builiding the pbi reports as well
- im pushing for the self-service analytics, eventhough there wont be report builders from their own department
- is good to have this standards, teammates scope is not focused on building this report, but sometimes he does build it
- i do plan ahead when builing stuff, so easier to train new employees if the team grows, and in the case of either of us finding better opportunities in other companies, easier to handover to the new member and he can pick up the pace faster

- talk about first handover experience
- back then just introduced the role data scientist (kinda do all) + a 3rd party service (whatever)
	- which is expected since the company just started this analytics journey
	- and focus on giving results to the stakeholders
	- lot of messiness, literally 0 documentations
	- the definition of certain columns, the how and why certain things are built is kinda loss
	- the how part is easier to digest, but the why takes quite some time
	- had to inititate conversations with the departments again - reunderstand their requirements etc.

- talk about challenges building dashboard
	- tables doesnt add up or some shit
	 - used to debug from wrong metrics calculation all the way to sql transformation bug and the data extraction script itself
	 - aggregation sometimes looks right - because its just a number but
	 - but this number is actually weird, so need to have the domain knowledge as well to identify this kind of thing

- talk about source in database
	- aggregate that thing into table
	- few rows with unexpected data
	- main table is corrupted
	- 


dashboard process
1. sandbox dashboard
2.  dev dashboard
3.  published dashboard



ask whether there is internal resources to ask for help

- being proactive in issues
	- first stage is notified by end users
	- second stage notifications
		- fix before it gets to users
	- third stage - currently I and the team is working on
		- data test in pipelines

analyst understand the pain of a poorly documented dataset
- talk on what improvement you bring

- add on when communicating with stakeholders
	- borrow concept from engineering - 5 whys
	- essentially try to pry deeper on how they want to use the data
	- sometimes they tell you what they want, but you dont know the why
	- if you know they why you incorporate that knowledge into the solution you are giving them

- informal conversations
	- sometimes people will express the pain points that they dont realise is solvable

focus on your impact
- in work its a team sport
- in interview focus on yourself

for measuring impact, always converge into business impact


talk about the simple price histogram
- they utilise it
- able to drive a conversation with marketing
- ongoing projects - optimize add on price point

lack of measuring marketing initiative impact
- talk on the voucher thingy
- how the price distribution change during the voucher period
- previously they only have a overview metrics of how effective the voucher is
- im able to provide insight on a deeper level
- hey eventhough the conversion rate is this much
	- but it is able to shift the price bucket 
	- so i would consider this succesful initiative
	- and we can use this knowledge for the next similar initiative
	- but as improvement, need to optimize better this price point
- currently, price histogram in dashboard they regularly use
- need to start small for collaboration, and deliver small impact repetitively
- is the better way to highlight the roles/tasks that we do
- and support them to better impact the business

highlight your actions throughout the project

highlight on driving initiative on ML projects
 - already have a network of data scientist & data engineer friends?!


Key points
- optimization of operations !!
- the 2 most important business unit is engineering and manufacturing
	- double down on these!!

- 









scope of the analysis
- on different departments
- on manufacturing
	1. supply chain
		1. inventory optimization
		2. demand forecasting
	2. product quality
		1. real time quality monitoring
		2. root cause
			- maximize this !! 
	 3. process
		 1. real time equipment & process monitoring
		 2. process capability
		 3. optimize maintenance
		 4. OEE & factory productivity
- on usage data of client using the pods (apps)
- 



![[Pasted image 20231220155111.png]]

After first identifying the business use cases, the next step in the journey is to assemble the data. Unfortunately, in manufacturing, there is so much data coming off of the factory floor, off of connected devices and sensors that data is often in silos. You have data for suppliers, processes, equipment, sales, and many other types of data as well. You need to wrangle that data, put it together, merge it, clean it, filter it if we need to and basically prepare it for analysis.

Once you do that, you can start to automate processes to look for signals such as defects, warranty claims, downtime or yield in the data. After we’ve done some initial exploration we may decide that there’s some standard ways we want to view things. We can create applications for real-time monitoring and dashboards that can be reused with new types of data.

Going beyond basic dashboards you can use [advanced analytics applications](https://www.spotfire.com/glossary/what-is-advanced-analytics.html) to build models for further prediction based analyses. Some of your input data could be pressure, temperature, or product measurements. You can use models to check or predict production volumes, equipment failure and product quality.

Once we have a good predictive model, we want to be able to push out alerts. One example of alerts is onto mobile devices.


## **Goals of manufacturing analytics**

The goal of manufacturing analytics is to go from a simple collection and display of data (descriptive) to being able to leverage that [data in real time](https://www.spotfire.com/glossary/what-is-real-time-data.html) (predictive) for detection of issues with processes and equipment, reducing costs and maximizing efficiencies throughout the supply chain with less overhead and risk. Manufacturing analytics make those insights available to everyone from the CEO down to the shop floor worker.

Manufacturing analytics can help improve the quality of a company’s end product. It does this through several processes such as data-driven product optimization, managing defect density levels and analyzing customer feedback and purchasing trends. Data-driven product optimization can rely on IoT sensors and machine learning models to optimize production based on many factors. By analyzing product usage in detail, manufacturers can reduce or increase components that lead to higher usage rates. As a manufacturer, you must keep your defect density ratio low. With data collected from digital factories, manufacturers can now more specifically understand process states that lead to increased defect density. Customer analytics enable you to understand customers’ buying habits and lifestyle preferences. Armed with the information of future buying behaviors, manufacturers can more accurately produce and deliver what customers actually want.

Manufacturing analytics can also increase production yield and throughput. One of the main ways it does this is through anomaly detection. Anomaly detection can alert factory supervisors of defects in their products early on in production so they can resolve issues quickly and without affecting the output. Anomaly detection utilizes a combination of IoT sensors, historical data, and machine learning algorithms to detect unusual data which might be an indication of a developing problem.

Manufacturing analytics can also reduce risks and costs associated with downtime or equipment failures. This is accomplished by identifying bottlenecks or unprofitable production lines, and by anticipating failures and decreasing machine downtime to reduce costs with [predictive maintenance](https://www.spotfire.com/glossary/what-is-predictive-maintenance.html) of critical assets.









[Analytics Engineering & Intelligence Manager Analytics Engineering & Intelligence Manager](https://www.linkedin.com/company/25567/ "https://www.linkedin.com/company/25567/")

[May 2023 - Present · 8 mosMay 2023 - Present · 8 mosRemoteRemote](https://www.linkedin.com/company/25567/ "https://www.linkedin.com/company/25567/")

• Manage a team of analytics engineers to design and implement data-driven solutions  
  
• Develop and maintain a robust data infrastructure, including  
data storage, data processing, and data visualization tools.   
  
Collaborate with internal IT Data & Analytics team as well as with business unit engineering and manufacturing teams to understand data requirements and develop custom solutions to meet their needs  
  
• Work with internal stakeholders to identify opportunities for data-driven optimization of operations  
  
• Ensure that all data management processes are compliant with relevant regulations and standards• Manage a team of analytics engineers to design and implement data-driven solutions • Develop and maintain a robust data infrastructure, including data storage, data processing, and data visualization tools. Collaborate with internal IT Data & Analytics team as well as with business unit engineering and manufacturing teams to understand data requirements and develop custom solutions to meet their needs • Work with internal stakeholders to identify opportunities for data-driven optimization of operations • Ensure that all data management processes are compliant with relevant regulations and standards

-   
    

[Senior Analytics Engineer Senior Analytics Engineer](https://www.linkedin.com/company/25567/ "https://www.linkedin.com/company/25567/")

[Mar 2023 - May 2023 · 3 mosMar 2023 - May 2023 · 3 mosUnited States · RemoteUnited States · Remote](https://www.linkedin.com/company/25567/ "https://www.linkedin.com/company/25567/")

**Skills:** Data Quality Assurance · Datasets**Skills:** Data Quality Assurance · Datasets

-   
    

[Analytics EngineerAnalytics Engineer](https://www.linkedin.com/company/25567/ "https://www.linkedin.com/company/25567/")

[Sep 2021 - Mar 2023 · 1 yr 7 mosSep 2021 - Mar 2023 · 1 yr 7 mosUnited StatesUnited States](https://www.linkedin.com/company/25567/ "https://www.linkedin.com/company/25567/")

Work with IT and cross functional teams to identify data sources, determine data collection and design aggregation mechanisms  
  
Act as liaison between the data science (Analytics) team and the data lake engineering team in building curated views required for reporting  
  
Perform data quality checks and data clean up  
Interface with business stakeholders in cross-functional teams, including manufacturing, quality assurance, and post-market surveillance to understand various applications and their data sets.  
  
Develop data preprocessing tools as needed and data sets for the data scientists’ consumption  
  
Maintenance and understanding of the various business intelligence tools  
  
Wrote complex SQL queries in database to analyze and manipulate data



specific examples from resume



Angelica & Charles
Norwati & Ann

intro script
- greetings - name
- pre Uni - bio, chem, phy
- path - mechanical engineering - UTM
- Internship - Process Engineer - Micron Semiconductor
- Right after Uni - first job - R&D Engineer (design & product development) - 2 years there
- Decided to transition into data industry - 1 year independent study
- First data job - 4Fingers - SG own F&B business - selling fried chicken (so think of Mcds & KFC)
- Overview current role - end to end report development
	- requirement gathering - extraction script - data pipeline - orchestration - report building
	- play the data engineer role - data analyst role - and the analytics engineer role (the one in the middle)

Let me elaborate further on my decision to transition into data industry

REASON FOR TRANSITION
- reading and having conversatins - exposed to data science / machine learning - Outside Malaysia already started in manufacturing industry implement data analytics
- close to none in malaysia - eventually start growing since big industry in Malaysia is manufacturing
- the RnD job is very demanding - so a faster way to transition is to commit full time
- First get data job in industry that already utilise it
- get experience - return back to manufacturing industry (leverage on my manufacturing knowledge)
- happy - see job listed - a good time to return back to this industry
- plus it is in Johor which is my hometown as well
- that's why i applied for this job

Im gonna stop here - I invite all questions - If you want me to elaborate on the projects/initiatives listed in resume - I'll happily do so


sentiment goreng
- few milestone in this project
- first demo [done]
- directly using pretrained llama2 model
- dev a script to parse reviews and output the sentiment & tagging [in local]
- using llama2 in huggingface
- currently still work in progress
- we do manage to convince the manager to allocate our time to continue this task after demo
- current challenges
	- reviews is 50% malay 50% english
	- currently deciding whether language detection task --> translate task --> sentiment + classification task
	- or fine tuning - involves a lot of labeling


1. sentiment analysis model - python, huggingface, tensorflow [what]
	1. pre train + finetune [how]
	2. [impact] ??
	3. business users can filter by category of reviews (eg: food or service) [business impact]
	4. business users can see overall sentiment (positive, negative, neutral/enquiry) [business impact]

2. report optimization project - azure synapse, power bi [what]
	1. push transformation upstream [how]
	2. eliminate report refresh error due to timeout [technical impact]
	3. cut report size by half [technical impact]
	4. cut report refresh time by half [technical impact]
	5. ready for scaling - can fit in more data and analysis inside [business impact]

3. reviews dashboard - [what]
	1. develop end-to-end pipelines to extract & store reviews online & food aggregators [how]
	2. business users just open 1 report in pbi to see all the reviews [business impact]

4. business metrics coordination with managers
	1. talking points - operations: productivity, marketing: pspd

5. management reporting framework - powerbi, M query, Dax [what]
	1. Collaborate with department managers the key information they are presenting weekly to top management, develop report & consolidate them into one workspace for all managers [how]
	2. Save managers time to manually create their final weekly report [business impact]
	3. report integrity - both top management and managers are seeing and presenting data from the same source [business impact]

6. troubleshoot end user issue

8. data infrastructure migration project [what]
	1. collaborate with the data engineer consultants [how]
	2. provide current framework data pipeline flow
	3. extra: current framework using vm + airflow as the orchestrator
		1. management wants full cloud base infra - better continuation & support
	4. once infra is built + the main pipelines
		1. continue develop for the remaining pipelines - azure functions, blob storage, synapse sql

###### Experience in medical device, healthcare, or manufacturing industries is desirable
- leverage on past experience, design process always incorporate manufacturing method.
- experienced in product development cycle, so involves lots of discussions with in house manufacturing team & subcontractors manufacturing
- 80% on machining and injection molding process
- we do involves manufacturing team early in the design process
- so usually they'll share their pain points and what causes the parts to be defective, and we'll try our this cycle of parts design will benefit them as well
- throughout the development cycle, weekly meeting to discuss issues with QE team as well
- if theres issue we are responsible to investigate the root cause as well
- there's a lot of knowledge transfer between us 

- im more directly involved in the manufacturing process during my internship as a Process Engineering for wafer backgrinding (a subprocess to produce memory chips)
- project based internship - a lot of extracting data from the machine - very straightforward 
- back the the tools im using is just excel 
- leverage on statistical process control
  - catching outliers, trend, drift - investigate what influence this situation
  - for the wafer backgrinding, the requirement was for it to be on a range of specified thickness
  - there was like 8 machines. i extracted the monthly data for 3 months. and created a simple boxplots diagram to compare all the 8 machines
  - and the standard deviation for each of them is not statistically significant
  - but their mean is different
  - and we have a range of acceptable thickness for the final output
  - so you can imagine the machine is operating as it should, but the mean is very close to the lower end of the accepted thickness
  - the sd will increase as usage increase - since it is a physical cutter so wear and tear
  - so in the machine there is a function to vertically align the cutter, so the team is able to shift the whole distribution so that the mean is at the center of the control chart
  - so able to reduce the amount of non conforming part
  - 1 / 2 machine the horizontal alignment is not ideal so the variance is big
  - so by doing this boxplots comparison - i can suggest to them 2 control points. hey if the variance reach this threshold value - you guys should check the horizontal alignment
  - if the mean reached this figure - check the vertical alignment
  - during the period, theres a maintenance to change the cutter - so took the opportunity to analyse the variance before maintenance and after maintenance
  - ran a t-test, it is statistically significant. also suggest a base line of acceptable variance, and how the variance shift over time
  - make it a control point as well - consider replacing the cutter

###### Demonstrated familiarity with different data types as inputs (CSV, XML, JSON)
- POS system data is JSON
- manpower system is XML
- internal sharepoint documents is CSV
- reviews data stored as CSV
	- comfortable working with this structure
	- main task is to unnest the data into mulitple flat tables

###### REPORT MAINTENANCE
- TIE BACK TO OPTIMIZATION PROJECT
- very capable in power bi
- when speaking about maintenance, scaling is a big issue
- actually first few months into this job, the report size already exceeds our service limits
- so had to reoptimize the query - pushing the transformation upstream, removing unneeded columns when loading the dataset, and using a cheaper method to calculate the metrics inside the report
- sometimes this simple thing does not affect much when the building the report, but over time it adds up
- so i do introduce a standard method to keep it at minimum
- regarding the different tools -
- when i started my analytics journey, of course im considering the 3 most popular pbi, tableau & looker studio
- but back then from what i see a lot of malaysian companies are microsoft centric
- so pbi is best for integrating with all this microsoft products
- the various tools refer to what actually?!
- other part of maintenance is version control
- pbi on lower tier of subscription does not have a managed framework for version control
- so what did i do?!


###### DATA QUALITY & CLEANUP
- yeah so, since we are the one monitoring the pipelines daily - which include weekends as well
- of course we encounter some problems that range from 
- oh this is a bad practice from us - lets develop a better logic to fix this common issue
- to some random error that comes from the source itself - usually for this we'll feedback to the vendor to fix their error
- and include some quality check to reject the data before it flows into our database
- yeah of course there is case where unfortunately, the error flows inside
- for examples duplications of data - so i have to write a query to identify and remove them
###### MESSY DATA
- add in - case where i need to identify the problematic rows first with SELECT, then manually DELETE AND INSERT
- emphasize on the early stages when i took over
- now there is a proper control in place
	- - eg: put additional column 'insertion method' - 'insertion time'
	-  always back up the DELETE query (save as SELECT first)
- with limited budget and resources - cant implement CI/CD pipeline for the database
- hands dirty on the manual stuff - but get the jobs done

WRONG COLUMN
- I just create 1 simple function in the extraction script itself
- compare the columns from the api response with the columns in our database
- if not match - dont ingest into datalake


PREPROCESS DATA FOR DATA SCIENCE TEAM
- so in terms of what is the ideal data sets that we want when working with ML project
- as mentioned involves a lot of preprocessing - especially for text data
- the current project im working on which is sentiment analysis from our customers' feedback
- there's a lot of messiness in the reviews
	- one quick example is how to handle emoji
	- convert it to text - i include this as a function in the preprocessing scripts
	- sometimes the reviews in chinese characters
	- build function to detect if in chinese - then skip this row (since the reviews in chinese is very little) so it is not significant
- since my team is small, I create some simple reusable function to preprocess this type of problems


###### Demonstrated knowledge of building, maintaining, and scaling business Intelligence Report
- building - their request changes, can build pbi report from scratch
- maintaining - goes hand in hand with scaling
	- the past project that i worked on is initiated due to scaling issue
	- report size exceed limit
	- identify unused columns, when importing tables into pbi
		- a bit tricky - a lineage of measurements calculated (use tabular editor to track)
		- something simple such as an aggregated tables
		- push this transformation upstream in the Synapse sql pool (more processing power)
		- organized and group the different entity - looks more cleaner
		- initiated naming conventions - easier to understand
			- this naming type reference a column name, this reference table name, this reference measure name
			- because at some point different people will be working on this report so start early
			- even when im developing new metrics for new request, easier & faster for myself to do it
		- documenting - because i write codes as well, so already used to writing comments
		- using the same principle comments to explain why im doing this, instead of how im doing this
		- because one of the pain points when i first start this job, there's literally 0 documentations. So i have to track down everything and ask the report user for some gaps in the knowledge
		- btw very understanble since early development - so focus more on delivering the reports to the user
		- now most important report is done - so during new development can also incorporate standardize workflow

engineering background
- undertand the term better
- can communicate with mechanics & customer

introduce more filters
- filter based on customer profile
- etc. family, frequent traveller, daily city usage
- show features based on this grouping
- eg. family trunk size
- frequent traveller horsepower, full tank max km how much


kong yin
shu han
