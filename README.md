<h1 align = "center"><b>CHAPSTONE PROJECT III</b></h1><br>
<h1 align = "center"><b>TELCO CUSTOMER CHURN</b></h1><br>

<p align="center">
  <img width="800" height="300" src="https://github.com/AlfiAlfian/Capstone_Project_III_Machine_Learning/blob/main/image/churn_illustration.png">
</p>

<h1 class="list-group-item list-group-item-action active" data-toggle="list" role="tab" aria-controls="home">TABLE OF CONTENT</h1>

<a id="toc"></a>

[1. BUSINESS PROBLEM UNDERSTANDING](#1)<br><br>
[2. LIBRARY](#2)<br>
&nbsp;&nbsp;&nbsp;&nbsp;[2.1. PYTHON LIBRARY](#2.1)<br><br>
[3. DATA UNDERSTANDING](#3)<br>
&nbsp;&nbsp;&nbsp;&nbsp;[3.1. FEATURE CHECK](#3.1)<br>
&nbsp;&nbsp;&nbsp;&nbsp;[3.2. FEATURE CORRELATION](#3.2)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[3.2.1. NUMERICAL FEATURE WITH TARGET](#3.2.1)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[3.2.2. CATEGORICAL FEATURE WITH TARGET](#3.2.2)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[3.2.3. ALL FEATURE WITH TARGET](#3.2.3)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[3.2.4. CURRENT CONCLUSION ABOUT OUR DATA](#3.2.4)<br><br>
[4. MACHINE LEARNING](#4)<br>
&nbsp;&nbsp;&nbsp;&nbsp;[4.1. DATA PREPARATION](#4.1)<br>
&nbsp;&nbsp;&nbsp;&nbsp;[4.2. BASE MODEL EVALUATION](#4.2)<br>
&nbsp;&nbsp;&nbsp;&nbsp;[4.3. BASE MODEL WITH OVERSAMPLING - SMOTENC](#4.3)<br>
&nbsp;&nbsp;&nbsp;&nbsp;[4.4. BASE MODEL WITH UNDERSAMPLING - RANDOM UNDER SAMPLING](#4.4)<br>
&nbsp;&nbsp;&nbsp;&nbsp;[4.5. BASE MODEL OUTPUT RECAP](#4.5)<br><br>
&nbsp;&nbsp;&nbsp;&nbsp;[4.6. HYPERPARAMETER TUNING](#4.6)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[4.6.1. HYPERPARAMETER TUNING - LOGISTIC REGRESSION](#4.6.1)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[4.6.2. HYPERPARAMETER TUNING - GRADIENTBOOSTCLASSIFIER](#4.6.2)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[4.6.3. HYPERPARAMETER TUNING OUTPUT RECAP](#4.6.3)<br>

&nbsp;&nbsp;&nbsp;&nbsp;[4.7. FEATURE IMPORTANCE & FEATURE SELECTION](#4.7)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[4.7.1. BEST MODEL WITH CURRENT FEATURE](#4.7.1)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[4.7.2. BEST MODEL WITH SELECTED FEATURE](#4.7.2)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[4.7.3. RECAP FOR FEATURE IMPORTANCE & FEATURE SELECTION](#4.7.3)<br><br>
[5. CONCLUSSION](#5)<br>
[6. RECOMMENDATION](#6)<br>
[7. DEPLOYMENT](#7)<br>

---

<a id="1"></a>
<font color="lightseagreen" size=+3><b>1. BUSINESS PROBLEM UNDERSTANDING</b></font>

<a href="#toc" class="btn btn-primary btn-sm" role="button" aria-pressed="true" 
style="color:white" data-toggle="popover">Table of Contents</a>

* Pada bagian ini saya menjelaskan beberapa hal sebagai berikut : 
    * Apa itu *Churn* penyebab dan dampaknya
    * Mendefinisikan beberapa hal seperti *Problem Statement*, * *Variables*, *Objectives*, *Action*, *Values* dan *Confussion Matrix*<br><br>
    
<a id="2"></a>
<font color="lightseagreen" size=+3><b>2. LIBRARY</b></font>

<a href="#toc" class="btn btn-primary btn-sm" role="button" aria-pressed="true" 
style="color:white" data-toggle="popover">Table of Contents</a>
* Berisikan Python Library yang digunakan pada Notebook ini<br><br>

<a id="3"></a>
<font color="lightseagreen" size=+3><b>3. DATA UNDERSTANDING</b></font>

<a href="#toc" class="btn btn-primary btn-sm" role="button" aria-pressed="true" 
style="color:white" data-toggle="popover">Table of Contents</a>
* Pada bagian ini berisikan Explanatory dan Exploratory Data Analysis<br><br>

<a id="4"></a>
<font color="lightseagreen" size=+3><b>4. MACHINE LEARNING</b></font>

<a href="#toc" class="btn btn-primary btn-sm" role="button" aria-pressed="true" 
style="color:white" data-toggle="popover">Table of Contents</a>
* Pada bagian ini berisikan beberapa tahapan pemodelan sebagai berikut : 
    * Model dasar
    * Model dasar + resampling method
    * Hyperparameter Tuning
    * Feature Importance & Feature Selection<br><br>
    
<a id="5"></a>
<font color="lightseagreen" size=+3><b>5. CONCLUSION</b></font>

<a href="#toc" class="btn btn-primary btn-sm" role="button" aria-pressed="true" 
style="color:white" data-toggle="popover">Table of Contents</a>

* Pada bagian ini berisikan beberapa kesimpulan dari data dan model yang telah dibuat pada tahap sebelumnya
* Kemudian ada juga menjelaskan mengenai classification report yang digenerate agar outputnya lebih *measureable*<br><br>

<a id="6"></a>
<font color="lightseagreen" size=+3><b>6. RECOMMENDATION</b></font>

<a href="#toc" class="btn btn-primary btn-sm" role="button" aria-pressed="true" 
style="color:white" data-toggle="popover">Table of Contents</a>

* Bagian ini berisikan hal hal yang dapat dilakukan TELCO dilihat dari data yang telah kita analisa.
* Beberapa *improvement* yang dapat dilakukan pada pemodelan yang telah saya lakukan.<br><br>

<a id="7"></a>
<font color="lightseagreen" size=+3><b>7. DEPLOYMENT</b></font>

<a href="#toc" class="btn btn-primary btn-sm" role="button" aria-pressed="true" 
style="color:white" data-toggle="popover">Table of Contents</a>

* Deployment Model mengguankan Pickle
* Pengujian dengan menggunakan data test mandiri.
