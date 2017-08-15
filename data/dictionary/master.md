---
layout: default
---

## # Master List of Variables

---

#### **geoid**
Unique 11-digit US 2010 Census Tract ID.

---


# Walkability Variables

#### **t10km2**
Total area of US 2010 Census Tract geography in km2.
 
# Walkability Variables

#### **t10lndkm2**
Total land area of US 2010 Census Tract geography in km2 (inland water bodies removed).
 
# Walkability Variables

#### **t10cnt**
Count of unique 2010 Census Blocks nested within each Tract and whose walkability index scale values participated in averaging-up process for each Tract.
 
# Walkability Variables

#### **t10resdn1**
Density of residential units: z-scored.
 
# Walkability Variables

#### **t10intden**
Density of unique streets intersections per km2: z-scored.
 
# Walkability Variables

#### **t10entrpy**
Entropy land use mix: z-scored.
 
# Walkability Variables

#### **t10rtlfar**
Retail floor area ratio: z-scored.
 
# Walkability Variables

#### **t10sub07d**
Density of subway stations per km2: z-scored.
 
# Walkability Variables

#### **t10walk**
BEH Walkability Scale.
 
# Walkability Variables

#### **t10walkc**
Quintiles of BEH Walkability Scale.

--- 

The information below is from a BEH data dictionary by James Quinn, Senior GIS Analyst called [GIS Code Book: New York City 2010 Census Tract Walkability Index](https://github.com/beh-gis/beh-gis.github.com/raw/master/projects/data_dictionary/walkability-gis-codebook-2010-tracts-20150112.pdf)

### Walkability Index Scale
A number of researchers have constructed walkability indices which summarize built environment features believed to promote walking. Although specification details vary, these indices typically include measures of population density, land use, and street network. Our walkability measure was adapted from that employed in recent papers by Frank and colleagues (2005 and 2006), which includes four components: residential population density (density of population per total residential land area), intersection density, an entropy measure of land use based on the distribution of building floor area among six land use types (education, entertainment, single-family residential, multi-family residential, retail, and office), and the retail floor area ratio, or the ratio of retail building floor area to retail land area. All of the Frank components were z-scored and summed, with intersection density receiving a double weight for the Frank Scale, but not for our scale. Our “BEH walkability scale” is documented in a paper by Neckerman and colleagues (2009).

* *Frank et al. Linking objectively measured physical activity with objectively measured urban form: findings from SMARTRAQ. American Journal of Preventive Medicine. 2005;28(2 Suppl 2):117-125.*
* *Frank et al. Many Pathways from Land Use to Health: Associations between Neighborhood Walkability and ActiveTransportation, Body Mass Index, and Air Quality. Journal of the American Planning Association. 2006;72(1):75-87.** *Neckerman et al. Disparities in urban neighborhood conditions: Evidence from GIS measures and field observation in New York City. Journal ofPublic Health Policy. 2009;1(1 Suppl): S264-S285.*
            
Important Note:Many of the figures in this document refer to 2010 Census Blocks. This data dictionary is for the 2010 Census Tracts. Figuresare only for illustrative purposes.

# Walkability Index Scales: City-­Wide Buffers
As an alternative to creating a ‘neighborhood walkability index scale’ based solely on the z-scored components within buffers specific to a study cohort, the BEH Working Group has developed a walkability index scale that considers the z-scored components across New York City as a whole.
The issue with creating a walkability index scale using buffer definitions specific to a study cohort is that the cohort may be spatially biased or clustered in a particular neighborhood(s) or parts of the City (e.g., northern Manhattan or the south Bronx). This could dramatically influence the range of z-scored components, and thus not provide a representative scale of walkability for that cohort compared to the walkability of the rest of the City.
The BEH Working Group has tackled this problem by buffering 2010 Census Block centroids (n=38,526) by 1-km radial buffers and then deriving the walkabilitycomponents that are later z-scored. In doing so, a more appropriate apples-to-apple comparison of walkability can be made between, say, an address in Staten Island to the rest of the City as whole rather than a cluster ofaddresses all within a similar built environment.

# Averaging up to Tract
In order to assign each 2010 Census Tract with the city-wide walkability index scale, the walkability index scale values for each Block centroid were simply averaged up to the Tract level. The following variables are the result of that process:
#### t10_key
Unique 11-digit US 2010 Census Tract ID.
#### t10_km2
Total area of US 2010 Census Tract geography in km2.
#### t10_lndkm2
Total land area of US 2010 Census Tract geography in km2 (inland water bodies removed).
#### t10_cnt
Count of unique 2010 Census Blocks nested within each Tract and whose walkability index scale values participated in averaging-up process for each Tract.
#### t10_walk
BEH Walkability Scale.

# Walkability Index Scale VariablesTo date, BEH has created and used two different versions of the Walkability Index Scales, which we refer to here as the “Frank et al. 2006” and BEH scales. The “Frank 2006” includes z-scored variables: residential density, land use mix using 5 land use types, intersection density * 2, and retail area ratio. The BEH scale includes z-scored variables: residential density,land use mix using 5 land use types, intersection density, retail area ratio, and subway stop density. Note that the BEH scale does not multiply intersection density by 2 and does include subway density.
#### t10_intden_z
Density of unique streets intersections per km2: z-scored.
#### t10_sub07d_z
Density of subway stations per km2: z-scored.
#### t10_rtlfar_z
Retail floor area ratio: z-scored.
#### t10_resdn1_z
Density of residential units: z-scored.
#### t10_entrpy_z
Entropy land use mix: z-scored.
#### t10_walk_cat
Quintiles of BEH Walkability Scale.

**Please note that the variables in text below have not been provided in this deliverable and are only described here to provide context for the variables that are being provided.**
# Walkability Index Scale “Component” Variables(these variables are not included in the dataset)
#### b1_intden
Density of unique streets intersections per km2.
#### b1_sub07d
Density of subway stations per km2.
#### b1_rtlfar
Retail floor area ratio – Retail building floor area divided by retail land area in km2.
#### b1_resdn1
Density of res units – Number of residential units divided by total residential building floor area in km2.
#### b1_entrpy
Land Use Mix – An entropy measure using the five of the six land use types employed in Frank et al. (2006). Single- and multi-family residential areas were combined because most housing in New York City is multi-family. Parcel-level measures of residential, office, and retail floor area were available from the MapPLUTO (version 04c; October 2004-October 2005) database. We used the MapPLUTO building class codes to identify buildings associated with education (schools) or entertainment (theaters, recreational facilities), and attributed the entire floor area of the identified building to education orentertainment. The entropy formula used was adapted from Frank et al. (2005), which yielded more plausible results: Land Use Mix = A/ln(N) where: A= –((b1/a)*ln(b1/a)+(b2/a)*ln(b2/a)+…) and b1 is the building floor area covered by the first land use, b2 is the building floor area covered by the second land use, etc., a is the total floor area across the five land uses, and N is the total number of land uses represented in the census tract. Zero values for b1…b5 were set to .000001 to avoid zero or undefined terms.

* ### Components of the Entropy Measure:
	* #### b1_b1
	Total building area for Education uses in square feet (set to .000001 if 0)	* #### b1_b2
	Total building area for Entertainment uses in square feet (set to .000001 if 0)	* #### b1_b3
	Total building area Residential uses in square feet (set to .000001 if 0)	* #### b1_b4
Total building area for Retail uses in square feet (set to .000001 if 0)	* #### b1_b5
Total building area for Office uses in square feet (set to .000001 if 0)	* #### b1_a
Total floor area across the five land uses in square feet (set to .000001 if 0)	* #### b1_n
The total number of land uses represented (between 1 and 5)

### ArcMap Entropy Field Calculation Expression:	
	entropy = –((([b1] / [a]) * log ( [b1] / [a] )) + (([b2] / [a]) * log ( [b2] / [a] )) + (([b3] / [a]) * log ( [b3] / [a] )) + (([b4] / [a]) * log ( [b4] / [a] )) + (([b5] / [a]) * log ( [b5] / [a] ))) / log ( [n] ) 
 
# Tree Canopy Variables

#### **t10treepc**
Percent of Tract Covered with Tree Canopy

--- 
The following set of variables regard Tree Canopy.

 
 
# ACS 2008-2012 Median Household Income Variables

#### **t10mhhi**
Median Household Income (t10_057001) from 2008-2012 American Community Survey

--- 
[American Community Survey](http://www.census.gov/acs/www/) 
 
# Off-Premise Alcohol Licenses Variables

#### **t10alcelig**
CDEligible
 
# Off-Premise Alcohol Licenses Variables

#### **t10alcall**
Count all License types
 
# Off-Premise Alcohol Licenses Variables

#### **t10alccl1**
Count On Premise Licenses
 
# Off-Premise Alcohol Licenses Variables

#### **t10alccl2**
Count Off Premise Licenses
 
# Off-Premise Alcohol Licenses Variables

#### **t10alccl3**
Count Wholesale Licenses
 
# Off-Premise Alcohol Licenses Variables

#### **t10alccl4**
Count Pending Licenses
 
# Off-Premise Alcohol Licenses Variables

#### **t10alccl5**
Count Disabled Licenses

--- 
Information and notes from the NYS-SLA recieved April 2013. 

### Liquor Authority Permit Data Overview#### General Description
The State Liquor Authority (SLA) regulates the manufacture and sale of alcoholic beverages.  The SLA maintains offices in New York City, Albany (which serves as the agency headquarters), and Buffalo.  The SLA’s Licensing Bureau is responsible for the statewide processing of licenses, license renewals, permits and brand label registrations.  All must be consistent with the Alcoholic Beverage Control Law.#### Data Collection Methodology
Base information corresponds to that provided, by applicants, on various permit applications.  Processing time is contingent upon review within the Licensing Bureau.#### Statistical and Analytical Issues
Information is entered into the agency’s workflow system as permits are received.  Correlations could be made for different variables as a user of the data assesses the information.#### Limitations of Data Use
The data is straight forward and indicates the facts associated with each permit request. 
 
# ACS 2008-2012 Total Population Variables

#### **t10totpop**
Total Population Estimate (B01003 - TOTAL POPULATION Universe: Total population) from 2008-2012 American Community Survey

--- 
[American Community Survey](http://factfinder.census.gov/faces/nav/jsf/pages/searchresults.xhtml?refresh=t#) 
 
# ACS 2008-2012 Population Density-Land Area Variables

#### **t10popdens**
Population Density - Total Population Estimate (B01003 - TOTAL POPULATION Universe: Total population) from 2008-2012 American Community Survey / t10lndkm2 - (land area in square km)

--- 
[American Community Survey](http://factfinder.census.gov/faces/nav/jsf/pages/searchresults.xhtml?refresh=t#) 
 
# ACS 2008-2012 Percent Age 65 and Up Variables

#### **t10pcag65u**
Percent population 65 years of age and older - American Community Survey 2008-2012 (5-year)

--- 
#### Percent population 65 years of age and older in Neighborhood Geography.
#### American Community Survey 2008-2012 (5-year)	( df[geo+'B01001020E'] + df[geo+'B01001021E'] + df[geo+'B01001022E'] + df[geo+'B01001023E'] + df[geo+'B01001024E'] + df[geo+'B01001025E'] + df[geo+'B01001044E'] + df[geo+'B01001045E'] + df[geo+'B01001046E'] + df[geo+'B01001047E'] +df[geo+'B01001048E'] + df[geo+'B01001049E'] ) / df[geo+'B01001001E'] 
 
# ACS 2008-2012 Percent in Poverty Variables

#### **t10pcpov**
Percent population in poverty

--- 

#### Percent population in poverty 
#### American Community Survey 2008-2012 (5-year)	( df[geo+'C17002002E'] + df[geo+'C17002003E'] ) / df[geo+'C17002001E'] 
 
# ACS 2008-2012 Percent Black Variables

#### **t10pcblack**
Percent population Black

--- 
#### Percent population Black#### American Community Survey 2008-2012 (5-year)	df[geo+'B02001003E'] / df[geo+'B02001001E'] 
 
# ACS 2008-2012 Percent Asian Variables

#### **t10pcasian**
Percent population Asian

--- 

#### Percent population Asian #### American Community Survey 2008-2012 (5-year)	df[geo+'B02001005E'] / df[geo+'B02001001E'] 
 
# ACS 2008-2012 Percent Unemployed Variables

#### **t10pcunemp**
Percent population 16 years and over who are civilians in the labor force that are unemployed

--- 

#### Percent population 16 years and over who are civilians in the labor force that are unemployed#### American Community Survey 2008-2012 (5-year)	( df[geo+'B23001008E'] + df[geo+'B23001015E'] + df[geo+'B23001022E'] + df[geo+'B23001029E'] + df[geo+'B23001036E'] + df[geo+'B23001043E'] + df[geo+'B23001050E'] + df[geo+'B23001057E'] + df[geo+'B23001064E'] + df[geo+'B23001071E'] + df[geo+'B23001076E'] + df[geo+'B23001081E'] + df[geo+'B23001086E'] + df[geo+'B23001094E'] + df[geo+'B23001101E'] + df[geo+'B23001108E'] + df[geo+'B23001115E'] + df[geo+'B23001122E'] + df[geo+'B23001129E'] + df[geo+'B23001136E'] + df[geo+'B23001143E'] + df[geo+'B23001150E'] + df[geo+'B23001157E'] + df[geo+'B23001162E'] + df[geo+'B23001167E'] + df[geo+'B23001172E'] ) / df[geo+'B23001001E'] 
 
# Count Homicide 2003-2011/08 - NY Times Variables

#### **t10muc0311**
Count Homicide 2003-2011/08 - NY Times

--- 

 
 
# Bike Routes Length Variables

#### **t10birtlen**
Bike Routes Length in meters

--- 

 
 
# Pedestrians Killed 1995-2013 Variables

#### **t10pek9513**
Pedestrians Killed 1995-2013

--- 

 
 
# Pedestrians Injured 1995-2013 Variables

#### **t10pei9513**
Pedestrians Injured 1995-2013

--- 

 
 
# Bicyclists Killed 1995-2013 Variables

#### **t10bik9513**
Bicyclists Killed 1995-2013

--- 

 
 
# Bicyclists Injured 1995-2013 Variables

#### **t10bii9513**
Bicyclists Injured 1995-2013

--- 

 
 
# Count Sidewalk Cafes - 2013/06 Variables

#### **t10cntcafe**
Count Sidewalk Cafes from Open Data Table released June 21, 2013

--- 

 
 