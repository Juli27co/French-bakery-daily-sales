# French-bakery-daily-sales
Forecast sales for a French bakery
https://www.kaggle.com/datasets/matthieugimbert/french-bakery-daily-sales?resource=download

About Dataset
Context
The dataset belongs to a French bakery. The dataset provides the daily transaction details of customers from 2021-01-01 to 2022-09-30.
Yearly and weekly saisonalities can be observed.

Content
The dataset has 234005 entries, over 136000 transactions and 6 columns.

Variables
date: date order
time: time order
ticket number: identifier for every single transaction
article: name of the product sold (in French)
quantity: quantity sold
unit_price: price per product
Objective: Forecast the sales in order to ease the production planning

Usability
9.71

License
Data files © Original Authors

# Raw Data

This is the data downloaded from the Kaggle dataset

,date,time,ticket_number,article,Quantity,unit_price
0,2021-01-02,08:38,150040.0,BAGUETTE,1.0,"0,90 â‚¬"
1,2021-01-02,08:38,150040.0,PAIN AU CHOCOLAT,3.0,"1,20 â‚¬"
4,2021-01-02,09:14,150041.0,PAIN AU CHOCOLAT,2.0,"1,20 â‚¬"
5,2021-01-02,09:14,150041.0,PAIN,1.0,"1,15 â‚¬"
8,2021-01-02,09:25,150042.0,TRADITIONAL BAGUETTE,5.0,"1,20 â‚¬"
11,2021-01-02,09:25,150043.0,BAGUETTE,2.0,"0,90 â‚¬"
12,2021-01-02,09:25,150043.0,CROISSANT,3.0,"1,10 â‚¬"
15,2021-01-02,09:27,150044.0,BANETTE,1.0,"1,05 â‚¬"
18,2021-01-02,09:32,150045.0,TRADITIONAL BAGUETTE,3.0,"1,20 â‚¬"
19,2021-01-02,09:32,150045.0,CROISSANT,6.0,"1,10 â‚¬"
22,2021-01-02,09:37,150046.0,PAIN AU CHOCOLAT,6.0,"1,20 â‚¬"
23,2021-01-02,09:37,150046.0,CROISSANT,6.0,"1,10 â‚¬"
24,2021-01-02,09:37,150046.0,TRADITIONAL BAGUETTE,6.0,"1,20 â‚¬"
29,2021-01-02,09:39,150048.0,CROISSANT,3.0,"1,10 â‚¬"
32,2021-01-02,09:40,150049.0,CROISSANT,2.0,"1,10 â‚¬"
33,2021-01-02,09:40,150049.0,TRADITIONAL BAGUETTE,1.0,"1,20 â‚¬"
36,2021-01-02,09:41,150050.0,TRADITIONAL BAGUETTE,2.0,"1,20 â‚¬"
39,2021-01-02,09:46,150051.0,PAIN,1.0,"1,15 â‚¬"
42,2021-01-02,09:48,150052.0,BANETTINE,1.0,"0,60 â‚¬"
43,2021-01-02,09:48,150052.0,SPECIAL BREAD,1.0,"2,40 â‚¬"
(...)

![image](https://user-images.githubusercontent.com/123991185/232857285-b5951742-9f48-43c3-b442-991eb28dbe72.png)

# Procesed Data

The data was processed with the help of power query, conditional columns and logical calculations were added to generate more information to analyze. Likewise, negative data and errors were cleaned

Ticket_number	Store	Employed	Date	Time	Article	NormalizedQuantity	Unit_price	NormalizedTotalSale	LogicalStore	LogicalEmployed	LogicalRedonEmployed
1501400	Mallorca	Carlos	2/01/2021	12:12:00 p. m.	CAMPAGNE	10	1,8	18	VERDADERO	2,148841968	2
1501400	Valencia	Luisa	2/01/2021	12:12:00 p. m.	TRADITIONAL BAGUETTE	10	1,2	12	FALSO	1,559884483	1
1501410	Valencia	Luisa	2/01/2021	12:12:00 p. m.	BAGUETTE	10	0,9	9	FALSO	1,443017105	1
1501430	Valencia	Roberto	2/01/2021	12:13:00 p. m.	GRAND FAR BRETON	10	7	70	FALSO	4,372014418	4
1501420	Mallorca	Luisa	2/01/2021	12:13:00 p. m.	BAGUETTE	10	0,9	9	VERDADERO	1,797743302	1
1501380	Mallorca	Luisa	2/01/2021	12:10:00 p. m.	GAL FRANGIPANE 4P	10	8	80	VERDADERO	1,606134448	1
1501340	Valencia	Carlos	2/01/2021	12:03:00 p. m.	BANETTE	10	1,05	10,5	FALSO	2,002463731	2
1501380	Valencia	Roberto	2/01/2021	12:10:00 p. m.	TRADITIONAL BAGUETTE	10	1,2	12	FALSO	4,744847858	4
1501400	Mallorca	Carlos	2/01/2021	12:12:00 p. m.	COUPE	10	0,15	1,5	VERDADERO	2,743994142	2
1501390	Valencia	Roberto	2/01/2021	12:11:00 p. m.	GRAND FAR BRETON	10	7	70	FALSO	4,630947733	4
1501440	Mallorca	Roberto	2/01/2021	12:15:00 p. m.	SPECIAL BREAD	10	2,4	24	VERDADERO	4,40102797	4
1501530	Valencia	Luisa	2/01/2021	12:22:00 p. m.	COMPLET	10	1,5	15	FALSO	1,581504077	1
1501500	Mallorca	Gabriela	2/01/2021	12:21:00 p. m.	BAGUETTE	10	0,9	9	VERDADERO	3,937032282	3
1501530	Mallorca	Carlos	2/01/2021	12:22:00 p. m.	COUPE	10	0,15	1,5	VERDADERO	2,880331653	2
1501540	Mallorca	Gabriela	2/01/2021	12:23:00 p. m.	TRADITIONAL BAGUETTE	10	1,2	12	VERDADERO	3,741995373	3
1501540	Valencia	Gabriela	2/01/2021	12:23:00 p. m.	COMPLET	10	1,5	15	FALSO	3,684164183	3
1501460	Valencia	Roberto	2/01/2021	12:18:00 p. m.	COUPE	10	0,15	1,5	FALSO	4,969319113	4
1501440	Valencia	Carlos	2/01/2021	12:15:00 p. m.	COUPE	10	0,15	1,5	FALSO	2,924869179	2
1501460	Mallorca	Carlos	2/01/2021	12:18:00 p. m.	BOULE 400G	10	1,5	15	VERDADERO	2,381752877	2
1501490	Valencia	Roberto	2/01/2021	12:21:00 p. m.	TRADITIONAL BAGUETTE	10	1,2	12	FALSO	4,240305138	4
1501480	Valencia	Gabriela	2/01/2021	12:20:00 p. m.	TRADITIONAL BAGUETTE	10	1,2	12	FALSO	3,661517113	3
1501220	Mallorca	Luisa	2/01/2021	11:50:00 a. m.	VIK BREAD	10	2,5	25	VERDADERO	1,353534922	1
1501190	Valencia	Carlos	2/01/2021	11:48:00 a. m.	GAL POMME 4P	10	8	80	FALSO	2,604091902	2
1501220	Valencia	Carlos	2/01/2021	11:50:00 a. m.	GACHE	10	5	50	FALSO	2,626259447	2
1501220	Valencia	Roberto	2/01/2021	11:50:00 a. m.	SEIGLE	10	1,8	18	FALSO	4,189362131	4
(...)

![image](https://user-images.githubusercontent.com/123991185/232857005-e345c8b8-a402-4604-b160-97a74053fb14.png)

# Exploratory Data Analyst (EDA)

Development of exploratory data analysis with dynamic tables, conditional formats and time scale segmenters

![image](https://user-images.githubusercontent.com/123991185/232857621-525c49aa-8741-4623-a5b7-25ae98047326.png)

![image](https://user-images.githubusercontent.com/123991185/232857670-f89298b6-8749-45bc-ba3f-e987756c89fb.png)

![image](https://user-images.githubusercontent.com/123991185/232857735-83d2ba00-3553-41b6-a501-ae9e7b03f5c5.png)

![image](https://user-images.githubusercontent.com/123991185/232857920-84623700-4bb1-442b-a540-77645373af2f.png)

# Sales Report

Development of data visualization and recommendations with the data found (business intelligence)

![image](https://user-images.githubusercontent.com/123991185/232858058-f6052001-33ed-4f46-87e5-a05a93699b96.png)

![image](https://user-images.githubusercontent.com/123991185/232858111-a463e84a-bbbd-4f36-a503-f6b2b481ea23.png)

![image](https://user-images.githubusercontent.com/123991185/232858168-e7c40ed5-b044-4507-92d2-f4cf0dfcfc23.png)




