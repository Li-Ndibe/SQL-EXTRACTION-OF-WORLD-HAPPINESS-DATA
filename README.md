# SQL-EXTRACTION-OF-WORLD-HAPPINESS-DATA

The world happiness dataset contains 1,229 cells and 11 columns. Years under reveiw was from 2015 to 2022, with about 7 Regions.

5 variables of Economy_GDP, Family_SocialSupport, Health_LifeExpectancy, Freedom, Trust_GovtCorruption and Generosity  were used as metrics to determine the countries that ranked high in being happy. 

Data extraction was done using Microsoft SQL server while visualization and analysis was done using Tableau Public.

below are the metrics used for the extraction:


1.	-- COUNTRIES RANKING BETWEEN 130 AND 150 IN ECONOMY(GDP) I.E RANKING THE TOP 20 ALL YEAR
SELECT Country,
	   Happiness_Rank,
	   Economy_GDP,
	   Year 
 FROM WorldHappiness
 WHERE Happiness_Rank BETWEEN 130 AND 150



2.	-- COUNTRIES RANKING BETWEEN 1 AND 20 IN ECONOMY(GDP) I.E RANKING THE LEAST 20 ALL YEAR 
SELECT Country,
	   Happiness_Rank,
	   Economy_GDP,
	   Year 
 FROM WorldHappiness
 WHERE Happiness_Rank BETWEEN 1 AND 20



3.	-- COUNTRIES RANKING BETWEEN 130 AND 150 IN Family_SocialSupport I.E RANKING THE TOP 20 ALL YEAR
SELECT Country,
	   Happiness_Rank,
	   Family_SocialSupport,
	   Year 
 FROM WorldHappiness
 WHERE Happiness_Rank BETWEEN 130 AND 150



4.	-- COUNTRIES RANKING BETWEEN 1 AND 20 IN Family_SocialSupport I.E RANKING THE LEAST 20 ALL YEAR
SELECT Country,
	   Happiness_Rank,
	   Family_SocialSupport,
	   Year 
 FROM WorldHappiness
 WHERE Happiness_Rank BETWEEN 1 AND 20



5.	-- COUNTRIES RANKING BETWEEN 130 AND 150 IN Health_LifeExpectancy I.E RANKING THE TOP 20 ALL YEAR
SELECT Country,
	   Happiness_Rank,
	   Health_LifeExpectancy,
	   Year 
 FROM WorldHappiness
 WHERE Happiness_Rank BETWEEN 130 AND 150



6.	  -- COUNTRIES RANKING BETWEEN 1 AND 20 IN Health_LifeExpectancy I.E RANKING THE LEAST 20 ALL YEAR
SELECT Country,
	   Happiness_Rank,
	   Health_LifeExpectancy,
	   Year 
 FROM WorldHappiness
 WHERE Happiness_Rank BETWEEN 1 AND 20



7.	 -- COUNTRIES RANKING BETWEEN 130 AND 150 IN Freedom I.E RANKING THE TOP 20 ALL YEAR
SELECT Country,
	   Happiness_Rank,
	   Freedom,
	   Year 
 FROM WorldHappiness
 WHERE Happiness_Rank BETWEEN 130 AND 150



8.	 -- COUNTRIES RANKING BETWEEN 1 AND 20 IN Freedom I.E RANKING THE LEAST 20 ALL YEAR
SELECT Country,
	   Happiness_Rank,
	  Freedom,
	   Year 
 FROM WorldHappiness
 WHERE Happiness_Rank BETWEEN 1 AND 20



9.	-- COUNTRIES RANKING BETWEEN 130 AND 150 IN Trust_GovtCorruption I.E RANKING THE TOP 20 ALL YEAR
SELECT Country,
	   Happiness_Rank,
	   Trust_Govt_Corruption,
	   Year 
 FROM WorldHappiness
 WHERE Happiness_Rank BETWEEN 130 AND 150



10.	-- COUNTRIES RANKING BETWEEN 1 AND 20 IN Trust_Govt Corruption I.E RANKING THE LEAST 20 ALL YEAR
SELECT Country,
	   Happiness_Rank,
	  Trust_Govt_Corruption,
	   Year 
 FROM WorldHappiness
 WHERE Happiness_Rank BETWEEN 1 AND 20



11.	-- COUNTRIES RANKING BETWEEN 130 AND 150 IN Generosity I.E RANKING THE TOP 20 ALL YEAR
SELECT Country,
	   Happiness_Rank,
	   Generosity,
	   Year 
 FROM WorldHappiness
 WHERE Happiness_Rank BETWEEN 130 AND 150



12.	 -- COUNTRIES RANKING BETWEEN 1 AND 20 IN Generosity I.E RANKING THE LEAST 20 ALL YEAR
SELECT Country,
	   Happiness_Rank,
	  Generosity,
	   Year 
 FROM WorldHappiness
 WHERE Happiness_Rank BETWEEN 1 AND 20



13.	-- COUNTRIES RANKING BETWEEN 130 AND 150 I.E RANKING THE TOP 20 ALL YEAR
SELECT Country,
	   Happiness_Rank,
	   Generosity,
	   Economy_GDP,
	   Family_SocialSupport,
	   Health_LifeExpectancy,
	   Freedom,
	   Trust_Govt_Corruption,
	   Year 
 FROM WorldHappiness
 WHERE Happiness_Rank BETWEEN 130 AND 150



14.	-- COUNTRIES RANKING BETWEEN 1 AND 20 I.E RANKING THE LEAST 20 ALL YEAR
SELECT Country,
	   Happiness_Rank,
	   Generosity,
	   Economy_GDP,
	   Family_SocialSupport,
	   Health_LifeExpectancy,
	   Freedom,
	   Trust_Govt_Corruption,
	   Year 
 FROM WorldHappiness
 WHERE Happiness_Rank BETWEEN 1 AND 20



15.	 -- COUNTRIES WITH hAPPINESS SCORE 7 ABOVE ALL YEAR
select * 
from WorldHappiness
where Happiness_Score BETWEEN 7.0 AND 7.9



16.	 -- COUNTRIES WITH hAPPINESS SCORE LESS THN 1 ALL YEAR
select * 
from WorldHappiness
where Happiness_Score BETWEEN 2.0 AND 3.0



17.	--TOP 20 COUNTRIES RATED HIGH ON HAPPINESS SCORE

SELECT TOP(20) 
       Happiness_Score,
	   Country
FROM WorldHappiness;



 -18. - COUNTRIES in WESTERN EUROPE REGION, YEAR WITH HAPPINESS SCORE less THAN 20 
SELECT Country,
		Year,
		Region,
		Happiness_Rank
FROM WorldHappiness
 WHERE Happiness_Rank <= 20 AND Region = 'Western Europe';


	
19.	-- COUNTRIES in WESTERN EUROPE REGION, YEAR WITH HAPPINESS SCORE greater THAN 70 to 102 
SELECT Country,
		Year,
		Happiness_Rank,
		Region
FROM WorldHappiness
 WHERE Happiness_Rank >= 70 AND Region = 'Western Europe';



20.	 -- COUNTRIES in Middle East and North Africa REGION, YEAR WITH HAPPINESS SCORE less THAN 50 
SELECT Country,
		Year,
		Happiness_Rank,
		Region
FROM WorldHappiness
 WHERE Happiness_Rank <= 50 AND Region = 'Middle East and North Africa';



21.	-- COUNTRIES in Middle East and North Africa REGION, YEAR WITH HAPPINESS SCORE greater THAN 70 to 102 
SELECT Country,
		Year,
		Happiness_Rank,
		Region
FROM WorldHappiness
 WHERE Happiness_Rank >= 20 AND Region = 'Middle East and North Africa';



22.	 -- COUNTRIES in North America and ANZ REGION, YEAR WITH HAPPINESS SCORE less THAN 20 and there no other country that fall above 100 
SELECT Country,
		Year,
		Happiness_Rank,
		Region
FROM WorldHappiness
 WHERE Happiness_Rank <= 20 AND Region = 'North America and ANZ';



23.	 -- COUNTRIES in sub-SAHARAN AFRICA REGION, YEAR WITH HAPPINESS SCORE between 50 t0 100 
SELECT Country,
		Year,
		Happiness_Rank,
		Region
FROM WorldHappiness
 WHERE Happiness_Rank <= 100 AND Region = 'Sub-Saharan Africa';



24.	-- COUNTRIES in Middle East and Northern Africa REGION, YEAR WITH HAPPINESS SCORE < 50  
SELECT Country,
		Year,
		Happiness_Rank,
		Region
FROM WorldHappiness
 WHERE Happiness_Rank <= 50 AND Region = 'Middle East and Northern Africa';



25.	 -- COUNTRIES in Middle East and Northern Africa REGION, YEAR WITH HAPPINESS SCORE > 130 
SELECT Country,
		Year,
		Happiness_Rank,
		Region
FROM WorldHappiness
 WHERE Happiness_Rank >= 130 AND Region = 'Middle East and Northern Africa';


26. -- COUNTRIES in Asia REGIONs, YEAR WITH HAPPINESS SCORE > 130 
SELECT Country,
		Year,
		Happiness_Rank,
		Region
FROM WorldHappiness
 WHERE  Region = 'Southern Asia' or Region = 'Southeast Asia' or Region = 'East Asia' or Region = 'Eastern Asia' or Region = 'South Asia';
 
 
 FULL ANALYSIS AND EXPLANATION IS ON THE POWERPOINT PDF FILE ATTACHED.
 
 THANK YOU FOR STOPPING BY.
