# ONET Occupation Codes

To explore the question of flexibility, the inherent properties of occupations should be considered. To do this, I use data from O\*Net to build an index of flexibility for a particular occupation. However, the O\*Net database uses the Standard Occupation Classification (SOC) Code, updated annually, while the CPS and ATUS use the 2010 Census Occupation Classification Codes. 

Linking the occupation codes requires utilizing the Crosswalk (https://www2.census.gov/programs-surveys/demo/guidance/industry-occupation/2018-occupation-code-list-and-crosswalk.xlsx). The design of the Crosswalk between 2018 SOC and 2010 Census is not friendly to easy linking. 

In order to use the Crosswalk to link the 2018 SOC with the 2010 Census, we must first extract some codes from the 2018 Census Title column, fill in empty cells (imported as NaN), create a dictionary, and append the 2010 Census codes to some O\*Net data. 

With the final .csv, we can merge the CPS/ATUS data with the O\*Net job characteristics via the 2010 Census occupation code. 
