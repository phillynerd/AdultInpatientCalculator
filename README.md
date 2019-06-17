# Adult Inpatient Calculator

This is similar in concept to the FBS calculator, only the output was a bit fancier.  Clinical wanted a way to assess the risk of readmission and the risk of a long length of stay for members at the time of admission.  Logistic regressions were used to create the model, and those models fed the calculator as proof of concept.  

Info on files used to create the model: 
1. Datasource for model: DC in 2013 - 2016, using 30 day readmission as outcome for AR440 stored procedure (precursor to uspTieringTemplateAnalysis, specific to 100.001, 100.004 & adults)

File associated with this project (not all of which are uploaded here)

1. LOSReadmCalc.xlsx - Baseline data produced from AR440 stored procedure; plus all manipulations prior to R code <font color = "red">(not provided, HIPAA)</font>

2. AR5294 AIP LOS and Readmit Calculator - R syntax (this file reads AIPcalc.csv, which is a sheet taken from file #1 and saved as csv)
    - The code in this file mirrors the calculator created for FBS; there are probably some comments and sections that I never removed especially since this project ended up not moving forward after a quick POC. 

3. LogitLOS.csv; LogitReadm.csv - R outputs of model coefficients, generated within code above <font color = "red">(not provided)</font>

4. AR 5294 AIPpred.xlsx - Accuracy/precision/etc assessed on predicted values output by R syntax file in step 2 <font color = "red">(not provided, HIPAA)</font>

5. AR5294 AIP Risk Calculator.xlsm Final calculator
