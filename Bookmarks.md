###### Designing Machine Learning Systems (Chip Huyen)
- validate data & reject in the extracting phase !!
- try to implement MapReduce or Spark for the batch processing
- stateful computation in stream
	- joining new data computation with the older data computation
- batch feature aka static features
	- features extracted from batch processing
- the opposite is stream features aka dynamic features

###### Go through just-pandas-things
- https://github.com/chiphuyen/just-pandas-things/blob/master/just-pandas-things.ipynb
- InterpretML: https://interpret.ml/

###### Sampling
- for reliable models, you might want to use probability-based sampling
- labelling problems
	- handling the lack of hand labels
	- augmentation method if not enough data

--> feature scaling



![[Pasted image 20231212155527.png]]

###### Side note on setiment analysis
- since customer review are more focused on identifying problematic reviews
	- use POSITIVE, NEGATIVE, ANGRY


how to incorporate campaign as one of the feature?!
--> features importance


latest page - Chapter 5

read on xgboost
https://towardsdatascience.com/xgboost-an-intuitive-explanation-88eb32a48eff
read on LightGBM

latest page - 214





https://otexts.com/fpp2/intro.html

The simplest time series forecasting methods use only information on the variable to be forecast, and make no attempt to discover the factors that affect its behaviour. Therefore they will extrapolate trend and seasonal patterns, but they ignore all other information such as marketing initiatives, competitor activity, changes in economic conditions, and so on.


Time series models used for forecasting include decomposition models, exponential smoothing models and ARIMA models

bev - battery electric vehicle
phev - plug in hybrid electric vehicle

hev - hybrid electric vehicle
- this one cannot be externally charged
so hev is not considered as EV

battery swapping station
Baas - battery as a service

check malaysian government subsidies / policies / incentives for EV
- seems like a significant influence for EV adoption


ev players
- skoda
- aiways

range anxiety


car dealership challenges/opportunities
- affordability (for customer)
- diminished customer loyalty
- changing consumer buying behaviours
- rising interest rates

terms to explore further
- dealership inventory levels

lifecycle
- customer buy a secondhand car
- customer return for regular service & maintenance
- customer sells the car back
- recondition the car
- car is sold back to another customer

how to pitch to customer, to trade in their cars
if they are not actively using it
what are the worry/annoying/pain points that people have,
when they are considering whether they should sell their car or not
- what if their car is still on loan? maybe it's tedious, having to think about those finance terms
what is the trigger points that makes people wants to buy car
or change their car
- new salary
- new requirements - need bigger car
theres a group of people that will buy a new car once they paid off the loan tenure
- people are more likely to get a new car, instead of just using the paid off car?!
- since at this point they probably have a significantly higher salary?
- or they just got married, and both partner have their own cars
- now they only need one
- for this type of customers, for their next car purchase, will they buy secondhand or new car?

maybe can take advantage of new car waiting period
- let say it's 6 month, they can trade in their car now - and still use them, while waiting for their new car
- maybe trade in, get money - and lease/long-term-rent(6months) throughout the waiting period
- since they need to pay downpayment for their new car, instead of saving few months prior
- can just trade in their car for money to use for their downpayment, and still keep their current
- car through leasing

for ev
- ensuring online vehicle descriptions speak to relevant selling points

so what's the selling points for ev?!







Expectations for senior data analyst
- provide actionable reports - inform operational & business decisions
- lead collaboration between cross-functional teams
- drive communication/engagement between business stakeholders & technical project team
	- to align technical solutions to business expectations
- develop strategies based on data driven insights
- lead the incorporation of AI/ML in data analysis
- forge strong partnerships with various departments
- enforce data governance policies / improving data quality & integrity
	-  Data Governance: The Definitive Guide: People, Processes, and Tools to Operationalize Data Trustworthiness
- conduct workshops & training sessions - for advanced data analysis
- mentor and guide junior analyst
	- offering guidance
	- sharing knowledge/expertise
	- for technical & non technical aspect
- promote culture of knowledge sharing & continuous learning
	- cultivate a collaborative & growth-focused team environment, as a senior member of data team
- identify trends, patterns, and anomalies
- lead data mapping
- lead identification & resolution of data-related issues promptly
- define and document data elements
	- enabling self-explanatory data fields


competencies
- advanced proficiency in visualization tools
- proficiency in SQL
- aptitude to learn ai/ml tools
- excellent interpersonal skills
- savvy storyteller - ability to draw out implications of events & situations
- interest of new/emerging trends & technologies
- solid understanding of statistics
- good understanding of performance, scalability & reliability concepts
- ability to deliver workarounds quickly to ensure business as usual
- stay current with emerging trends & technologies in
	- data analytics
	- digital banking
	- financial services industries

bonus/plus
- experience in database, data model design
- proficiency in python
- experience in cloud
- familiarity with LLMs
- self-starter, proactive & resourceful
- high eq and patience to understand stakeholders' challenges & issues
- willing to learn new tech & systems quickly
- cognizant of agile devops processes, coding best practices & performance tuning



Start the day by scanning industry news websites, trade publications, and automotive-specific news sources to stay updated on the latest developments, announcements, and trends in the automotive sector

Dive deeper into emerging technologies impacting the automotive industry, such as electric vehicles (EVs), autonomous driving, connected cars, and mobility-as-a-service (MaaS). Read whitepapers, research reports, and case studies to understand the potential implications and opportunities.

Analyze market reports, industry forecasts, and statistical data related to the automotive sector. Look for key metrics such as sales trends, market share, consumer preferences, and regional dynamics. Identify patterns and insights that indicate emerging trends or shifting market dynamics.

Research competitors in the automotive industry to understand their strategies, product offerings, and areas of innovation. Analyze press releases, earnings reports, and company presentations to identify emerging trends and competitive threats.

Participate in webinars, virtual conferences, or industry events focused on automotive innovation and emerging trends. Engage with industry experts, thought leaders, and peers to gain insights, exchange ideas, and network with professionals in the field.

Review the research findings from Day 1, including notes, insights, and key takeaways. Summarize the most significant emerging trends and potential opportunities identified in the automotive industry.

Conduct a brainstorming session with relevant team members to discuss the emerging trends identified and brainstorm potential strategies and initiatives to capitalize on them. Encourage creativity and collaboration to generate innovative ideas.

Develop an action plan outlining specific steps, timelines, and responsibilities for implementing the identified strategies and initiatives. Prioritize initiatives based on their potential impact, feasibility, and resource requirements.


FIND ALL THE CAR BRANDS IN MALAYSIA


automotive market share in malaysia
- usually compared against TIV (total inventory volume)
need to pay attention to export volume
- export only account for ~1%. ~99% is domestic


how the OPR thingy affects consumers' behaviour in purchasing cars
Overnight Policy Rate (OPR)

disruption in supply chain due to major flood in malaysia
chip supply issue


explore:
- behavioural economics
- behavioural finance

what contributes to the cycle

people search for explanations that would make events understandable, often to an extent
beyond that which is appropriate. This is true in investing as it is in other aspects of life

Derive some ideas, on how knowing the cycle helps your task as a data analyst

Earners may choose to spend a higher percentage of their earnings on consumption because:
- the daily headlines are favourable
- they believe election results presage a stronger economy, higher incomes or lower taxes
- consumer credit has become more readily available
- asset appreciation has made them feel richer
- their team won the world series

aka 'wealth effect'
- demonstrates the contribution of psychology to behaviour
- and behaviour to short-term economic variation

short term relation related to inventories

velocity of inventories movement

the forecast that are potentially valuable are those that correctly foresee deviation from
long-term trends and recent levels

most economic forecasts are just extrapolations. Extrapolations are usually correct but not valuable

not valuable as in it will lead to average

by forecasting deviation from trends - mostly incorrect, only a small amount is correct

create dashboard to track commodities price

explore ali baba supply chain / logistics infrastructure
https://www.amazon.com/Smart-Business-Alibabas-Success-Strategy/dp/1633693295

explore carclarity company

explore strategic partnership

corporate finance
merger & acquisition

multi-armed bandit (MAB)
https://www.kdnuggets.com/2023/01/introduction-multiarmed-bandit-problems.html#:~:text=A%20multi%2Darmed%20bandit%20(MAB,medicine%20researchers%2C%20and%20marketing%20specialists.

to explore:
how does central bankers & tresurers manage cycles?!
- reducing money supply
- raising interest rate
- selling securities

tradeoff between keeping inflation under control & allowing economic growth
stimulus vs restraint

capitalism - socialism - communism

connections between cost of goods & inflation

injecting liquidity into the economy by buying securities

how does government manage cycles
- usually involves in taxing & spending

explore national debt


monetory policy


##### cycle in profits

profit cycles performs differently from economic cycle

technological development
social development
cultural development

selective perception
skewed interpretation

capitulation: 
![[Pasted image 20240215153015.png]]


to read:
- Caste: The Origins of Our Discontents
- Crying in H Mart: A Memoir
- 


Do a competitor study on CarClarity


LG 27 ultragear

to explore:
- risk management

explore the books mentioned in 'Mastering the Market Cycle'


study on grabs car rental initiative in Indonesia !!3

caricarz.com
- have filter for:
	- new car launches
	- ev
	- fresh graduate (literally meant for fresh grads) - low buget car
	- upcoming
	- 
- have a dedicated news section for EV !!
- have tabs on JPJ running number (latest license plate number)
- have sections for their tiktok videos
- have sections for their youtube videos
- AI powered search tab
	- will ask few questions, then suggest the most suitable cars for you (recommender system)
	- they group car cc into (Practical: below 1.5cc, Comfort: 1.6-1.8cc, Mature: above 2.0cc)
- have tabs on current fuel price
![[Pasted image 20240219120656.png]]

chargesini.com

government bodies:
National Electric Vehicle Steering Committee (NEVSC)
Energy Commission's (ST) licensing
charging stations throughout PLUS


eldertech
https://x.com/gregisenberg/status/1752754916186083728?s=20



e27.co


investment firms
- ascend angels
- 

ev-related startups
- volcon epowersports
	- ev offroad bikes / quads
	- some listed specs
		- motor (kw)
		- battery (kwh)
		- charger (level 1 charging) -> explore more on types of ev charger
		- final drive -> explore more on how ev is integrated into the drive train?

- ascend elements
	- sustainable lithium-ion battery materials and recycling --> explore more on battery manufacturing
	- battery recycling company in malaysia ??
	- company that properly dispose ev waste
	- ev waste management
		- https://www.reneos.eu/case/the-waste-management-hierarchy-how-to-deal-with-end-of-life-ev-batteries-1

- bang jamin
	- vehicle insurans in indonesia
		- have specific insurans for EV
			- 

explore bjak
	- bad reviews !!

### credit cycle

try to identify what cycles affect which activities

capital
- credit
- equity

To make money cheaper typically refers to reducing the cost of borrowing or accessing funds
In the financial world, if you offer cheap money, they will borrow, buy and build - often without
discipline, and with very negative consequences.

from the tech bubble, see where are we now in the ai bubble

money from VC funds caused far too many companies to be created, often with little in terms of business justification or profit prospects
much of the investment that went into it may never be recovered
Being positioned to make investments in an uncrowded arena conveys vast advantages.
Participating in a field that everyone’s throwing money at is a formula for disaster
It’s hard to fully understand most phenomena in the investment world unless you’ve lived
through them.

where are we standing in the various cycle in real time?

prudent: acting with care, and showing thoughts for the future

race to the bottom
	- lenders will finance less-deserving borrowers
	- lenders more accepting of weaker debt structure
	stacking the logs in the fireplace for the next bonfire
	--> bonds that lacks safety margin are issued
	--> and, cant be serviced if things get a bit worse

credit window
	- credit window shuts
	- existing debt cant be refinance
	- will proceed to default

the real estate cycle