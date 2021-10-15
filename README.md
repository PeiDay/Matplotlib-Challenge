# Matplotlib - The Power of Plots :mouse2:

## Background

Pymaceuticals Inc., a burgeoning pharmaceutical company based out of San Diego. Pymaceuticals specializes in anti-cancer pharmaceuticals. In its most recent efforts, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.

With the access to the complete data from their most recent animal study. In this study, 249 mice identified with SCC tumor growth were treated through a variety of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals' drug of interest, Capomulin, versus the other treatment regimens. We are generating all of the tables and figures needed for the technical report of the study and a top-level summary of the study results.

The **Mouse_metadata** csv file contains `Mouse ID`,`Drug Regimen`, `Sex`, `Age_months`, and `Weight (g)`; the **Study_Result** csv file contains `Mouse ID`, `Timepoint`, `Tumor Volume (mm3)`, and `Metastatic Sites`. 

![Laboratory]()

## Drug regimens and Tumor volume study

Merge the given data from two csv files. In order to get clean data, we started from identifying and removing the duplicate entries. The following inforamtion are based on the clean data:

* Summary statistics table consisting of the mean, median, variance, standard deviation, and SEM of the tumor volume for each drug regimen.

* Drug Regimen bar plot shows the total number of timepoints for all mice tested for each drug regimen throughout the course of the study:

![Drug regimen by pyplot]()

* Mice Gender pie plot shows the distribution of female or male mice in the study:

![Mice gender by pyplot]()

* Calculate the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin.  Identify any potential outliers across all four treatment regimens by calculating the quartiles, IQR, and quantitatively. The result is presented by the Final tumor volumn boxplot:

![Final tumor volume boxplot]

* Randomly select a mouse that was treated with Capomulin and generate a line plot of tumor volume vs. time point for that mouse. **Outcome various due to the ramdom selection**
    * In order to observe the Capomulin treatment influence on tumor volume vs. time point, I selected  a sample size of 5 mice:  

![Samples Time vs Vol line plot]

* The correlation coefficient and linear regression model between mouse weight and average tumor volume for the Capomulin treatment.  The linear regression model and Capomulin treatment regimen tumor volume versus mouse weight scatter plot:

![Weight vs Vol scatter plot]
![Linear regression model]

## Observations or inferences:
    This is also included at the top of notebook.

* There are **10 drug regimen** treatments in the study. The highest number of study is treated by Capomulin, the lowest number of study is treated by Propriva. This study is more focused toward **Capomulin regimen** compared to other treatments. 

* There are more male mice treated than female mice. However, the statistics shows **less than 1%** difference. Gender might not be the significant variable to the study.

* When we narrow down the drug regimen, final tumor volume treated by **Capomulin and Ramicane** tend to have lower number than the others. Ramicane seems to have lower final tumor volume. However, the number of mice treated by Ramicane is slightly less than Capomulin. In order to get more accurate study and conclusion, the treatment of both regimens might be continued with the same number of mice.

* Random select a Mouse ID can see the example of mouse treated by Capomulin.  In order to have a better understanding of the Capomulin treatment affect the tumor volume.  The samples line chart of 5 mice treated in the same regimen shows **the Capomulin could reduce the size of tumor volumn**.

* The correlation coefficient between the average weight and the final tumor volumn is **0.84**, that indicates **high positive correlation** between the weight and tumor volume. In addition, the r-squared **0.71** could infer that the final tumor volume could be predictable by using average weight of mouse.
