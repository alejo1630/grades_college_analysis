# Whatsapp Chat Analysis

A Jupyter Notebook with the analysis and prediction of Final Grades (Pass/Fail) for students of mechatronics engineering in several mechanic courses.


## 🔰 How does it work?

The dataset contains the grade records for several students of the Mechatronics Engineering Program from 2020 to 2023. Each semesters is splitted into three periods (G1, G3, G3). The Final Grade (FG) is calculated based on the grades from each period using the following equation:

$$ FG = 0.3G_1 + 0.3G_3 + 0.4G_3$$

The grade scale ranges from **0.00** to **5.00**. 

A student approves a class if $FG \geq 3.00$

All classes belong to the mechanic area of the program. This Mechatronics Engineering Program has a duration 10 semesters (5 years)

### Feature description

- **ID**: Student's ID, which increases according to its starting year
- **Sex**: Student's sex (M: Male, F: Female)
- **Class**: Class name
    - Material Science
    - Mechanic of Materials
    - Applied Dynamics
    - Fluid Mechanics
    - Thermofluids
    - Material Selection
    - Forensic Engineering
- **Semester**: Semester in which the class is taught
    - 3
    - 5
    - 6
    - 8
    - 9
- **Year**: Year of the record
- **Type**: Type of semester
    - Spring
    - Fall
- **G1**: Grades for the first period of the semester
- **G2**: Grades for the second period of the semester
- **G3**: Grades for the third period of the semester
- **FG**: Final Grades

### EDA
Several data analysis were performed such as:
- Proportion Male and Female students
- Students dristibtion per classes, year, type of semester
- Grades Distribution per period and final grade
- Create a column for the College Level for each class based on the credit hours
  1. **freshmen**: 0–30 hours
  3. **sophomore**: 31–60 hours
  3. **junior**: 61–90 hours
  4. **senior**: 90+ hours
- Pandemic performance comparison
- Pass/Fail rate

In addition, some question were proposed:
1. How has the female proportion changed for each semester?
2. Has the number of women increased in the recent generations?
3. Who has had a better performance?
4. Performance Before and After Pandemic

### Predictive Models
#### *Regression Models*
**6** regression models were compared based on the Final Grade, using cross-validation, recursive feature elimination (RFE), and **R2-Score** as a metric:
- Linear Regression
- Ridge Regression
- Lasso Regression
- Support Vector Regression (SVR)
- Random Forest Regression
- Polynomial Regression
  
*The best regression model was **Linear Regression** with a predictive score above **80%***

<img src = "https://raw.githubusercontent.com/alejo1630/grades_college_analysis/main/Images/Regression.png" width = "500">

#### *Binary Classification Models*
**3** binary classification models were compared based on the classes Pass or Fail, using cross-validation, recursive feature elimination (RFE), and **F1 weighted-Score** as a metric and **confussion matrix**:
- Logistic Regression
- Support Vector Classifier (SVC)
- Random Forest Classifier

*The best regression model was **Logistic Regression** with a predictive score above **90%***

<img src = "https://raw.githubusercontent.com/alejo1630/grades_college_analysis/main/Images/Classification.png" width = "500">
