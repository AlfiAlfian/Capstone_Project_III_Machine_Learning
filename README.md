<h1 align = "center"><b>CAPSTONE PROJECT III<br>TELCO CUSTOMER CHURN</b></h1><br>

<p align="center">
  <img width="600" src="https://github.com/AlfiAlfian/Capstone_Project_III_Machine_Learning/blob/main/image/churn_illustration.png">
</p>

<a id="toc"></a>

<h1 class="list-group-item list-group-item-action active" data-toggle="list" role="tab" aria-controls="home">FOR BETTER EXPERIENCE</h1>

Before continuing any further, please run cell code available in this section. Only this section only. No need to run the whole notebook

***Notes***
* Sorry that this notebook explanation is in bahasa, but figure and graphs are all in English. Hope you can still learn something.
* I'll make it in English Version later. So Stay Tuned. 
* Hyperlink that I made might not work well with several nbextension like `table of content`
* Others might also causing the issue, but uncheck the `table of content` does the job for me.
* Running the whole notebook take me 30 - 50 minutes

<h1 class="list-group-item list-group-item-action active" data-toggle="list" role="tab" aria-controls="home">TABLE OF CONTENT</h1>

<a id="toc"></a>

[1. BUSINESS PROBLEM UNDERSTANDING](#1)<br><br>
[2. LIBRARY](#2)<br>
&nbsp;&nbsp;&nbsp;&nbsp;2.1. PYTHON LIBRARY<br>

[3. DATA UNDERSTANDING](#3)<br>
&nbsp;&nbsp;&nbsp;&nbsp;3.1. FEATURE CHECK<br>
&nbsp;&nbsp;&nbsp;&nbsp;3.2. FEATURE CORRELATION<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.2.1. NUMERICAL FEATURE WITH TARGET<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.2.2. CATEGORICAL FEATURE WITH TARGET<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.2.3. ALL FEATURE WITH TARGET<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.2.4. CURRENT CONCLUSION ABOUT OUR DATA<br><br>
[4. MACHINE LEARNING](#4)<br>
&nbsp;&nbsp;&nbsp;&nbsp;4.1. DATA PREPARATION<br>
&nbsp;&nbsp;&nbsp;&nbsp;4.2. BASE MODEL EVALUATION<br>
&nbsp;&nbsp;&nbsp;&nbsp;4.3. BASE MODEL WITH OVERSAMPLING - SMOTENC<br>
&nbsp;&nbsp;&nbsp;&nbsp;4.4. BASE MODEL WITH UNDERSAMPLING - RANDOM UNDER SAMPLING<br>
&nbsp;&nbsp;&nbsp;&nbsp;4.5. BASE MODEL OUTPUT RECAP<br><br>
&nbsp;&nbsp;&nbsp;&nbsp;4.6. HYPERPARAMETER TUNING<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.6.1. HYPERPARAMETER TUNING - LOGISTIC REGRESSION<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.7.1. HYPERPARAMETER TUNING - GRADIENTBOOSTCLASSIFIER<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.8.1. HYPERPARAMETER TUNING OUTPUT RECAP<br>

&nbsp;&nbsp;&nbsp;&nbsp;4.7. FEATURE IMPORTANCE & FEATURE SELECTION<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.7.1. BEST MODEL WITH CURRENT FEATURE<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.7.2. BEST MODEL WITH SELECTED FEATURE<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.7.3. RECAP FOR FEATURE IMPORTANCE & FEATURE SELECTION<br><br>
[5. CONCLUSSION](#5)<br>
[6. RECOMMENDATION](#6)<br>
[7. DEPLOYMENT](#7)

---

<a id="1"></a>
<h2 class="list-group-item list-group-item-action active" data-toggle="list" role="tab" aria-controls="home">1. BUSINESS PROBLEM UNDERSTANDING</h2>

<a href="#toc" class="btn btn-primary btn-sm" role="button" aria-pressed="true" 
style="color:white" data-toggle="popover">Table of Contents</a>

* Explaining what is Churn, Why Churn Happen, Churn impact for the company.
* Define Problem Statement, Variables, Objectives, Action, Value
* Explaining confussion matrix and what metrics to use<br><br>

<a id="2"></a>
<h2 class="list-group-item list-group-item-action active" data-toggle="list" role="tab" aria-controls="home">2. LIBRARY</h2>

<a href="#toc" class="btn btn-primary btn-sm" role="button" aria-pressed="true" 
style="color:white" data-toggle="popover">Table of Contents</a>

Library that will be used in this notebook and defined function<br><br>

<a id="3"></a>
<h2 class="list-group-item list-group-item-action active" data-toggle="list" role="tab" aria-controls="home">3. DATA UNDERSTANDING</h2>

<a href="#toc" class="btn btn-primary btn-sm" role="button" aria-pressed="true" 
style="color:white" data-toggle="popover">Table of Contents</a>

* Explain the data in general
* Checking for anomalies, missing values and adjustment for Modelling
* Explanatory Data Analysis
* Correlation between features & target
* Conclusion based on the data<br><br>

<a id="4"></a>
<h2 class="list-group-item list-group-item-action active" data-toggle="list" role="tab" aria-controls="home">4. MACHINE LEARNING</h2>

<a href="#toc" class="btn btn-primary btn-sm" role="button" aria-pressed="true" 
style="color:white" data-toggle="popover">Table of Contents</a>

* Data Preparataion
* Base Model Result (CV & Test)
* Base Model + Resampling Result (CV & Test)
* There's 2 best model, Logistic Regression & GradientBoost.
* Output Recap for Hyperparameter Tuning
* Choose Best Model based on Output Recap
* Feature Importance
* Compare Best Model with selected feature & Model with all feature<br><br>

<a id="5"></a>
<h2 class="list-group-item list-group-item-action active" data-toggle="list" role="tab" aria-controls="home">5. CONCLUSION</h2>

<a href="#toc" class="btn btn-primary btn-sm" role="button" aria-pressed="true" 
style="color:white" data-toggle="popover">Table of Contents</a>

* Conclusion about my data
* Conclusion for Machine Learning Model
* Classification Report Intepretation (My Model can be used ?)<br><br>

<a id="6"></a>
<h2 class="list-group-item list-group-item-action active" data-toggle="list" role="tab" aria-controls="home">6. RECOMMENDATION</h2>

<a href="#toc" class="btn btn-primary btn-sm" role="button" aria-pressed="true" 
style="color:white" data-toggle="popover">Table of Contents</a>

* Giving TELCO some recommendation based on findings (if you're asked what should we (TELCO) do as a consultant. Sorry might be kinda bias)
* Several things that can be done in the future for model improvement<br><br>

<a id="7"></a>
<h2 class="list-group-item list-group-item-action active" data-toggle="list" role="tab" aria-controls="home">7. DEPLOYMENT</h2>

<a href="#toc" class="btn btn-primary btn-sm" role="button" aria-pressed="true" 
style="color:white" data-toggle="popover">Table of Contents</a>

* `Before Continuing Any Further`
* Hyperparameter tuning for model with selected feature but 100% data training. (For all process I do above, I'm still using 80% data train, I use the other 20% to validate my model)
* Compare the CV result and bestparameter
* Deployment Prep
  * Which feature to use
  * Deploy Model in Pickle
  * (template to predict) Load Pickle Model
  * (template to predict) Data Preparation
  * (template to predict) Predict with data test

***To Predict with Pickle, Notes***
* Please adjust categorical value for internetservice & contract with the one I'll give in the notebook
* Please check notebook for more details
