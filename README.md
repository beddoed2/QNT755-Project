# QNT755-Project
import pandas as pd

df = pd.read_csv (r'C:\\Users\mbrog\Documents\QNT755\Project\NHANES.csv')
print (df)

     SurveyYr     ID  Gender  Age AgeDecade  AgeMonths    Race1    Race3  \
0     2009_10  55829  female   28     20-29      343.0    White      NaN   
1     2009_10  57112    male   14     10-19      170.0    White      NaN   
2     2009_10  60232    male   80       NaN        NaN    White      NaN   
3     2009_10  59919    male   22     20-29      268.0    White      NaN   
4     2009_10  56351    male    1       0-9       16.0    White      NaN   
...       ...    ...     ...  ...       ...        ...      ...      ...   
9995  2011_12  64065    male   46     40-49        NaN    White    White   
9996  2011_12  66189    male   47     40-49        NaN  Mexican  Mexican   
9997  2011_12  63714    male   48     40-49        NaN    White    White   
9998  2011_12  68501    male   52     50-59        NaN    White    White   
9999  2011_12  62881  female   57     50-59        NaN    White    White   

        Education MaritalStatus  ... AgeFirstMarij  RegularMarij  AgeRegMarij  \
0     CollegeGrad       Married  ...          15.0            No          NaN   
1             NaN           NaN  ...           NaN           NaN          NaN   
2        8thGrade       Married  ...           NaN           NaN          NaN   
3      HighSchool  NeverMarried  ...          10.0           Yes         10.0   
4             NaN           NaN  ...           NaN           NaN          NaN   
...           ...           ...  ...           ...           ...          ...   
9995  SomeCollege       Married  ...           NaN            No          NaN   
9996  9_11thGrade       Married  ...          15.0           Yes         20.0   
9997  SomeCollege       Married  ...          16.0            No          NaN   
9998  SomeCollege       Married  ...          16.0           Yes         16.0   
9999  CollegeGrad       Married  ...           NaN           NaN          NaN   

      HardDrugs SexEver SexAge  SexNumPartnLife  SexNumPartYear  SameSex  \
0           Yes     Yes   13.0             20.0             1.0       No   
1           NaN     NaN    NaN              NaN             NaN      NaN   
2           NaN     NaN    NaN              NaN             NaN      NaN   
3           Yes     Yes   18.0              3.0             1.0       No   
4           NaN     NaN    NaN              NaN             NaN      NaN   
...         ...     ...    ...              ...             ...      ...   
9995         No     Yes   17.0              7.0             1.0       No   
9996         No     Yes   18.0              7.0             1.0       No   
9997         No     Yes   17.0              4.0             1.0       No   
9998        Yes     Yes   16.0             50.0             1.0       No   
9999        NaN     NaN    NaN              NaN             NaN      NaN   

      SexOrientation  
0       Heterosexual  
1                NaN  
2                NaN  
3       Heterosexual  
4                NaN  
...              ...  
9995    Heterosexual  
9996    Heterosexual  
9997    Heterosexual  
9998    Heterosexual  
9999             NaN  

[10000 rows x 75 columns]

df.describe()
	ID	Age	AgeMonths	HHIncomeMid	Poverty	HomeRooms	Weight	Length	HeadCirc	Height	...	TVHrsDayChild	CompHrsDayChild	AlcoholDay	AlcoholYear	SmokeAge	AgeFirstMarij	AgeRegMarij	SexAge	SexNumPartnLife	SexNumPartYear
count	10000.00000	10000.000000	4962.000000	9189.000000	9274.000000	9931.000000	9922.000000	543.000000	88.000000	9647.000000	...	653.000000	653.000000	4914.000000	5922.000000	3080.000000	2891.000000	1366.000000	5540.000000	5725.000000	4928.000000
mean	61944.64380	36.742100	420.123942	57206.170421	2.801844	6.248918	70.981798	85.016022	41.180682	161.877838	...	1.938744	2.197550	2.914123	75.101655	17.826623	17.022829	17.691069	17.428700	15.085066	1.342330
std	5871.16716	22.397566	259.043091	33020.276584	1.677909	2.277538	29.125357	13.705026	2.311483	20.186567	...	1.434431	2.516667	3.182672	103.033738	5.326660	3.895010	4.806103	3.716551	57.846434	2.782688
min	51624.00000	0.000000	0.000000	2500.000000	0.000000	1.000000	2.800000	47.100000	34.200000	83.600000	...	0.000000	0.000000	1.000000	0.000000	6.000000	1.000000	5.000000	9.000000	0.000000	0.000000
25%	56904.50000	17.000000	199.000000	30000.000000	1.240000	5.000000	56.100000	75.700000	39.575000	156.800000	...	1.000000	0.000000	1.000000	3.000000	15.000000	15.000000	15.000000	15.000000	2.000000	1.000000
50%	62159.50000	36.000000	418.000000	50000.000000	2.700000	6.000000	72.700000	87.000000	41.450000	166.000000	...	2.000000	1.000000	2.000000	24.000000	17.000000	16.000000	17.000000	17.000000	5.000000	1.000000
75%	67039.00000	54.000000	624.000000	87500.000000	4.710000	8.000000	88.900000	96.100000	42.925000	174.500000	...	3.000000	6.000000	3.000000	104.000000	19.000000	19.000000	19.000000	19.000000	12.000000	1.000000
max	71915.00000	80.000000	959.000000	100000.000000	5.000000	13.000000	230.700000	112.200000	45.400000	200.400000	...	6.000000	6.000000	82.000000	364.000000	72.000000	48.000000	52.000000	50.000000	2000.000000	69.000000
8 rows × 45 columns

df.head(10)

	SurveyYr	ID	Gender	Age	AgeDecade	AgeMonths	Race1	Race3	Education	MaritalStatus	...	AgeFirstMarij	RegularMarij	AgeRegMarij	HardDrugs	SexEver	SexAge	SexNumPartnLife	SexNumPartYear	SameSex	SexOrientation
0	2009_10	55829	female	28	20-29	343.0	White	NaN	CollegeGrad	Married	...	15.0	No	NaN	Yes	Yes	13.0	20.0	1.0	No	Heterosexual
1	2009_10	57112	male	14	10-19	170.0	White	NaN	NaN	NaN	...	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN
2	2009_10	60232	male	80	NaN	NaN	White	NaN	8thGrade	Married	...	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN
3	2009_10	59919	male	22	20-29	268.0	White	NaN	HighSchool	NeverMarried	...	10.0	Yes	10.0	Yes	Yes	18.0	3.0	1.0	No	Heterosexual
4	2009_10	56351	male	1	0-9	16.0	White	NaN	NaN	NaN	...	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN
5	2009_10	56329	female	39	30-39	477.0	White	NaN	8thGrade	Married	...	15.0	Yes	23.0	No	Yes	15.0	15.0	1.0	No	Heterosexual
6	2009_10	57197	male	18	10-19	223.0	White	NaN	NaN	NaN	...	NaN	No	NaN	No	No	NaN	0.0	0.0	No	Heterosexual
7	2009_10	52795	male	61	60-69	740.0	Other	NaN	SomeCollege	Married	...	NaN	NaN	NaN	No	Yes	13.0	3.0	NaN	No	NaN
8	2009_10	52719	female	73	70+	883.0	White	NaN	CollegeGrad	Married	...	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN
9	2009_10	61770	male	40	40-49	485.0	Mexican	NaN	8thGrade	Married	...	NaN	No	NaN	No	Yes	14.0	5.0	1.0	No	Heterosexual
10 rows × 75 columns
