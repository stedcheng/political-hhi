<h1>Unveiling the Enablers: Analyzing the Persistence of Dynasties in Local Philippine Politics</h1>

<h2>Abstract</h2>
<h3>Introduction and Literature Review</h3>
Political dynasties have long dominated Philippine politics, raising concerns about their impact on democratic processes. Previous studies have linked the concentration of political power in dynasties to higher poverty and corruption rates using indices like Dynastic Share and Political Herfindahl-Hirschman Index (HHI). However, these studies overlook reverse causality, prompting us to explore how household-level socioeconomic factors might influence the political power concentration. Our aim is to identify these factors that enable dynastic persistence
and propose effective policy interventions to address this issue.

<h3>Methods</h3>
The dataset of winning politicians per election from 2004 to 2016 was sourced from the Ateneo School of Government, and the proportion of each last name was used to calculate the political HHI for each election year and province. The geographic dataset, which is a shapefile with provincial and districtal granularity, was matched with HHI data and utilized to calculate latitude and longitude. The FIES datasets published from 2006 to 2018 were retrieved from the PSA data archive; common columns were selected and aggregated in terms of mean per province, and only common provinces in both FIES and HHI datasets were retained. Then, OLS regression was done to determine the FIES variables that affect the HHI. Finally, the concept of spatial regression was applied due to the geographic nature of the dataset, using the Moran's I statistic to test for spatial autocorrelation as well as the Lagrange multiplier tests for spatial lag and error dependence.

<h3>Results</h3>
From the OLS regression, along with VIF diagnostics, 21 variables were found to have no multicollinearity, and further selection based on statistical significance narrowed this down to 10 key factors. Among these, regular employment rates had the most significant impact on political power concentration, meaning that higher employment levels led to increased political power concentration; while the remaining 10 key factors, such as income from livestock and other sectors, were negatively associated with political power concentration. The final model explains 29.2% of the variation in the logarithmic transformation of political power concentration, suggesting that economic diversification may help reduce political monopolies. Additionally, spatial autocorrelation is present between the provincial HHI values and our variables of interest, and such correlation is present in the error terms of the model. The spatial error model reveals that four FIES variables (income from agriculture, forestry, construction, and entrepreneurial services) can explain values of provincial political aggregation even in the presence of spatial correlation.

<h3>Conclusion</h3>
Our research poses two significant insights: (1) the income attained by households and society from essential sectors such as agriculture and fisheries can act as determinants of increasing political concentration at the provincial level, and (2) political power aggregation happens beyond geographical boundaries. These issues pose significant concern on how we can prevent spillover effects of political power concentration in the hands of the few in minute processes in the society. Thus, our group calls for creation of bills and policies that will prevent politicization of vital sectors of the society, as well as an Anti-Dynasty Bill that will formally define what dynasty is and how it will become measured. These policies are suggested to ensure that a healthy competition shall still persist during election periods and prevent any collusion from political clans.

<h2>R Markdown (RMD) files and PDFs</h2>
<ul>
  <li><code>1 HHI Computation</code>: Code used to compute the HHI from the winning politicians data.</li>
  <li><code>2 Merging Geographical and HHI Data; 4 Visualizations.rmd</code>: Code used to merge the geographical and HHI data (described in the Methods section), and codes used for exploratory data analysis on the HHI data (described in the Results section).</li>
  <li><code>3 FIES Data Cleaning.rmd</code>: Codes used to perform data cleaning on FIES datasets such as column selection, province code extraction, and aggregation.</li>
  <li><code>5 OLS Regression.rmd</code>: Codes used to fit an OLS regression model to the cleaned dataset, with the associated hypothesis tests and plots.</li>
  <li><code>6 Spatial Regression.rmd</code>: Codes used to fit a spatial regression model to the cleaned dataset, with the associated hypothesis tests and plots.</li>
  <li><code>Merged RMD Files.pdf</code>: All the five RMD files are converted to PDF and merged into one file.</li>
  <li><code>Slide Deck.pdf</code>: Slide deck used to present the research. (For a more complete discussion, check the <a href="https://drive.google.com/open?id=1cI8-gr_IoQ5cf_J_n5p232eWF_7c5B_K&usp=drive_copy">video</a>.)</li>
</ul>

<h2>Datasets</h2>
This includes both raw and intermediate datasets. All datasets should be placed in the path <code>datasets/</code>.

<h3>Uploaded Datasets</h3>
<ul>
  <li><code>ASoG-POLITICAL-DYNASTIES-DATASET.xlsx</code>: Sourced from <a href="https://www.inclusivedemocracy.ph/data-and-infographics">Ateneo School of Government</a>, used in RMD 1.</li>
  <li><code>unweighted_hhi_yearly.csv</code>: Produced in RMD 1, used in RMD 2.</li>
  <li><code>fies_hhi_all_years.csv</code>: Produced in RMD 3, used in RMD 4 and 5.</li>
</ul>

<h3>Unuploaded Datasets</h3>
The following datasets are unuploaded due to their large size.
<ul>
  <li><code>raw_geo_dataset</code> folder: Sourced from <a href="https://github.com/altcoder/philippines-psgc-shapefiles/blob/main/dist/PH_Adm2_ProvDists.shp.zip">GitHub</a>, used in RMD 2. The following files should be in the <code>datasets/raw_geo_dataset/</code> folder:</li><ul>
    <li><code>Provdists.shp.cpg</code></li>
    <li><code>Provdists.shp.dbf</code></li>
    <li><code>Provdists.shp.prj</code></li>
    <li><code>Provdists.shp.shp</code></li>
    <li><code>Provdists.shp.shx</code></li></ul>
  <li><code>hhi_map</code> folder: Produced in RMD 2, used in RMDs 3 and 5.</li>
  <li><code>fies_datasets</code> folder: Sourced from <a href="https://psada.psa.gov.ph/catalog/FIES/about">FIES (Family Income Expenditure Survey)</a>, used in RMD 3. The following CSVs should be in the <code>datasets/fies_datasets/</code> folder:</li><ul>
  <li>2006: <code>FIES PUF 2006 Vol.1.csv</code></li>
  <li>2009: <code>FIES PUF 2009 Vol.2.csv</code></li>
  <li>2012: <code>FIES PUF 2012 Vol.1.csv</code></li>
  <li>2015: <code>FIES PUF 2015 Vol.1.csv</code></li>
  <li>2018: <code>FIES PUF 2018 Vol.1.csv</code></li></ul></ul>

<h2>Credits</h2>
This project was created by Rafael Acuna, Aldie Alejandro, Sted Cheng, Ivan De Leon, and Rafael Tagulao, and submitted as a requirement for the course <b>ECON 185.78i: Data Science for Economists</b> taken in the first semester of AY 2024-2025 in Ateneo de Manila University. 


