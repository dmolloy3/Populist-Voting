Party Graphs
================
Declan Molloy
08/04/2018

Identifying Populist Parties
============================

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

<img src="Party_Graphs_files/figure-markdown_github/compare-1.png" alt="Significant differences in how the two methods classify parties" width="100%" />
<p class="caption">
Significant differences in how the two methods classify parties
</p>

Finally, I've plotted the residuals themselves, with the same parties labelled (Figure @ref(fig:resid-compare)).

<img src="Party_Graphs_files/figure-markdown_github/resid-compare-1.png" alt="Above 0 means a party's CHES populism score is higher (more populist) than expected given its score from the Manifesto Project" width="100%" />
<p class="caption">
Above 0 means a party's CHES populism score is higher (more populist) than expected given its score from the Manifesto Project
</p>
