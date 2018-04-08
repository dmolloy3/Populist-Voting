Identifying Populist Parties
================
Declan Molloy

There are two main datasets that attempt to classify parties around the world on various metrics, the Chapel Hill Expert Survey (CHES) and the Manifesto Project (previously known as the Comparative Manifesto Project). Neither explicitly code for populism, and so the challenge is to figure out a way to use the variables they do measure to try and come up with a systematic way to classify a party as populist or not.

Chapel Hill Expert Survey
-------------------------

To begin with, we'll look at the CHES dataset, which has asked country experts to rate various parties on different metrics. Inglehart and Norris have found that 13 variables from CHES neatly correspond to two separate cleavages: four can be reduced to an economic cleavage and nine can be reduced to a cultural cleavage. The variables summed to create the populism factor have been chosen to closely reflect ideological leanings associated with right wing populism. The results for every party is plotted below on both economic and populist scales, with parties classified as populist coloured in red, corresponding to higher cultural cleavage scores.

<img src="Party_Graphs_files/figure-markdown_github/CHES-party-positions-1.png" width="100%" style="display: block; margin: auto;" />

Manifesto Project
-----------------

A second large scale source of data on parties is the Manifesto Project which, as the name suggests, examines the electoral manifestos and other related materials of parties, coding based on how often certain topics are mentioned. Again, parties are plotted on an economic and populist scale. Parties have also been coloured according to whether they were previously classified as populist in the CHES dataset. As parties take a much smaller range of values and are thus more tightly clustered using the Manifesto project variables, it was not possible to label all of them. In order to highlight the differences in outcomes between the CHES and Manifesto Project results, political parties have been labelled that were classed as populist by the CHES data but scored lowly on the populist scale using the Manifesto Project data, as well as parties that scored highly but were not classified as populist by CHES.

<img src="Party_Graphs_files/figure-markdown_github/cmp-parties-1.png" width="100%" style="display: block; margin: auto;" />

To further compare and contrast both datasets and methods, the Manifesto Project populist scores have been rescaled to a 0-100 scale, then each party plotted by their populist scores from the CHES data against the scores from the Manifesto data. Also included is a simple linear regression showing the relationship between the two scores, with some of the parties that have the highest absolute residuals from this linear regression labelled.

<img src="Party_Graphs_files/figure-markdown_github/compare-1.png" width="100%" style="display: block; margin: auto;" />

Finally, I've plotted the residuals themselves, with the same parties labelled. Parties above 0 means a party's CHES populism score is higher (more populist) than expected given its score from the Manifesto Project.

<img src="Party_Graphs_files/figure-markdown_github/resid-compare-1.png" width="100%" style="display: block; margin: auto;" />

Which to use?
-------------

Looking at these comparisons, it becomes clear that the Manifesto Project populism score is worse at identifying populist radical right parties than the CHES score. The plot of its party classifications shows several widely accepted populist parties, including *Ataka* in Bulgaria, *AfD* in Germany and *Lega Nord* in Italy, with populist scores close to the mean of all parties. This difference is even more stark in when we look at the residuals, where we can see that the parties rated higher by CHES include other populist parties, such as *Jobbik* in Hungary and the *People's Party – Dan Diaconescu* in Romania. Parties that are rated as higher by the Manifesto Project metric include more left-leaning parties, such as the *Left Bloc* in Portugal and the *Green Party* in Sweden. Given this project is focused on radical right populist parties, I use the CHES data to classify populist parties. See below for a full table.

<table>
<caption>
Classification of Parties
</caption>
<thead>
<tr>
<th style="text-align:left;">
Country
</th>
<th style="text-align:right;">
CHES Wave
</th>
<th style="text-align:left;">
Party Abbreviation
</th>
<th style="text-align:left;">
Party Name in English
</th>
<th style="text-align:right;">
Election Year
</th>
<th style="text-align:right;">
Vote Share
</th>
<th style="text-align:right;">
Economic Scale
</th>
<th style="text-align:right;">
Populism Scale
</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left;">
Austria
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
FPO
</td>
<td style="text-align:left;">
Freedom Party of Austria
</td>
<td style="text-align:right;">
2013
</td>
<td style="text-align:right;">
20.50
</td>
<td style="text-align:right;">
50.97
</td>
<td style="text-align:right;">
83.75
</td>
</tr>
<tr>
<td style="text-align:left;">
Belgium
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
VB
</td>
<td style="text-align:left;">
Flemish Block
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:right;">
3.70
</td>
<td style="text-align:right;">
52.12
</td>
<td style="text-align:right;">
81.33
</td>
</tr>
<tr>
<td style="text-align:left;">
Belgium
</td>
<td style="text-align:right;">
2010
</td>
<td style="text-align:left;">
FN
</td>
<td style="text-align:left;">
National Front
</td>
<td style="text-align:right;">
2010
</td>
<td style="text-align:right;">
0.51
</td>
<td style="text-align:right;">
75.06
</td>
<td style="text-align:right;">
83.65
</td>
</tr>
<tr>
<td style="text-align:left;">
Bulgaria
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
VMRO-BND
</td>
<td style="text-align:left;">
Bulgarian National Movement
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:right;">
3.10
</td>
<td style="text-align:right;">
31.03
</td>
<td style="text-align:right;">
84.52
</td>
</tr>
<tr>
<td style="text-align:left;">
Bulgaria
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
ATAKA
</td>
<td style="text-align:left;">
Attack
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:right;">
4.50
</td>
<td style="text-align:right;">
13.35
</td>
<td style="text-align:right;">
90.33
</td>
</tr>
<tr>
<td style="text-align:left;">
Bulgaria
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
NFSB
</td>
<td style="text-align:left;">
National Front for the Salvation of Bulgaria
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:right;">
4.20
</td>
<td style="text-align:right;">
34.73
</td>
<td style="text-align:right;">
81.41
</td>
</tr>
<tr>
<td style="text-align:left;">
Bulgaria
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
BBT
</td>
<td style="text-align:left;">
Bulgaria without Censorship
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:right;">
5.70
</td>
<td style="text-align:right;">
35.32
</td>
<td style="text-align:right;">
75.78
</td>
</tr>
<tr>
<td style="text-align:left;">
Croatia
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
HDZ
</td>
<td style="text-align:left;">
Croatian Democratic Union
</td>
<td style="text-align:right;">
2011
</td>
<td style="text-align:right;">
21.90
</td>
<td style="text-align:right;">
59.58
</td>
<td style="text-align:right;">
75.79
</td>
</tr>
<tr>
<td style="text-align:left;">
Croatia
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
HSS
</td>
<td style="text-align:left;">
Croatian Peasant Party
</td>
<td style="text-align:right;">
2011
</td>
<td style="text-align:right;">
0.60
</td>
<td style="text-align:right;">
42.19
</td>
<td style="text-align:right;">
84.01
</td>
</tr>
<tr>
<td style="text-align:left;">
Croatia
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
HDSSB
</td>
<td style="text-align:left;">
Croatian Democratic Alliance of Slavonia and Baranja
</td>
<td style="text-align:right;">
2011
</td>
<td style="text-align:right;">
3.00
</td>
<td style="text-align:right;">
44.36
</td>
<td style="text-align:right;">
82.51
</td>
</tr>
<tr>
<td style="text-align:left;">
Croatia
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
HSP
</td>
<td style="text-align:left;">
Croatian Party of Rights
</td>
<td style="text-align:right;">
2011
</td>
<td style="text-align:right;">
3.00
</td>
<td style="text-align:right;">
47.12
</td>
<td style="text-align:right;">
89.02
</td>
</tr>
<tr>
<td style="text-align:left;">
Croatia
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
HSP-AS
</td>
<td style="text-align:left;">
Croatian Party of Rights – Dr. Ante Starcevic
</td>
<td style="text-align:right;">
2011
</td>
<td style="text-align:right;">
0.60
</td>
<td style="text-align:right;">
51.13
</td>
<td style="text-align:right;">
87.49
</td>
</tr>
<tr>
<td style="text-align:left;">
Czech Republic
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
USVIT
</td>
<td style="text-align:left;">
Tomio Okamura's Dawn of Direct Democracy
</td>
<td style="text-align:right;">
2013
</td>
<td style="text-align:right;">
6.90
</td>
<td style="text-align:right;">
44.82
</td>
<td style="text-align:right;">
79.99
</td>
</tr>
<tr>
<td style="text-align:left;">
Denmark
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
DF
</td>
<td style="text-align:left;">
Danish Peoples Party
</td>
<td style="text-align:right;">
2011
</td>
<td style="text-align:right;">
12.20
</td>
<td style="text-align:right;">
41.81
</td>
<td style="text-align:right;">
78.67
</td>
</tr>
<tr>
<td style="text-align:left;">
Finland
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
PS
</td>
<td style="text-align:left;">
Finnish Party | True Finns
</td>
<td style="text-align:right;">
2011
</td>
<td style="text-align:right;">
19.10
</td>
<td style="text-align:right;">
38.26
</td>
<td style="text-align:right;">
84.57
</td>
</tr>
<tr>
<td style="text-align:left;">
France
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
FN
</td>
<td style="text-align:left;">
National Front
</td>
<td style="text-align:right;">
2012
</td>
<td style="text-align:right;">
13.60
</td>
<td style="text-align:right;">
44.89
</td>
<td style="text-align:right;">
83.16
</td>
</tr>
<tr>
<td style="text-align:left;">
France
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
MPF
</td>
<td style="text-align:left;">
Movement for France
</td>
<td style="text-align:right;">
2012
</td>
<td style="text-align:right;">
0.23
</td>
<td style="text-align:right;">
63.96
</td>
<td style="text-align:right;">
86.84
</td>
</tr>
<tr>
<td style="text-align:left;">
Germany
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
NPD
</td>
<td style="text-align:left;">
German People's Union
</td>
<td style="text-align:right;">
2013
</td>
<td style="text-align:right;">
1.30
</td>
<td style="text-align:right;">
42.33
</td>
<td style="text-align:right;">
89.12
</td>
</tr>
<tr>
<td style="text-align:left;">
Germany
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
AfD
</td>
<td style="text-align:left;">
Alternative for Germany
</td>
<td style="text-align:right;">
2013
</td>
<td style="text-align:right;">
4.70
</td>
<td style="text-align:right;">
77.27
</td>
<td style="text-align:right;">
81.77
</td>
</tr>
<tr>
<td style="text-align:left;">
Greece
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
ND
</td>
<td style="text-align:left;">
New Democracy
</td>
<td style="text-align:right;">
2012
</td>
<td style="text-align:right;">
29.70
</td>
<td style="text-align:right;">
60.97
</td>
<td style="text-align:right;">
76.17
</td>
</tr>
<tr>
<td style="text-align:left;">
Greece
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
LAOS
</td>
<td style="text-align:left;">
Popular Orthodox Rally
</td>
<td style="text-align:right;">
2012
</td>
<td style="text-align:right;">
1.60
</td>
<td style="text-align:right;">
49.46
</td>
<td style="text-align:right;">
87.30
</td>
</tr>
<tr>
<td style="text-align:left;">
Greece
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
ANEL
</td>
<td style="text-align:left;">
Independent Greeks
</td>
<td style="text-align:right;">
2012
</td>
<td style="text-align:right;">
7.50
</td>
<td style="text-align:right;">
41.92
</td>
<td style="text-align:right;">
88.51
</td>
</tr>
<tr>
<td style="text-align:left;">
Greece
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
XA
</td>
<td style="text-align:left;">
Golden Dawn
</td>
<td style="text-align:right;">
2012
</td>
<td style="text-align:right;">
6.90
</td>
<td style="text-align:right;">
17.50
</td>
<td style="text-align:right;">
93.46
</td>
</tr>
<tr>
<td style="text-align:left;">
Hungary
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
Fidesz
</td>
<td style="text-align:left;">
Fidesz -- Hungarian Civic Party / Christian Democratic People's Party
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:right;">
39.50
</td>
<td style="text-align:right;">
43.66
</td>
<td style="text-align:right;">
81.85
</td>
</tr>
<tr>
<td style="text-align:left;">
Hungary
</td>
<td style="text-align:right;">
2010
</td>
<td style="text-align:left;">
KDNP
</td>
<td style="text-align:left;">
Christian Democratic People's Party
</td>
<td style="text-align:right;">
2010
</td>
<td style="text-align:right;">
7.32
</td>
<td style="text-align:right;">
47.41
</td>
<td style="text-align:right;">
77.02
</td>
</tr>
<tr>
<td style="text-align:left;">
Hungary
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
JOBBIK
</td>
<td style="text-align:left;">
Jobbik Movement for a Better Hungary
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:right;">
20.20
</td>
<td style="text-align:right;">
29.43
</td>
<td style="text-align:right;">
92.33
</td>
</tr>
<tr>
<td style="text-align:left;">
Italy
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
LN
</td>
<td style="text-align:left;">
North League
</td>
<td style="text-align:right;">
2013
</td>
<td style="text-align:right;">
4.10
</td>
<td style="text-align:right;">
61.50
</td>
<td style="text-align:right;">
83.16
</td>
</tr>
<tr>
<td style="text-align:left;">
Italy
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
Fdl
</td>
<td style="text-align:left;">
Brothers of Italy - National Centre-right
</td>
<td style="text-align:right;">
2013
</td>
<td style="text-align:right;">
2.00
</td>
<td style="text-align:right;">
47.38
</td>
<td style="text-align:right;">
86.82
</td>
</tr>
<tr>
<td style="text-align:left;">
Latvia
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
NA
</td>
<td style="text-align:left;">
Latvian National Independence Movement
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:right;">
16.60
</td>
<td style="text-align:right;">
57.50
</td>
<td style="text-align:right;">
76.03
</td>
</tr>
<tr>
<td style="text-align:left;">
Lithuania
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
DK
</td>
<td style="text-align:left;">
The Way of Courage
</td>
<td style="text-align:right;">
2012
</td>
<td style="text-align:right;">
8.00
</td>
<td style="text-align:right;">
35.17
</td>
<td style="text-align:right;">
76.08
</td>
</tr>
<tr>
<td style="text-align:left;">
Luxembourg
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
ADR
</td>
<td style="text-align:left;">
Alternative Democatic Reform Party
</td>
<td style="text-align:right;">
2013
</td>
<td style="text-align:right;">
6.60
</td>
<td style="text-align:right;">
60.00
</td>
<td style="text-align:right;">
85.56
</td>
</tr>
<tr>
<td style="text-align:left;">
Netherlands
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
SGP
</td>
<td style="text-align:left;">
Reformed Political Party
</td>
<td style="text-align:right;">
2012
</td>
<td style="text-align:right;">
2.10
</td>
<td style="text-align:right;">
60.98
</td>
<td style="text-align:right;">
85.97
</td>
</tr>
<tr>
<td style="text-align:left;">
Netherlands
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
PVV
</td>
<td style="text-align:left;">
Party for Freedom
</td>
<td style="text-align:right;">
2012
</td>
<td style="text-align:right;">
10.10
</td>
<td style="text-align:right;">
48.54
</td>
<td style="text-align:right;">
76.34
</td>
</tr>
<tr>
<td style="text-align:left;">
Norway
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
FrP
</td>
<td style="text-align:left;">
Progress Party
</td>
<td style="text-align:right;">
NA
</td>
<td style="text-align:right;">
NA
</td>
<td style="text-align:right;">
64.17
</td>
<td style="text-align:right;">
75.37
</td>
</tr>
<tr>
<td style="text-align:left;">
Poland
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
PiS
</td>
<td style="text-align:left;">
Law and Justice
</td>
<td style="text-align:right;">
2011
</td>
<td style="text-align:right;">
29.90
</td>
<td style="text-align:right;">
31.37
</td>
<td style="text-align:right;">
77.83
</td>
</tr>
<tr>
<td style="text-align:left;">
Poland
</td>
<td style="text-align:right;">
2010
</td>
<td style="text-align:left;">
LPR
</td>
<td style="text-align:left;">
League of Polish Families
</td>
<td style="text-align:right;">
2007
</td>
<td style="text-align:right;">
1.30
</td>
<td style="text-align:right;">
32.25
</td>
<td style="text-align:right;">
85.72
</td>
</tr>
<tr>
<td style="text-align:left;">
Poland
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
KNP
</td>
<td style="text-align:left;">
Congress of the New Right
</td>
<td style="text-align:right;">
2011
</td>
<td style="text-align:right;">
1.10
</td>
<td style="text-align:right;">
96.03
</td>
<td style="text-align:right;">
78.75
</td>
</tr>
<tr>
<td style="text-align:left;">
Poland
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
SP
</td>
<td style="text-align:left;">
United Poland
</td>
<td style="text-align:right;">
2011
</td>
<td style="text-align:right;">
NA
</td>
<td style="text-align:right;">
33.40
</td>
<td style="text-align:right;">
82.04
</td>
</tr>
<tr>
<td style="text-align:left;">
Romania
</td>
<td style="text-align:right;">
2010
</td>
<td style="text-align:left;">
PRM
</td>
<td style="text-align:left;">
Greater Romania Party
</td>
<td style="text-align:right;">
2008
</td>
<td style="text-align:right;">
3.20
</td>
<td style="text-align:right;">
22.70
</td>
<td style="text-align:right;">
82.39
</td>
</tr>
<tr>
<td style="text-align:left;">
Romania
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
PP-DD
</td>
<td style="text-align:left;">
People's Party - Dan Dianconescu
</td>
<td style="text-align:right;">
2012
</td>
<td style="text-align:right;">
14.00
</td>
<td style="text-align:right;">
31.46
</td>
<td style="text-align:right;">
78.97
</td>
</tr>
<tr>
<td style="text-align:left;">
Slovakia
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
KDH
</td>
<td style="text-align:left;">
Christian Democratic Movement
</td>
<td style="text-align:right;">
2012
</td>
<td style="text-align:right;">
8.80
</td>
<td style="text-align:right;">
52.50
</td>
<td style="text-align:right;">
79.98
</td>
</tr>
<tr>
<td style="text-align:left;">
Slovakia
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
SNS
</td>
<td style="text-align:left;">
Slovak National Party
</td>
<td style="text-align:right;">
2012
</td>
<td style="text-align:right;">
4.60
</td>
<td style="text-align:right;">
46.70
</td>
<td style="text-align:right;">
90.84
</td>
</tr>
<tr>
<td style="text-align:left;">
Slovenia
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
SDS
</td>
<td style="text-align:left;">
Slovenian Democratic Party
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:right;">
20.70
</td>
<td style="text-align:right;">
78.26
</td>
<td style="text-align:right;">
78.60
</td>
</tr>
<tr>
<td style="text-align:left;">
Slovenia
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
NSI
</td>
<td style="text-align:left;">
New Slovenia -- Christian People's Party
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:right;">
5.60
</td>
<td style="text-align:right;">
78.36
</td>
<td style="text-align:right;">
77.96
</td>
</tr>
<tr>
<td style="text-align:left;">
Sweden
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
SD
</td>
<td style="text-align:left;">
Sweden Democrats
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:right;">
12.90
</td>
<td style="text-align:right;">
45.74
</td>
<td style="text-align:right;">
87.58
</td>
</tr>
<tr>
<td style="text-align:left;">
Switzerland
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
SVP/UDC
</td>
<td style="text-align:left;">
Swiss People's Party
</td>
<td style="text-align:right;">
NA
</td>
<td style="text-align:right;">
NA
</td>
<td style="text-align:right;">
73.12
</td>
<td style="text-align:right;">
83.58
</td>
</tr>
<tr>
<td style="text-align:left;">
Switzerland
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
EDU/UDF
</td>
<td style="text-align:left;">
Federal Democratic Union of Switzerland
</td>
<td style="text-align:right;">
NA
</td>
<td style="text-align:right;">
NA
</td>
<td style="text-align:right;">
52.50
</td>
<td style="text-align:right;">
82.88
</td>
</tr>
<tr>
<td style="text-align:left;">
Turkey
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
MHP
</td>
<td style="text-align:left;">
National Action Party
</td>
<td style="text-align:right;">
NA
</td>
<td style="text-align:right;">
NA
</td>
<td style="text-align:right;">
49.90
</td>
<td style="text-align:right;">
79.81
</td>
</tr>
<tr>
<td style="text-align:left;">
UK
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:left;">
UKIP
</td>
<td style="text-align:left;">
United Kingdom Independence Party
</td>
<td style="text-align:right;">
2010
</td>
<td style="text-align:right;">
3.10
</td>
<td style="text-align:right;">
82.92
</td>
<td style="text-align:right;">
85.75
</td>
</tr>
<tr>
<td style="text-align:left;">
UK
</td>
<td style="text-align:right;">
2010
</td>
<td style="text-align:left;">
BNP
</td>
<td style="text-align:left;">
British National Party
</td>
<td style="text-align:right;">
2010
</td>
<td style="text-align:right;">
1.90
</td>
<td style="text-align:right;">
33.61
</td>
<td style="text-align:right;">
85.86
</td>
</tr>
</tbody>
</table>
