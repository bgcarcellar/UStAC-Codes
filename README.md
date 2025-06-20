# UStAC-Codes
This repository contains the codes in data scraping CRS for UStAC purposes


How to run:
1. Open bs_ge_courses_demand_report notebook. Open it in Google Colab
2. Prepare two input files
   
   a. Curriculum JSON File - json file describing the prerequisites of courses in a curriculum
   b. Student Profile File - Can be extracted from CRS (delete the first few rows until the first row is the column name). Can be multiple semesters.
   
4. Run the codes sequentially
   
   a. installing of colab-selenium
   b. grades extractor codes for default classes
   c. demand generation - scraping sample output
![image](https://github.com/user-attachments/assets/92d2b3ca-051a-422b-a290-98cc6ff14ba4)
      Please check kung meron pang piniprint yung code. ang piniprint nyang student numbers ay yung mga student numbers na di niya na scrape properly (maybe due to bandwidht issues,
   or limits ng pagscrape. Nabibilisan masyado yung crs data kung automated masyado hehe.) So kelangan po icheck kung madami pa yung mga piniprint ng code. Sometimes, yung mga students
   ay nagshift out na so magfafail talaga sya mag scrape kasi di na covered ng dge crs account. So ok lang talaga na meron kayong makitang nagpiprint na student number
   d. Extra Scraping code: Pag may mga students pa rin na piniprint pero ge students, run pa rin etong extra scraping code
6.  
