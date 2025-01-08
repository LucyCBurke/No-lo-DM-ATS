# No-lo-DM-ATS
Repo containing open access R script for regression paper exploring relationships between drinking motives and no/lo consumption

# Coding workbook

# Datafiles
	
Feb23	imported ATS data for Feb 23
Apr23	imported ATS data for Apr 23
Feb23_study1var	Feb23 datafile with only variables of interest retained
Apr23_study1var	Apr23 datafile with only variables of interest retained
Feb23_drinkers	Subset sample for those who scored => 1 in AUDIT (i.e. had had an alcoholic drink in the last 12 months)
Apr23_drinkers	Subset sample for those who scored => 1 in AUDIT (i.e. had had an alcoholic drink in the last 12 months)
Data_alpha_audit	This is the merged Feb and April datafiles including non-drinkers in order to calculate an alpha score for AUDIT-C
Study1data	Merged Feb and April datafiles including respondents who drink alcohol
Study1dataC	Dataset that has removed participants who responded inconsistently to the NoLo frequency items
Data_for_impute	This dropped cases where:
- a participant had responded ‘Don’t know’ to any of the drinking motive items (coded as NA). There were no actual missing data for these variables. 
- a participant had identified their sex as ‘In another way”
MIA_data	This is the dataset which includes imputed values for missing cases on sg4R, imd_quintile, sex and ft_emp.
Clean_data	This is the Data_for_impute uploaded and renamed and used for descriptives and tests when don’t need to pool the results as working with data that doesn’t have any imputes 

# Study variables taken from the ATS datasets
	Label	Response options
sexz	Sex	
agez	Age	
actage	ACTUAL AGE	
sgz	Social Grade (5 level ordinal variable)	1 = AB
2 = C1
3 = C2
4 = D
5 = E
tenure	TENURE	BEING BOUGHT ON A MORTGAGE OWNED OUTRIGHT BY HOUSEHOLD
RENTED FROM LOCAL AUTHORITY
RENTED FROM A PRIVATE LANDLORD                                                             BELONGS TO HOUSING ASSOCIATION 
OTHER                                                       REFUSED
gor	Government Office Region (11 categories)	
ethnic	ETHNIC ORIGIN - NETS	
dethnin	ETHNIC ORIGIN – binary variable whether respondent white or not.	White Yes/ No
qual	EDUCATION	
work	Working status respondent	HAVE PAID JOB - FULL TIME (30+ HOURS PER WEEK)") 
HAVE PAID JOB - PART TIME (8-29 HOURS PER WEEK)
HAVE PAID JOB - PART TIME (UNDER 8 HOURS PER WEEK)
SELF-EMPLOYED 
FULL TIME STUDENT
STILL AT SCHOOL,
UNEMPLOYED AND SEEKING WORK
NOT IN PAID WORK FOR OTHER REASON
NOT IN PAID WORK BECAUSE OF LONG TERM ILLNESS OR DISABILITY
NOT WORKING - HOUSEWIFE,
RETIRED
urban	URBAN/RURAL	
audit1	AUDIT1 - How often do you have a drink containing alcohol?	
audit2	AUDIT2 - How many standard drinks containing alcohol do you have on a typical day when you are drinking?	
audit3	AUDIT3 - How often do you have six or more standard drinks on one occasion?	
nla1	NLA1 - How often do you have an alcohol-free or low alcohol drink, that is, beer, wine, cider, spirit or other type of alcoholic drink under 1.2% ABV?	Never, Once or twice a year, Once every couple of months,                                       Once or twice a month, Once or twice a week,                                                                         Three or four days a week, Five or six days a week,                                                                   Almost every day
nla2	NLA2 - How often do you have an alcohol-free or low alcohol drink (under 1.2% ABV) during the same occasion that you also drink standard alcoholic drinks?	Never, Once or twice a year, Once every couple of months,                                       Once or twice a month, Once or twice a week,                                                                         Three or four days a week, Five or six days a week,                                                                   Almost every day
nla3	NLA3 - How often do you have an alcohol-free or low alcohol drink (under 1.2% ABV) in a pub, club, bar or restaurant?	Never, Once or twice a year, Once every couple of months,                                       Once or twice a month, Once or twice a week,                                                                         Three or four days a week, Five or six days a week,                                                                   Almost every day
nla4	NLA4 - How often do you have an alcohol-free or low alcohol drink (under 1.2% ABV) whilst drinking at your home or someone else's home?	
NAQ1 - I am going to read a list of reasons people sometimes give for drinking alcohol.
naq1_01	Because it gives you a pleasant feeling- ENHANCEMENT	6 level factor
1 = Never/ Almost never
2 = Sometimes
3 = Half the time
4 = Often
5 = Always/nearly always
6 = Don’t know
naq1_02	Because it makes social gatherings more fun – SOCIAL	6 level factor
1 = Never/ Almost never
2 = Sometimes
3 = Half the time
4 = Often
5 = Always/nearly always
6 = Don’t know
naq1_03	To fit in with a group that you like – CONFORMITY	6 level factor
1 = Never/ Almost never
2 = Sometimes
3 = Half the time
4 = Often
5 = Always/nearly always
6 = Don’t know6 level factor
1 = Never/ Almost never
2 = Sometimes
3 = Half the time
4 = Often
5 = Always/nearly always
6 = Don’t know
naq1_04	To forget about your problems – COPING DEP	6 level factor
1 = Never/ Almost never
2 = Sometimes
3 = Half the time
4 = Often
5 = Always/nearly always
6 = Don’t know
naq1_05	Because you feel more self-confident and sure of yourself – COPING - ANX	6 level factor
1 = Never/ Almost never
2 = Sometimes
3 = Half the time
4 = Often
5 = Always/nearly always
6 = Don’t know
imd_quintile	IMD quintile	
X.weight0	England weights	
weight_sy	SY weight	
weight_gb	GB weight	
weight_wales	Wales weight	
weight_scotland	Scotland weight	

# Variables created 
		
audit_class	Classification of total AUDIT-C score into risk category	1 = 1-4 (low risk)
2 = 5-7 (increasing risk)
3 = 8-10 (higher risk)
4 = 11-12 (possible dependence)
nolo_monthly	The 8 responses from nla1 were collapsed into a binary variable describing whether participant drinks nolo at least monthly or less than monthly	0 = less than monthly
1 = at least monthly
nolo_ontrade	The 8 responses from nla3 were collapsed into a binary variable describing whether participant drinks nolo on-trade at least monthly or less than monthly	0 = less than monthly
1 = at least monthly
nolo_offtrade	The 8 responses from nla3 were collapsed into a binary variable describing whether participant drinks nolo off-trade at least monthly or less than monthly	0 = less than monthly
1 = at least monthly
sg4	4 level social grade variable collapsing categories D and E	1 = AB
2 = C1
3 = C2
4 = DE
sg4R	Reverse code sg4 so that a higher score is associated with a higher social grade	1 = DE
2 = C2
3 = C1
4 = AB
ed4	4 level social grade variable collapsing the original qual responses	1= GCSE/O-LEVEL/CSE, VOCATIONAL QUALIFICATIONS (=NVQ1+2), NO FORMAL QUALIFICATIONS
2 = A-LEVEL OR EQUIVALENT (=NVQ3), OTHER, DON'T KNOW, STILL STUDYING
3 = BACHELOR DEGREE OR EQUIVALENT (=NVQ4)
4 = MASTERS/PHD OR EQUIVALENT

Other, don’t know and still studying were placed in category 2 based on these respondents characteristics (age, social grade, sex, and audit)
Didn’t want to separate into a separate group as then would be difficult to use variable as an ordinal scale and they are not really distinct. 
home_owner	Binary variable created from tenure responses	1 = BEING BOUGHT ON A MORTGAGE, OWNED OUTRIGHT BY HOUSEHOLD 
2 = RENTED FROM LOCAL AUTHORITY, RENTED FROM A PRIVATE LANDLORD,                                                             BELONGS TO HOUSING ASSOCIATION, OTHER,                                                        REFUSED
emp	6 level factor capturing responses from the work variable	1 = HAVE PAID JOB - FULL TIME (30+ HOURS PER WEEK)") 
2 = HAVE PAID JOB - PART TIME (8-29 HOURS PER WEEK), HAVE PAID JOB - PART TIME (UNDER 8 HOURS PER WEEK),
3 = SELF-EMPLOYED) 
4 = FULL TIME STUDENT, STILL AT SCHOOL,
5 = UNEMPLOYED AND SEEKING WORK, NOT IN PAID WORK FOR OTHER REASON, NOT IN PAID WORK BECAUSE OF LONG TERM ILLNESS OR DISABILITY, NOT WORKING - HOUSEWIFE,
6 = RETIRED
ft_emp	Binary variables describing whether participant works FT or not	1 = FT EMPLOYEE
0 = ALL OTHER RESPONSES (although a bit tricky as self-employed in here which could be FT)
region	Collapsed the 11 gor responses into 6, but not sure whether to use this variable or stick with gor. 	1 = LONDON, SOUTH EAST, "EASTERN,
2 = NORTH EAST, NORTH WEST, YORKS AND HUMBR,
3 = SOUTH WEST
4 = EAST MIDLANDS, WEST MIDLANDS,
5= SCOTLAND,
6 = WALES
enh5L	Created from naq1_01 – change value 6 to NA	5 level factor
1 = Never/ Almost never
2 = Sometimes
3 = Half the time
4 = Often
5 = Always/nearly always

soc5L	Created from naq1_02 – change value 6 to NA	5 level factor
1 = Never/ Almost never
2 = Sometimes
3 = Half the time
4 = Often
5 = Always/nearly always

con5L	Created from naq1_03 – change value 6 to NA	5 level factor
1 = Never/ Almost never
2 = Sometimes
3 = Half the time
4 = Often
5 = Always/nearly always

dep5L	Created from naq1_04 – change value 6 to NA	5 level factor
1 = Never/ Almost never
2 = Sometimes
3 = Half the time
4 = Often
5 = Always/nearly always

anx5L	Created from naq1_05 – change value 6 to NA	5 level factor
1 = Never/ Almost never
2 = Sometimes
3 = Half the time
4 = Often
5 = Always/nearly always

enhBIN	Variable recoded as binary variable with low and high endorsers 1-2 low, 3-5 high	0 = low (less than half the time)
1 = high (at least half the time)
socBIN	Variable recoded as binary variable with low and high endorsers 1-2 low, 3-5 high	0 = low (less than half the time)
1 = high (at least half the time)
conBIN	Variable recoded as binary variable with low and high endorsers 1-2 low, 3-5 high	0 = low (less than half the time)
1 = high (at least half the time)
depBIN	Variable recoded as binary variable with low and high endorsers 1-2 low, 3-5 high	0 = low (less than half the time)
1 = high (at least half the time)
anxBIN	Variable recoded as binary variable with low and high endorsers 1-2 low, 3-5 high	0 = low (less than half the time)
1 = high (at least half the time)
		


