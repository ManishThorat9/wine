# wineThe following table shows the average mean of points and price for various wine-producing countries

	points	price
country		
Argentina	86.754186	25.337971
Armenia	88.000000	15.000000
Australia	87.943163	29.231544
Austria	90.340930	31.862480
Brazil	84.777778	26.031250
Bulgaria	88.018349	15.201835
Canada	89.275676	33.896175
Chile	86.430842	20.740542
Croatia	86.000000	23.928571
Cyprus	86.857143	15.428571
Czech Republic	87.000000	22.750000
England	91.746032	52.677966
France	88.895470	43.861815
Georgia	86.866667	13.600000
Germany	90.012277	43.889015
Greece	86.956044	23.584270
Hungary	88.619048	31.333333
India	89.500000	12.000000
Israel	88.407609	32.719101
Italy	88.971102	46.487805
Lebanon	87.366667	29.966667
Luxembourg	88.500000	23.750000
Macedonia	85.800000	15.200000
Mexico	85.245283	28.433962
Moldova	87.414634	18.414634
Morocco	88.750000	17.650000
New Zealand	88.302621	26.853639
Peru	83.250000	18.416667
Portugal	87.997855	21.564713
Romania	86.130952	16.071429
Serbia	88.250000	31.000000
Slovakia	87.000000	16.000000
Slovenia	88.307692	26.086957
South Africa	88.201900	25.173969
Spain	87.171365	28.140334
Switzerland	87.750000	94.750000
Turkey	88.000000	29.090909
US	88.615964	37.631470
Ukraine	83.833333	9.250000
Uruguay	86.028571	24.600000

This data can be useful in understanding the average quality and price of wines produced in different countries.








 



wine['country'].unique() 

value =28
array(['Italy', 'Portugal', 'US', 'France', 'Germany', 'Argentina', 'Chile', 'Australia', 'Austria', 'South Africa', 'New Zealand', 'Israel', 'Spain', 'Romania', 'Greece', 'Mexico', 'Hungary', 'Slovenia', nan, 'Luxembourg', 'England', 'Uruguay', 'Lebanon', 'Canada', 'Brazil', 'Morocco', 'Czech Republic', 'Bulgaria', 'Cyprus', 'Turkey', 'Moldova', 'Croatia', 'Peru', 'Georgia', 'Ukraine', 'Switzerland', 'Slovakia', 'Serbia', 'India', 'Macedonia', 'Armenia'])
Here are the unique countries for which we have data.

How countries perform and top 15 country’s 

 
user_name	country	review_title	review_description	designation	points	price	province	region_1	region_2	winery	variety	variety_no	clean_text	sentiment
@kerinokeefe	Italy	Nicosia 2013 VulkÃ  Bianco (Etna)	Aromas include tropical fruit, broom, brimston...	VulkÃ  Bianco	87	NaN	Sicily & Sardinia	Etna	NaN	Nicosia	White Blend	0	aromas include tropical fruit broom brimstone ...	positive
@vossroger	Portugal	Quinta dos Avidagos 2011 Avidagos Red (Douro)	This is ripe and fruity, a wine that is smooth...	Avidagos	87	15.0	Douro	NaN	NaN	Quinta dos Avidagos	Portuguese Red	1	ripe fruity wine smooth still structured firm ...	positive
@paulgwineÂ	US	Rainstorm 2013 Pinot Gris (Willamette Valley)	Tart and snappy, the flavors of lime flesh and...	NaN	87	14.0	Oregon	Willamette Valley	Willamette Valley	Rainstorm	Pinot Gris	2	tart snappy flavors lime flesh rind dominate g...	positive
NaN	US	St. Julian 2013 Reserve Late Harvest Riesling ...	Pineapple rind, lemon pith and orange blossom ...	Reserve Late Harvest	87	13.0	Michigan	Lake Michigan Shore	NaN	St. Julian	Riesling	3	pineapple rind lemon pith orange blossom start...	negative
@paulgwineÂ	US	Sweet Cheeks 2012 Vintner's Reserve Wild Child...	Much like the regular bottling from 2012, this...	Vintner's Reserve Wild Child Block	87	65.0	Oregon	Willamette Valley	Willamette Valley	Sweet Cheeks	Pinot Noir	4	much like regular bottling comes across rather...	positive


There are diversity in review data positive , negative and neutral

 
Here we analysis review according to test 
tastes =['Fruity','Earthy','Spicy','Smoky','Flowery','Acidic']
taste_count = []
for taste in tastes:
  num = len(wine[wine['review_description'].str.contains(taste.lower())])
  taste_count.append(num)
print(taste_count)
pd.Series(taste_count, index = tastes).plot(kind='bar')
plt.show()
[6965, 3206, 4824, 3165, 74, 1026]
 
variety_dict = {
    'White Blend':0,
    'Portuguese Red':1,
    'Pinot Gris':2,
    'Riesling':3,
    'Pinot Noir':4,
    'GewÃ¼rztraminer':5,
    'Cabernet Sauvignon':6,
    'Chardonnay':7,
    'Malbec':8,
    'Red Blend':9,
    'Merlot':10,
    'Gamay':11,
    'Sauvignon Blanc':12,
    'Bordeaux-style White Blend' :13,
    'Sangiovese':14,
    'Cabernet Franc':15,
    'Champagne Blend':16,
    'Bordeaux-style Red Blend':17,
    'RosÃ©':18,
    'Zinfandel':19,
    'GrÃ¼ner Veltliner':20,
    'Syrah':21,
    'Nebbiolo':22,
    'RhÃ´ne-style Red Blend':23,
    'Portuguese White':24,
    'Sparkling Blend':25,
    'Pinot Grigio':26,
    'Tempranillo':27

}
 
How variety of wine perform 
Top 5 wine variety are     'Pinot Noir', 'Chardonnay', 'Cabernet Sauvignon', 'Red Blend', 'Bordeaux-style Red Blend'

Here are code github


