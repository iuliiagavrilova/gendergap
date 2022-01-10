# Gender Gap Project. Is there a correlation between gender share in tertiary education and the gender pay gap? 


## 
**1. Introduction**

In recent years, the issue of persistent gender inequality across different areas of life is becoming more and more visible. 

One of the major problems that have been put on the map during the last decades is the pay gap. Women are consistently underpaid for the same jobs as men or are encouraged to occupy low-qualified and, therefore, low-paid jobs. Nurses, caregivers, kindergarten and primary school teachers are considered to be ‘female’ jobs while politicians, professors, lawyers, and programmers are professions ‘for men’.  

We have decided to look into the pay gap across different European countries and investigate whether the level of education may give an explanation for the payment differences. For example, higher-level education is believed to be one of the most important factors for finding a good job and getting a good salary. 

We have investigated gender distribution in tertiary education and whether or not it correlates with the gender pay gap. What was discovered is that female students enrolled in tertiary education represent the majority in academies. We can see that why there are more educated women than men they still have to count on lower payments than their male counterparts.


## 
**2. Application scenario**

Gender Gap Project aligns data from different sources in order to gain insight, through data, into the factors behind the gender pay gap. The results of the project can be used to illustrate inequalities in the workplace both for educational purposes and lawmaking purposes. Statistics help us to gain an objective insight into the nature of the workplace for women and try to mitigate these injustices.

In order to be able to track any correlation between women and academies and the gender pay gap, we had to align the geodata of the two datasets as well as the timeframe. The result is the clickable visualization of the gender pay gap and education gap across different countries.


### 
**2.1 The data**

Gender Gap Project uses an open-source dataset provided by Eurostat about the gender pay gap across different countries of the European Union. This dataset measures the difference between average gross hourly earnings of male paid employees and of female paid employees as a percentage of average gross hourly earnings of male paid employees. The indicator has been defined as unadjusted because it gives an overall picture of gender inequalities in terms of pay and measures a concept that is broader than the concept of equal pay for equal work. All employees working in firms with ten or more employees, without restrictions for age and hours worked, are included.

It also uses data provided by Eurostat about students enrolled in tertiary education by education level, program orientation, sex, and field of education. We have aggregated the data in order to obtain the total number of female students in the academy including enrolled students, learning mobility, education personnel, education finance, graduates, and language learning students.


### 
**2.2 How Gender Gap can contribute to E-Governance**

In the context of E-Governance, Gender Gap might play a role in:



* promoting debate among citizens, who could press authorities for an introduction of better policies that would promote gender equality;
* raising awareness about gender inequality in academy and workplace;
* reducing the gender pay gap via the promotion of better policies in the private sector;
* reducing the gender imbalance in tertiary education by introducing quotas and other measures.

**3. Original datasets and mashup**


### 
**D1**

Eurostat, 04/05/2021, Gender pay gap in unadjusted form, viewed 11 November 2021, 

[https://data.europa.eu/data/datasets/bqa6wwduux4gosowoquq?locale=en](https://data.europa.eu/data/datasets/bqa6wwduux4gosowoquq?locale=en) 

License: [https://ec.europa.eu/eurostat/statistics-explained/index.php?title=Copyright/licence_policy](https://ec.europa.eu/eurostat/statistics-explained/index.php?title=Copyright/licence_policy) 

Content description: The indicator measures the difference between average gross hourly earnings of male paid employees and of female paid employees as a percentage of average gross hourly earnings of male paid employees. The indicator has been defined as unadjusted because it gives an overall picture of gender inequalities in terms of pay and measures a concept that is broader than the concept of equal pay for equal work. All employees working in firms with ten or more employees, without restrictions for age and hours worked, are included. The gender pay gap is based on the methodology of the structure of earnings survey (SES), which is carried out every four years.


### 
**D2**

Eurostat, 28/10/2021, Students enrolled in tertiary education by education level, program orientation, sex, and field of education, viewed 11 November 2021, 

[https://data.europa.eu/data/datasets/tvoyfp236pvctmgfqyudca?locale=en](https://data.europa.eu/data/datasets/tvoyfp236pvctmgfqyudca?locale=en)

License: [https://ec.europa.eu/eurostat/statistics-explained/index.php?title=Copyright/licence_policy](https://ec.europa.eu/eurostat/statistics-explained/index.php?title=Copyright/licence_policy) 

Content description: This domain covers statistics and indicators on key aspects of the education systems across Europe. The data show entrants and enrolments in education levels, education personnel, and the cost and type of resources dedicated to education.

Data and indicators disseminated include e.g. participation rates at different levels of education, shares of pupils and students by program orientation (general/academic and vocational/professional) and in combined school and work-based programs, enrolments in public and private institutions, tertiary education graduates, degree mobile students enrolled and graduates, pupil-teacher ratios, foreign language learning, expenditure on education per student and relative GDP.


### 
**D3 (mashup)**

Dataset: https://github.com/iuliiagavrilova/gendergap/blob/main/dataset/gender%20gap%20project.rdf

Metadata: https://github.com/iuliiagavrilova/gendergap/blob/main/metadata/metadata.rdf

Content description: The mashup dataset shows the gender pay gap and distribution of females in academies in percentage across different countries of the European Union in the period from 2013 to 2018. 

Methodology: The mashup of datasets D1, D2, D4.2 was done semi-automatically using Python scripts and the library Pandas, which required a CSV version of the datasets as an input. The script developed using Pandas was able to align D1 and D2 through the geo and year properties. The newly created dataset was then cleaned to remove empty values. The data about women in tertiary education across different levels and types of education were aggregated in order to obtain the total percentage. 

After the semi-automatic mashup, the mashup was edited to remove unnecessary data such as data related to EU-27 and EU 28, not covered by this project. Subsequently, the headings of the CSV dataset were modified in order to facilitate further computation processes.

Finally, the CSV dataset obtained was transformed into an RDF dataset. The RDF dataset obtained made use of OWL ontology.


## 
**4. Datasets analysis**


### 
**4.1 Information quality**

In this section, we make some observations related to information quality in the main datasets used in the Gender Gap Project (D1, D2, D3) according to the "[Linee guida per la valorizzazione del patrimonio informativo pubblico" by AGID](https://docs.italia.it/italia/daf/lg-patrimonio-pubblico/it/stabile/aspettiorg.html#qualita-dei-dati).


#### Accuracy

D1 contains data about the overall picture in terms of gender inequality in terms of pay. However, it is defined as unadjusted because it measures a concept that is broader than the concept of equal pay for equal work. 

The indicator is produced according to the high-level quality standards of European Statistics. The unadjusted gender pay gap (GPG) represents the difference between the average gross hourly earnings of male paid employees and of female paid employees as a percentage of average gross hourly earnings of male paid employees. The GPG is calculated on the basis of:

- the four-yearly Structure of Earnings Survey (SES) 2002, 2006, 2010, and 2014, and with the scope as required by the SES regulation,

 - national estimates based on national sources for the years between the SES years, from the reference year 2007 onwards, with the same coverage as the SES.

Data are broken down by economic activity (Statistical Classification of Economic Activities in the European Community - NACE), economic control (public/private) of the enterprise as well as working time (full-time/part-time), and age (six age groups) of employees. Data are released in February/March on the basis of information provided by national statistical institutes.

The gender pay gap for the EU is calculated as the weighted mean of the gender pay gaps in the EU Member States, where the numbers of employees in the Member States are weighted. The EU gender pay gap is calculated only for the aggregated sections B to S without O.

D2 covers statistics and indicators on key aspects of the education systems across Europe. The data show entrants and enrolments in education levels, education personnel, and the cost and type of resources dedicated to education. 

The quality of the education systems statistics from UOE data collection is ensured through specific requirements set in Regulation (EC) No 452/2008 and the details provided in Commission Regulation (EU) No 912/2013 for data from 2013 onwards and Commission Regulation (EU) No 88/2011 for 2011 and 2012 data. Until 2011 data was collected based on gentlemen’s agreement.

Quality is also reflected through the use of harmonized definitions and concepts. Specific recommendations to help countries properly collect the expected data are also available through a set of methodological documents and guidelines. The quality is discussed in working groups (such as the Education and Training Statistics Working Group) within the European Statistical System (ESS) and with other organizations involved in UOE data collection, namely UNESCO-UIS and OECD.

UOE data is provided in the standard questionnaires prepared jointly by the three organizations (UNESCO-UIS, OECD, and Eurostat). For countries that are both EU and OECD members, a common validation process is carried out by the two organizations based on gentlemen’s agreement.

UOE statistics are considered to be of good quality thanks to a harmonized production process (as described in item 11.1. above).

Data quality requirements and standard quality reports are set out in Annex II of Commission Regulation (EU) No 912/2013. The EU Member States and EFTA countries are obliged to transmit to Eurostat the standard quality reports together with ISCED mapping of national programs and qualifications every year.

D3 dataset was mashup relying on quality data provided by Eurostat. We have used the methods of data aggregation and data cleaning in order to obtain new data. No third-party data has been introduced to the abovementioned datasets.


#### Coherence

We haven’t managed to find any contradictions in D1. The data about the gender pay gap in different European countries don’t intersect and don’t contradict each other.

D2 -  The education systems differ between countries. The ISCED 2011 classification makes it possible to compare educational levels in spite of these differences, but the differences may nevertheless affect certain figures. The degree structures differ between countries. To which extent students qualify for and receive more than one qualification differs between the countries, as well as the length of studies to obtain a degree.

In indicators of participation rates, enrolment statistics are related to population statistics. The reference date for ages is the same (1st of January) but differences in data collection dates or methodologies may result in slight differences, which affect the participation rates. Percentages above 100 percent can be due to such differences, but can also appear because of inflows or outflows of students. The enrolment statistics refer to all education enrolments within the country while population statistics refer to residents in the country. In some countries, where the outflow of students is substantial (Luxembourg, Cyprus), specific notes are added in the tables, but other countries' figures may also be affected.

Country of origin in the learning mobility data should in principle refer to the "country of prior secondary education". However, until the reference year, 2016 countries might use instead country of prior residence or citizenship or other. From the reference year 2016 onwards all countries should report data according to "country of prior education". Information on the specific definition currently used by countries is available in Chapter 3. Annexes "Footnotes - Learning mobility".


#### Completeness

D1 - The data about EU countries’ pay gap is complete. 

D2 - The data sent by participating countries to Eurostat are overall complete and match the requirements set out in the Commission Regulations or gentlemen’s agreement.

Nevertheless, some national datasets are not always fully match the expected format because some content is missing or is not applicable. In those cases the data disseminated are displayed as ‘not available’ (‘:’) or ‘not applicable’ (‘:’z). This can be explained either because the country could not implement the variable for some reason and may have received a temporary derogation from implementing the Commission Regulations or because the concept does not exist in the country.


#### Actuality

D1 and D2 are regularly updated and include information about recent years. In the D3 dataset, we have concentrated on a 5-year time span that contains information both about the gender pay gap and the number of students in tertiary education by gender. 


### 
**4.2 Juridical and ethical analysis **


#### 
**Privacy**

The dataset is free of any personal data as defined in the Regulation (EU) 2016/679. It is also free of any indirect personal data that could be used for identifying the natural person. It is free of any information that combined with common data available in the web, could identify the person. It doesn’t contain any information related to human rights (e.g. refugees, witness protection, etc.). Geolocalization data doesn’t allow the identification of single individuals. 


#### 
**Licenses**

D1 and D2 are licensed under CC-BY 4.0. Each dataset is accompanied by a clear license declaration.

D3 is distributed by CC-BY 4.0.


### 
**4.3 Technical analysis (formats, metadata, URIs, provenance)**


### 
**4.4 Updating the dataset over time**

We do not plan to update the Gender Gap Project. However, it would be interesting to create new datasets for the following years to see whether the trend for gender inequality persists or some improvements happen.

**5. Visualization**

To provide visualization, we have used D3 in CVS format and the program Flourish. We have created a clickable map that allows seeing the percentage of women in tertiary education across different countries.

We have also decided to display the comparison between percentages in the gender pay gap and in education using a grouped bar chart. 


### 
**5.1 Data processing**

Although the final dataset has been released in RDF format, the CSV has also been made available on the project GitHub repository as it was used to extract the data needed in order to produce the visualization.


## 
**6. Final considerations**

By looking at the data about the gender pay gap and the percentage of women enrolled in higher educations, we can detect clear trends. Women tend to represent the overall majority of students in higher education. However, in the professional world, their education doesn’t pay off. All across Europe, women are underpaid about 10 to 20% in comparison to men. This data allows us to talk about gender-based inequalities.

However, the data that we have isn’t enough to explain why the inequality persists. For example, we didn’t investigate how many women that have obtained a Bachelor's or Master’s degree go on to continue their career in the academy to obtain a Ph.D. that can result in a better paid and prestigious career. We also don’t know about other potential factors that can cause such inequalities. 
