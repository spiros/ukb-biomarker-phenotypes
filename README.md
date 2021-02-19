

# A semi-supervised approach for rapidly creating clinical biomarker phenotypes in the UK Biobank, across different primary care EHR and clinical terminology systems.

The UK Biobank is making [primary care electronic health records](http://biobank.ctsu.ox.ac.uk/crystal/crystal/docs/primary_care_data.pdf) available for the entire cohort for [COVID-19 research](https://www.ukbiobank.ac.uk/2020/04/covid/). This repository provides machine-readable versions (CSV files) of electronic health record phenotyping algorithms for 31 commonly-measured biomakers, many of which are associated with COVID-19 comorbidities such as body mass index, cardiovascular disease and respiratory disease.

Details on how these algorithms were bootstrapped and validated can be found in the [publication](https://doi.org/10.1093/jamiaopen/ooaa047):

    Spiros Denaxas, Anoop D Shah, Bilal A Mateen, Valerie Kuan, Jennifer K Quint, Natalie Fitzpatrick, Ana Torralbo, Ghazaleh Fatemifar, Harry Hemingway, A semi-supervised approach for rapidly creating clinical biomarker phenotypes in the UK Biobank using different primary care EHR and clinical terminology systems, JAMIA Open, Volume 3, Issue 4, December 2020, Pages 545–556, https://doi.org/10.1093/jamiaopen/ooaa047



# Phenotypes 



Phenotype | Category | Units | Definition | Download | 
----------|----------|-------|------------|----------|
| [Glucose](#Glucose) | Blood biochemistry | mmol/L | Blood-based glucose level derived from plasma. Excludes fasting measurements. | [Glucose.csv](Glucose.csv) 
| [Triglycerides](#Triglycerides) | Blood biochemistry | mmol/L | Serum triglycerides measurements. Algorithm excludes plasma-derived measurements. Includes fasting/non-fasting/random values. | [Triglycerides.csv](Triglycerides.csv) 
| [HDL](#HDL) | Blood biochemistry | mmol/L | Serum fasting/non-fasting/random HDL cholesterol level. | [HDL.csv](HDL.csv) 
| [HbA1c](#HbA1c) | Blood biochemistry | mmol/mol | HbA1c level recorded using International Federation of Clinical Chemistry and Laboratory Medicine or Diabetes Control and Complications Trial (DCCT). | [HbA1c.csv](HbA1c.csv) 
| [Creatinine](#Creatinine) | Blood biochemistry | umol/L | Creatinine levels including corrected levels. Algorithm includes serum, plasma, and unspecified source measurements. | [Creatinine.csv](Creatinine.csv) 
| [Cholesterol](#Cholesterol) | Blood biochemistry | mmol/L | Serum cholesterol measurent including total cholesterol measurements but excluding plasma-derived measurements. The phenotype includes fasting and non-fasting measurements. | [Cholesterol.csv](Cholesterol.csv) 
| [Calcium](#Calcium) | Blood biochemistry | mmol/L | Serum calcium measurement. Excludes ionized calcium level measurements. The phenotype does not include corrected/adjusted levels. | [Calcium.csv](Calcium.csv) 
| [CRP](#CRP) | Blood biochemistry | mg/L | Serum C reactive protein level excluding plasma-derived measurements. | [CRP.csv](CRP.csv) 
| [ALT](#ALT) | Blood biochemistry | U/L | Serum alanine aminotransferase level | [ALT.csv](ALT.csv) 
| [ALP](#ALP) | Blood biochemistry | U/L | Serum alkaline phosphatase measurement excluding liver isoenzyme level. | [ALP.csv](ALP.csv) 
| [Total bilirubin](#Totalbilirubin) | Blood biochemistry | umol/L | Serum bilirubin level. Excludes conjugated bilirubin levels. | [Totalbilirubin.csv](Totalbilirubin.csv) 
| [Urea](#Urea) | Blood biochemistry | mmol/L | Serum / plasma urea level | [Urea.csv](Urea.csv) 
| [Albumin](#Albumin) | Blood biochemistry | g/L | Serum albumin levels. | [Albumin.csv](Albumin.csv) 
| [Haemoglobin conc](#Haemoglobinconc) | Blood count | g/dL | Haemoglobin estimation | [Haemoglobinconc.csv](Haemoglobinconc.csv) 
| [MCV](#MCV) | Blood count | fL | Mean corpuscular volume (MCV) | [MCV.csv](MCV.csv) 
| [WBC](#WBC) | Blood count | 10^9/L | Total white cell count. Excludes polymorphonuclear leukocyte count. | [WBC.csv](WBC.csv) 
| [MCHb conc](#MCHbconc) | Blood count | g/dL | Mean corpusc. Hb. conc. (MCHC) | [MCHbconc.csv](MCHbconc.csv) 
| [Haematocrit perc](#Haematocritperc) | Blood count | % | Haematocrit / packed cell volume | [Haematocritperc.csv](Haematocritperc.csv) 
| [Basophills](#Basophills) | Blood count | 10^9/L | Basophil count | [Basophills.csv](Basophills.csv) 
| [RBC](#RBC) | Blood count | 10^12/L | Red blood cell (RBC) count excluding nucleated RBC values. | [RBC.csv](RBC.csv) 
| [Platelets](#Platelets) | Blood count | 10^9/L | Platelet count. Excludes platelet distribution width measurements. | [Platelets.csv](Platelets.csv) 
| [Neutrophills](#Neutrophills) | Blood count | 10^9/L | Neutrophil count | [Neutrophills.csv](Neutrophills.csv) 
| [Monocytes](#Monocytes) | Blood count | 10^9/L | Monocyte count | [Monocytes.csv](Monocytes.csv) 
| [Lymphocytes](#Lymphocytes) | Blood count | 10^9/L | Leucocyte count | [Lymphocytes.csv](Lymphocytes.csv) 
| [Eosinophills](#Eosinophills) | Blood count | 10^9/L | Eosinophil count | [Eosinophills.csv](Eosinophills.csv) 
| [Height](#Height) | Physical measures | cm | Height | [Height.csv](Height.csv) 
| [FVC](#FVC) | Physical measures | L | Forced vital capacity measurement. Excludes predictd values and measurements post-bronchodialation. | [FVC.csv](FVC.csv) 
| [SBP](#SBP) | Physical measures | mmHg | Systolic blood pressure. | [SBP.csv](SBP.csv) 
| [DBP](#DBP) | Physical measures | mmHg | Diastolic blood pressure. | [DBP.csv](DBP.csv) 
| [Weight](#Weight) | Physical measures | Kg | Weight | [Weight.csv](Weight.csv) 
| [FEV1](#FEV1) | Physical measures | L | Forced expired volume in 1 second. Excludes predicted values and measurements post-bronchodialation. | [FEV1.csv](FEV1.csv) 


## ALP <a name='ALP'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | ALP |
| Category | Blood biochemistry
| Type | Biomarker |
| UK Biobank field | [30610](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=30610) |
| Units | U/L ([UO_0000179](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0000179))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 11|
| Definition | Serum alkaline phosphatase measurement excluding liver isoenzyme level. |
| Version | alpha | 



### Implementation 


```
IF Read v2 code = read_2
    IF data_provider = England Vision (1) OR data provider = Wales (4)
        ALP = value1

    ELSE IF data_provider = Scotland (2)
        ALP = value2
        units = value3

ELSE IF CTV3 code = read_3 
    IF data_provider = England TPP (3)
        ALP = value1
```
    


| Terminology   | Read code   | Read term                        |
|---------------|-------------|----------------------------------|
| read2         | 44F..00     | Serum alkaline phosphatase       |
| read2         | 44F3.00     | Total alkaline phosphatase       |
| read2         | 44FZ.00     | Serum alkaline phosphatase NOS   |
| read2         | 44F1.00     | Serum alk. phos. normal          |
| read2         | 44F2.00     | Serum alk. phos. raised          |
| ctv3          | XE2px       | Serum alkaline phosphatase       |
| ctv3          | XE2px       | Serum alkaline phosphatase level |
| ctv3          | 44F3.       | Alkaline phosphatase level       |
| ctv3          | 44FZ.       | Serum alkaline phosphatase NOS   |
| ctv3          | 44F1.       | Serum alk. phos. normal          |
| ctv3          | 44F2.       | Serum alk. phos. raised          |

<hr>

## ALT <a name='ALT'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | ALT |
| Category | Blood biochemistry
| Type | Biomarker |
| UK Biobank field | [30620](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=30620) |
| Units | U/L ([UO_0000179](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0000179))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 11|
| Definition | Serum alanine aminotransferase level |
| Version | alpha | 



### Implementation 


```
IF Read v2 code = read_2
    IF data_provider = England Vision (1) OR data provider = Wales (4)
        ALT = value1

    ELSE IF data_provider = Scotland (2)
        ALT = value2
        units = value3

ELSE IF CTV3 code = read_3 
    IF data_provider = England TPP (3)
        ALT = value1
```
    


| Terminology   | Read code   | Read term                            |
|---------------|-------------|--------------------------------------|
| read2         | 44G3.00     | ALT/SGPT serum level                 |
| read2         | 44GB.00     | Serum alanine aminotransferase level |
| read2         | 44G..11     | ALT - blood level                    |
| read2         | 44G3000     | ALT/SGPT level normal                |
| read2         | 44G3100     | ALT/SGPT level abnormal              |
| ctv3          | 44G3.       | ALT/SGPT serum level                 |
| ctv3          | XaLJx       | Serum alanine aminotransferase level |
| ctv3          | X771f       | ALT - blood level                    |
| ctv3          | X771e       | SGPT - blood level                   |
| ctv3          | 44G30       | ALT.SGPT level normal                |
| ctv3          | 44G31       | ALT.SGPT level abnormal              |

<hr>

## Albumin <a name='Albumin'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | Albumin |
| Category | Blood biochemistry
| Type | Biomarker |
| UK Biobank field | [30600](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=30600) |
| Units | g/L ([UO_0000175](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0000175))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 7|
| Definition | Serum albumin levels. |
| Version | alpha | 



### Implementation 


```
IF Read v2 code = read_2
    IF data_provider = England Vision (1) OR data provider = Wales (4)
        Albumin = value1

    ELSE IF data_provider = Scotland (2)
        Albumin = value2
        units = value3

ELSE IF CTV3 code = read_3 
    IF data_provider = England TPP (3)
        Albumin = value1
```
    


| Terminology   | Read code   | Read term            |
|---------------|-------------|----------------------|
| read2         | 44M4.00     | Serum albumin        |
| read2         | 44M4000     | Serum albumin normal |
| read2         | 44M4100     | Serum albumin low    |
| ctv3          | XE2eA       | Serum albumin        |
| ctv3          | XE2eA       | Serum albumin level  |
| ctv3          | 44M40       | Serum albumin normal |
| ctv3          | 44M41       | Serum albumin low    |

<hr>

## Basophills <a name='Basophills'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | Basophills |
| Category | Blood count
| Type | Biomarker |
| UK Biobank field | [30160](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=30160) |
| Units | 10^9/L ([UO_0000317](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0000317))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 8|
| Definition | Basophil count |
| Version | alpha | 



### Implementation 


```
IF Read v2 code = read_2
    IF data_provider = England Vision (1) OR data provider = Wales (4)
        Basophills = value1

    ELSE IF data_provider = Scotland (2)
        Basophills = value2
        units = value3

ELSE IF CTV3 code = read_3 
    IF data_provider = England TPP (3)
        Basophills = value1
```
    


| Terminology   | Read code   | Read term               |
|---------------|-------------|-------------------------|
| read2         | 42L..00     | Basophil count          |
| read2         | 42LZ.00     | Basophil count NOS      |
| read2         | 42L1.00     | Basophil count normal   |
| ctv3          | 42L..       | Basophil count          |
| ctv3          | 42LZ.       | Basophil count NOS      |
| ctv3          | 42L1.       | Basophil count normal   |
| read2         | 42L3.00     | Basophil count abnormal |
| read2         | 42L2.00     | Basophilia              |

<hr>

## CRP <a name='CRP'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | CRP |
| Category | Blood biochemistry
| Type | Biomarker |
| UK Biobank field | [30710](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=30710) |
| Units | mg/L ([UO_0000273](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0000273))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 6|
| Definition | Serum C reactive protein level excluding plasma-derived measurements. |
| Version | alpha | 



### Implementation 


```
IF Read v2 code = read_2
    IF data_provider = England Vision (1) OR data provider = Wales (4)
        CRP = value1

    ELSE IF data_provider = Scotland (2)
        CRP = value2
        units = value3

ELSE IF CTV3 code = read_3 
    IF data_provider = England TPP (3)
        CRP = value1
```
    


| Terminology   | Read code   | Read term                      |
|---------------|-------------|--------------------------------|
| read2         | 44CS.00     | Serum C reactive protein level |
| read2         | 44CC000     | C reactive protein normal      |
| read2         | 44CC100     | C reactive protein abnormal    |
| ctv3          | XaINL       | Serum C reactive protein level |
| ctv3          | 44CC0       | C-reactive protein normal      |
| ctv3          | 44CC1       | C-reactive protein abnormal    |

<hr>

## Calcium <a name='Calcium'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | Calcium |
| Category | Blood biochemistry
| Type | Biomarker |
| UK Biobank field | [30680](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=30680) |
| Units | mmol/L ([UO_0010003](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0010003))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 7|
| Definition | Serum calcium measurement. Excludes ionized calcium level measurements. The phenotype does not include corrected/adjusted levels. |
| Version | alpha | 



### Implementation 


```
IF Read v2 code = read_2
    IF data_provider = England Vision (1) OR data provider = Wales (4)
        Calcium = value1

    ELSE IF data_provider = Scotland (2)
        Calcium = value2
        units = value3

ELSE IF CTV3 code = read_3 
    IF data_provider = England TPP (3)
        Calcium = value1
```
    


| Terminology   | Read code   | Read term                            |
|---------------|-------------|--------------------------------------|
| read2         | 44I8.00     | Serum calcium                        |
| read2         | 44I8000     | Normal serum calcium level           |
| ctv3          | XE2q3       | Serum calcium                        |
| ctv3          | XE2q3       | Serum calcium level                  |
| ctv3          | 44I80       | Normal serum calcium level           |
| ctv3          | Xabpk       | Serum adjusted calcium concentration |
| read2         | 44h4.00     | Blood calcium level                  |

<hr>

## Cholesterol <a name='Cholesterol'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | Cholesterol |
| Category | Blood biochemistry
| Type | Biomarker |
| UK Biobank field | [30690](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=30690) |
| Units | mmol/L ([UO_0010003](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0010003))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 21|
| Definition | Serum cholesterol measurent including total cholesterol measurements but excluding plasma-derived measurements. The phenotype includes fasting and non-fasting measurements. |
| Version | alpha | 



### Implementation 


```
IF Read v2 code = read_2
    IF data_provider = England Vision (1) OR data provider = Wales (4)
        Cholesterol = value1

    ELSE IF data_provider = Scotland (2)
        Cholesterol = value2
        units = value3

ELSE IF CTV3 code = read_3 
    IF data_provider = England TPP (3)
        Cholesterol = value1
```
    


| Terminology   | Read code   | Read term                       |
|---------------|-------------|---------------------------------|
| read2         | 44P..00     | Serum cholesterol               |
| read2         | 44PJ.00     | Serum total cholesterol level   |
| read2         | 44PH.00     | Total cholesterol measurement   |
| read2         | 44P3.00     | Serum cholesterol raised        |
| read2         | 44P1.00     | Serum cholesterol normal        |
| read2         | 44PZ.00     | Serum cholesterol NOS           |
| read2         | 44P9.00     | Serum cholesterol studies       |
| read2         | 44P2.00     | Serum cholesterol borderline    |
| read2         | 44PK.00     | Serum fasting total cholesterol |
| read2         | 44P4.00     | Serum cholesterol very high     |
| ctv3          | XE2eD       | Serum cholesterol               |
| ctv3          | XE2eD       | Serum cholesterol level         |
| ctv3          | XaJe9       | Serum total cholesterol level   |
| ctv3          | XSK14       | Total cholesterol measurement   |
| ctv3          | 44P3.       | Serum cholesterol raised        |
| ctv3          | 44P1.       | Serum cholesterol normal        |
| ctv3          | 44PZ.       | Serum cholesterol NOS           |
| ctv3          | 44P9.       | Serum cholesterol studies       |
| ctv3          | 44P2.       | Serum cholesterol borderline    |
| ctv3          | XaLux       | Serum fasting total cholesterol |
| ctv3          | 44P4.       | Serum cholesterol very high     |

<hr>

## Creatinine <a name='Creatinine'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | Creatinine |
| Category | Blood biochemistry
| Type | Biomarker |
| UK Biobank field | [30700](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=30700) |
| Units | umol/L ([UO_0010003](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0010003))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 17|
| Definition | Creatinine levels including corrected levels. Algorithm includes serum, plasma, and unspecified source measurements. |
| Version | alpha | 



### Implementation 


```
IF Read v2 code = read_2
    IF data_provider = England Vision (1) OR data provider = Wales (4)
        Creatinine = value1

    ELSE IF data_provider = Scotland (2)
        Creatinine = value2
        units = value3

ELSE IF CTV3 code = read_3 
    IF data_provider = England TPP (3)
        Creatinine = value1
```
    


| Terminology   | Read code   | Read term                         |
|---------------|-------------|-----------------------------------|
| read2         | 44J3.00     | Serum creatinine                  |
| read2         | 44J3200     | Serum creatinine normal           |
| read2         | 44J3z00     | Serum creatinine NOS              |
| read2         | 44J3300     | Serum creatinine raised           |
| read2         | 44JD.00     | Corrected serum creatinine level  |
| read2         | 44JC.00     | Corrected plasma creatinine level |
| read2         | 44J3100     | Serum creatinine low              |
| read2         | 44J3000     | Serum creatinine abnormal         |
| ctv3          | XE2q5       | Serum creatinine                  |
| ctv3          | XE2q5       | Serum creatinine level            |
| ctv3          | 44J32       | Serum creatinine normal           |
| ctv3          | 44J3z       | Serum creatinine NOS              |
| ctv3          | 44J33       | Serum creatinine raised           |
| ctv3          | XaERc       | Corrected serum creatinine level  |
| ctv3          | XaERX       | Corrected plasma creatinine level |
| ctv3          | 44J31       | Serum creatinine low              |
| ctv3          | 44J30       | Serum creatinine abnormal         |

<hr>

## DBP <a name='DBP'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | DBP |
| Category | Physical measures
| Type | Biomarker |
| UK Biobank field | [94](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=94) |
| Units | mmHg ([UO_0000272](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0000272))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 0|
| Definition | Diastolic blood pressure. |
| Version | alpha | 



### Implementation 



```
IF data_provider = England Vision (1)
    IF read_2 = “246..00 O/E - blood pressure reading”' 
        SBP = value1
        DBP = value2

ELSE IF data_provider = Scotland (2)
    IF read_2 = “246..00 O/E - blood pressure reading”
        DBP = value1
        SBP = value2
    ELSE IF read_2 = “2469.00 O/E - Systolic BP reading”
        SBP = value1
    ELSE IF read_2 = “246A.00 O/E - Diastolic BP reading”
        DBP = value1

IF data_provider = England TPP (3)
    IF read_3 = “2469.00 O/E - Systolic BP reading” 
        SBP = value1
    ELSE IF read_3 = “246A.00 O/E - Diastolic BP reading” 
        DBP = value1

IF data_provider = Wales (4)
    IF read_2 = “246..00 O/E - blood pressure reading”
        SBP = value1
        DBP = value2
    ELSE IF read_2 = “2469.00 O/E - Systolic BP reading”
        SBP = value1
    ELSE IF read_2 = “246A.00 O/E - Diastolic BP reading”
        DBP = value1
```



<hr>

## Eosinophills <a name='Eosinophills'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | Eosinophills |
| Category | Blood count
| Type | Biomarker |
| UK Biobank field | [30150](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=30150) |
| Units | 10^9/L ([UO_0000317](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0000317))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 9|
| Definition | Eosinophil count |
| Version | alpha | 



### Implementation 


```
IF Read v2 code = read_2
    IF data_provider = England Vision (1) OR data provider = Wales (4)
        Eosinophills = value1

    ELSE IF data_provider = Scotland (2)
        Eosinophills = value2
        units = value3

ELSE IF CTV3 code = read_3 
    IF data_provider = England TPP (3)
        Eosinophills = value1
```
    


| Terminology   | Read code   | Read term               |
|---------------|-------------|-------------------------|
| read2         | 42K..00     | Eosinophil count        |
| read2         | 42KZ.00     | Eosinophil count NOS    |
| read2         | 42K1.00     | Eosinophil count normal |
| read2         | 42K3.00     | Eosinophil count raised |
| ctv3          | 42K..       | Eosinophil count        |
| ctv3          | 42KZ.       | Eosinophil count NOS    |
| ctv3          | 42K1.       | Eosinophil count normal |
| ctv3          | 42K3.       | Eosinophil count raised |
| read2         | 42K2.00     | Eosinopenia             |

<hr>

## FEV1 <a name='FEV1'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | FEV1 |
| Category | Physical measures
| Type | Biomarker |
| UK Biobank field | [3063](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=3063) |
| Units | L ([UO_0000099](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0000099))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 7|
| Definition | Forced expired volume in 1 second. Excludes predicted values and measurements post-bronchodialation. |
| Version | alpha | 



### Implementation 


```
IF Read v2 code = read_2
    IF data_provider = England Vision (1) OR data provider = Wales (4)
        FEV1 = value1

    ELSE IF data_provider = Scotland (2)
        FEV1 = value2
        units = value3

ELSE IF CTV3 code = read_3 
    IF data_provider = England TPP (3)
        FEV1 = value1
```
    


| Terminology   | Read code   | Read term                         |
|---------------|-------------|-----------------------------------|
| read2         | 339O.00     | Forced expired volume in 1 second |
| read2         | 3397.00     | Forced expiratory volume - FEV    |
| read2         | 339a.00     | FEV1 before bronchodilation       |
| read2         | 3397000     | FEV normal                        |
| ctv3          | X77Qu       | Forced expired volume in 1 second |
| ctv3          | XaIxQ       | FEV1 before bronchodilation       |
| ctv3          | 33970       | FEV normal                        |

<hr>

## FVC <a name='FVC'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | FVC |
| Category | Physical measures
| Type | Biomarker |
| UK Biobank field | [3062](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=3062) |
| Units | L ([UO_0000099](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0000099))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 7|
| Definition | Forced vital capacity measurement. Excludes predictd values and measurements post-bronchodialation. |
| Version | alpha | 



### Implementation 


```
IF Read v2 code = read_2
    IF data_provider = England Vision (1) OR data provider = Wales (4)
        FVC = value1

    ELSE IF data_provider = Scotland (2)
        FVC = value2
        units = value3

ELSE IF CTV3 code = read_3 
    IF data_provider = England TPP (3)
        FVC = value1
```
    


| Terminology   | Read code   | Read term                                    |
|---------------|-------------|----------------------------------------------|
| read2         | 3396.00     | Forced vital capacity - FVC                  |
| read2         | 3396000     | FVC - forced vital capacity normal           |
| read2         | 3396100     | FVC - forced vital capacity abnormal         |
| ctv3          | 3396.       | Forced vital capacity                        |
| ctv3          | 33960       | FVC - forced vital capacity normal           |
| ctv3          | 33961       | FVC - forced vital capacity abnormal         |
| read2         | 339s.00     | Forced vital capacity before bronchodilation |

<hr>

## Glucose <a name='Glucose'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | Glucose |
| Category | Blood biochemistry
| Type | Biomarker |
| UK Biobank field | [30740](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=30740) |
| Units | mmol/L ([UO_0010003](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0010003))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 16|
| Definition | Blood-based glucose level derived from plasma. Excludes fasting measurements. |
| Version | alpha | 



### Implementation 


```
IF Read v2 code = read_2
    IF data_provider = England Vision (1) OR data provider = Wales (4)
        Glucose = value1

    ELSE IF data_provider = Scotland (2)
        Glucose = value2
        units = value3

ELSE IF CTV3 code = read_3 
    IF data_provider = England TPP (3)
        Glucose = value1
```
    


| Terminology   | Read code   | Read term                    |
|---------------|-------------|------------------------------|
| read2         | 44g..00     | Plasma glucose level         |
| read2         | 44g0.00     | Plasma random glucose level  |
| ctv3          | XM0ly       | Plasma glucose level         |
| ctv3          | 44g0.       | Plasma random glucose level  |
| read2         | 44U..00     | Blood glucose result         |
| read2         | 44TJ.00     | Blood glucose level          |
| read2         | 44U..11     | Blood sugar result           |
| read2         | 44TA.00     | Plasma glucose               |
| read2         | 44U4.00     | Blood glucose 5-6.9 mmol/L   |
| read2         | 44T1000     | Random blood sugar normal    |
| read2         | 44U3.00     | Blood glucose 2.5-4.9 mmol/L |
| read2         | 44U8.00     | Blood glucose normal         |
| read2         | 44U5.00     | Blood glucose 7-9.9 mmol/L   |
| read2         | 44U..12     | Plasma glucose level         |
| read2         | 44U6.00     | Blood glucose 10-13.9 mmol/L |
| read2         | 44T5.00     | Laboratory blood sugar       |

<hr>

## HDL <a name='HDL'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | HDL |
| Category | Blood biochemistry
| Type | Biomarker |
| UK Biobank field | [30760](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=30760) |
| Units | mmol/L ([UO_0010003](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0010003))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 6|
| Definition | Serum fasting/non-fasting/random HDL cholesterol level. |
| Version | alpha | 



### Implementation 


```
IF Read v2 code = read_2
    IF data_provider = England Vision (1) OR data provider = Wales (4)
        HDL = value1

    ELSE IF data_provider = Scotland (2)
        HDL = value2
        units = value3

ELSE IF CTV3 code = read_3 
    IF data_provider = England TPP (3)
        HDL = value1
```
    


| Terminology   | Read code   | Read term                           |
|---------------|-------------|-------------------------------------|
| read2         | 44P5.00     | Serum HDL cholesterol level         |
| read2         | 44PB.00     | Serum fasting HDL cholesterol level |
| read2         | 44PC.00     | Serum random HDL cholesterol level  |
| ctv3          | 44P5.       | Serum HDL cholesterol level         |
| ctv3          | 44PB.       | Serum fasting HDL cholesterol level |
| ctv3          | 44PC.       | Serum random HDL cholesterol level  |

<hr>

## Haematocrit perc <a name='Haematocritperc'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | Haematocrit perc |
| Category | Blood count
| Type | Biomarker |
| UK Biobank field | [30030](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=30030) |
| Units | % ([UO_0000187](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0000187))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 18|
| Definition | Haematocrit / packed cell volume |
| Version | alpha | 



### Implementation 


```
IF Read v2 code = read_2
    IF data_provider = England Vision (1) OR data provider = Wales (4)
        Haematocrit perc = value1

    ELSE IF data_provider = Scotland (2)
        Haematocrit perc = value2
        units = value3

ELSE IF CTV3 code = read_3 
    IF data_provider = England TPP (3)
        Haematocrit perc = value1
```
    


| Terminology   | Read code   | Read term                     |
|---------------|-------------|-------------------------------|
| read2         | 4258.00     | Haematocrit                   |
| read2         | 4257.00     | Packed cell volume            |
| read2         | 425..00     | Haematocrit - PCV             |
| read2         | 425..11     | Packed cell volume - PCV      |
| read2         | 425Z.00     | Haematocrit - PCV - NOS       |
| read2         | 4254.00     | Haematocrit - PCV - low       |
| read2         | 4251.00     | Haematocrit - PCV - normal    |
| ctv3          | X76tb       | Haematocrit                   |
| ctv3          | X76tc       | Packed cell volume            |
| ctv3          | XE2Zq       | Haematocrit - PCV             |
| ctv3          | XE2Zq       | Haematocrit - PCV level       |
| ctv3          | 425Z.       | Haematocrit - PCV - NOS       |
| ctv3          | 4254.       | Haematocrit - PCV - low       |
| ctv3          | 4251.       | Haematocrit - PCV - normal    |
| read2         | 4255.00     | Haematocrit - borderline low  |
| read2         | 4253.00     | Haematocrit - PCV - high      |
| read2         | 4256.00     | Haematocrit - PCV - abnormal  |
| read2         | 4252.00     | Haematocrit - borderline high |

<hr>

## Haemoglobin conc <a name='Haemoglobinconc'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | Haemoglobin conc |
| Category | Blood count
| Type | Biomarker |
| UK Biobank field | [30020](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=30020) |
| Units | g/dL ([UO_0000208](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0000208))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 22|
| Definition | Haemoglobin estimation |
| Version | alpha | 



### Implementation 


```
IF Read v2 code = read_2
    IF data_provider = England Vision (1) OR data provider = Wales (4)
        Haemoglobin conc = value1

    ELSE IF data_provider = Scotland (2)
        Haemoglobin conc = value2
        units = value3

ELSE IF CTV3 code = read_3 
    IF data_provider = England TPP (3)
        Haemoglobin conc = value1
```
    


| Terminology   | Read code   | Read term                   |
|---------------|-------------|-----------------------------|
| read2         | 423..00     | Haemoglobin estimation      |
| read2         | 423..11     | Hb estimation               |
| read2         | 4237.00     | Haemoglobin normal          |
| read2         | 4235.00     | Haemoglobin low             |
| read2         | 423Z.00     | Haemoglobin estimation NOS  |
| read2         | 4239.00     | Haemoglobin high            |
| read2         | 4236.00     | Haemoglobin borderline low  |
| read2         | 4234.00     | Haemoglobin very low        |
| read2         | 423B.00     | Haemoglobin abnormal        |
| ctv3          | Xa96v       | Haemoglobin concentration   |
| ctv3          | XE2m6       | Haemoglobin estimation      |
| ctv3          | XM1Vu       | Hb estimation               |
| ctv3          | 4237.       | Haemoglobin normal          |
| ctv3          | 4235.       | Haemoglobin low             |
| ctv3          | 423Z.       | Haemoglobin estimation NOS  |
| ctv3          | 4239.       | Haemoglobin high            |
| ctv3          | 4236.       | Haemoglobin borderline low  |
| ctv3          | X76ti       | Haemoglobin H inclusion     |
| ctv3          | 4234.       | Haemoglobin very low        |
| ctv3          | 423B.       | Haemoglobin abnormal        |
| read2         | 4238.00     | Haemoglobin borderline high |
| read2         | 423A.00     | Haemoglobin very high       |

<hr>

## HbA1c <a name='HbA1c'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | HbA1c |
| Category | Blood biochemistry
| Type | Biomarker |
| UK Biobank field | [30750](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=30750) |
| Units | mmol/mol ([nan](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/nan))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 25|
| Definition | HbA1c level recorded using International Federation of Clinical Chemistry and Laboratory Medicine or Diabetes Control and Complications Trial (DCCT). |
| Version | alpha | 



### Implementation 


```
IF Read v2 code = read_2
    IF data_provider = England Vision (1) OR data provider = Wales (4)
        HbA1c = value1

    ELSE IF data_provider = Scotland (2)
        HbA1c = value2
        units = value3

ELSE IF CTV3 code = read_3 
    IF data_provider = England TPP (3)
        HbA1c = value1
```
    


| Terminology   | Read code   | Read term                                                                                                   |
|---------------|-------------|-------------------------------------------------------------------------------------------------------------|
| read2         | 42W5.00     | Haemoglobin A1c level - IFCC standardised                                                                   |
| read2         | 42W4.00     | HbA1c level (DCCT aligned)                                                                                  |
| read2         | 42W..00     | Hb. A1C - diabetic control                                                                                  |
| read2         | 42W..11     | Glycosylated Hb                                                                                             |
| read2         | 42W..12     | Glycated haemoglobin                                                                                        |
| read2         | 42W2.00     | Hb. A1C 7-10% - borderline                                                                                  |
| read2         | 42W1.00     | Hb. A1C < 7% - good control                                                                                 |
| read2         | 42WZ.00     | Hb. A1C - diabetic control NOS                                                                              |
| read2         | 42W3.00     | Hb. A1C > 10% - bad control                                                                                 |
| ctv3          | XaPbt       | Haemoglobin A1c level - International Federation of Clinical Chemistry and Laboratory Medicine standardised |
| ctv3          | XaERp       | HbA1c level (DCCT aligned)                                                                                  |
| ctv3          | XE24t       | Hb. A1C - diabetic control                                                                                  |
| ctv3          | X80U3       | Glycated haemoglobin                                                                                        |
| ctv3          | X80U3       | Glycosylated Hb                                                                                             |
| ctv3          | 42W2.       | Hb. A1C 7-10% - borderline                                                                                  |
| ctv3          | 42W1.       | Hb. A1C < 7% - good control                                                                                 |
| ctv3          | 42WZ.       | Hb. A1C - diabetic control NOS                                                                              |
| ctv3          | 42W3.       | Hb. A1C > 10% - bad control                                                                                 |
| read2         | 44TB.00     | Haemoglobin A1c level                                                                                       |
| read2         | 42c..00     | HbA1 - diabetic control                                                                                     |
| read2         | 42c3.00     | HbA1 level (DCCT aligned)                                                                                   |
| read2         | 42c1.00     | HbA1 7 - 10% - borderline control                                                                           |
| read2         | 42c0.00     | HbA1 < 7% - good control                                                                                    |
| read2         | 44TC.00     | Haemoglobin A1 level                                                                                        |
| read2         | 42c2.00     | HbA1 > 10% - bad control                                                                                    |

<hr>

## Height <a name='Height'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | Height |
| Category | Physical measures
| Type | Biomarker |
| UK Biobank field | [50](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=50) |
| Units | cm ([UO_0000015](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0000015))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 6|
| Definition | Height |
| Version | alpha | 



### Implementation 


    
IF data_provider = England Vision (1) OR data_provider = Wales (4)
    IF read_2 in phenotype codes
        Height = value1

ELSE IF data_provider = Scotland (2)
    IF read_2 = “229.. O/E – height” 
        Height = value1

ELSE IF data_provider = England TPP (3)
    IF CTV3 code = read_3
        Height = value1


| Terminology   | Read code   | Read term                      |
|---------------|-------------|--------------------------------|
| read2         | 229..00     | O/E - height                   |
| read2         | 229Z.00     | O/E - height NOS               |
| read2         | 2293.00     | O/E -height within 10% average |
| ctv3          | 229..       | O/E - height                   |
| ctv3          | 229Z.       | O/E - height NOS               |
| ctv3          | 2293.       | O/E -height within 10% average |

<hr>

## Lymphocytes <a name='Lymphocytes'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | Lymphocytes |
| Category | Blood count
| Type | Biomarker |
| UK Biobank field | [30120](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=30120) |
| Units | 10^9/L ([UO_0000317](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0000317))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 7|
| Definition | Leucocyte count |
| Version | alpha | 



### Implementation 


```
IF Read v2 code = read_2
    IF data_provider = England Vision (1) OR data provider = Wales (4)
        Lymphocytes = value1

    ELSE IF data_provider = Scotland (2)
        Lymphocytes = value2
        units = value3

ELSE IF CTV3 code = read_3 
    IF data_provider = England TPP (3)
        Lymphocytes = value1
```
    


| Terminology   | Read code   | Read term               |
|---------------|-------------|-------------------------|
| read2         | 42M..00     | Lymphocyte count        |
| read2         | 42MZ.00     | Lymphocyte count NOS    |
| read2         | 42M1.00     | Lymphocyte count normal |
| read2         | 42M4.00     | Abnormal lymphocytes    |
| ctv3          | 42M..       | Lymphocyte count        |
| ctv3          | 42MZ.       | Lymphocyte count NOS    |
| ctv3          | 42M1.       | Lymphocyte count normal |

<hr>

## MCHb conc <a name='MCHbconc'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | MCHb conc |
| Category | Blood count
| Type | Biomarker |
| UK Biobank field | [30060](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=30060) |
| Units | g/dL ([UO_0000208](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0000208))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 10|
| Definition | Mean corpusc. Hb. conc. (MCHC) |
| Version | alpha | 



### Implementation 


```
IF Read v2 code = read_2
    IF data_provider = England Vision (1) OR data provider = Wales (4)
        MCHb conc = value1

    ELSE IF data_provider = Scotland (2)
        MCHb conc = value2
        units = value3

ELSE IF CTV3 code = read_3 
    IF data_provider = England TPP (3)
        MCHb conc = value1
```
    


| Terminology   | Read code   | Read term                           |
|---------------|-------------|-------------------------------------|
| read2         | 429..00     | Mean corpusc. Hb. conc. (MCHC)      |
| read2         | 429Z.00     | MCHC - NOS                          |
| read2         | 4291.00     | MCHC - normal                       |
| ctv3          | 429..       | Mean cell haemoglobin concentration |
| ctv3          | 429Z.       | MCHC - NOS                          |
| ctv3          | 4291.       | MCHC - normal                       |
| read2         | 4294.00     | MCHC - raised                       |
| read2         | 4293.00     | MCHC - low                          |
| read2         | 4292.00     | MCHC - borderline low               |
| read2         | 4295.00     | MCHC - borderline raised            |

<hr>

## MCV <a name='MCV'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | MCV |
| Category | Blood count
| Type | Biomarker |
| UK Biobank field | [30040](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=30040) |
| Units | fL ([UO_0000104](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0000104))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 13|
| Definition | Mean corpuscular volume (MCV) |
| Version | alpha | 



### Implementation 


```
IF Read v2 code = read_2
    IF data_provider = England Vision (1) OR data provider = Wales (4)
        MCV = value1

    ELSE IF data_provider = Scotland (2)
        MCV = value2
        units = value3

ELSE IF CTV3 code = read_3 
    IF data_provider = England TPP (3)
        MCV = value1
```
    


| Terminology   | Read code   | Read term                     |
|---------------|-------------|-------------------------------|
| read2         | 42A..00     | Mean corpuscular volume (MCV) |
| read2         | 42A..11     | Mean cell volume              |
| read2         | 42AZ.00     | MCV - NOS                     |
| read2         | 42A1.00     | MCV - normal                  |
| read2         | 42A3.00     | MCV - raised                  |
| read2         | 42A4.00     | MCV - low                     |
| ctv3          | 42A..       | Mean cell volume              |
| ctv3          | 42AZ.       | MCV - NOS                     |
| ctv3          | 42A1.       | MCV - normal                  |
| ctv3          | 42A3.       | MCV - raised                  |
| ctv3          | 42A4.       | MCV - low                     |
| read2         | 42A2.00     | MCV - borderline raised       |
| read2         | 42A5.00     | MCV - borderline low          |

<hr>

## Monocytes <a name='Monocytes'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | Monocytes |
| Category | Blood count
| Type | Biomarker |
| UK Biobank field | [30130](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=30130) |
| Units | 10^9/L ([UO_0000317](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0000317))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 9|
| Definition | Monocyte count |
| Version | alpha | 



### Implementation 


```
IF Read v2 code = read_2
    IF data_provider = England Vision (1) OR data provider = Wales (4)
        Monocytes = value1

    ELSE IF data_provider = Scotland (2)
        Monocytes = value2
        units = value3

ELSE IF CTV3 code = read_3 
    IF data_provider = England TPP (3)
        Monocytes = value1
```
    


| Terminology   | Read code   | Read term               |
|---------------|-------------|-------------------------|
| read2         | 42N..00     | Monocyte count          |
| read2         | 42NZ.00     | Monocyte count NOS      |
| read2         | 42N1.00     | Monocyte count normal   |
| read2         | 42N5.00     | Monocyte count abnormal |
| ctv3          | 42N..       | Monocyte count          |
| ctv3          | 42NZ.       | Monocyte count NOS      |
| ctv3          | 42N1.       | Monocyte count normal   |
| ctv3          | 42N5.       | Monocyte count abnormal |
| read2         | 42N2.00     | Monocyte count raised   |

<hr>

## Neutrophills <a name='Neutrophills'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | Neutrophills |
| Category | Blood count
| Type | Biomarker |
| UK Biobank field | [30140](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=30140) |
| Units | 10^9/L ([UO_0000317](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0000317))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 13|
| Definition | Neutrophil count |
| Version | alpha | 



### Implementation 


```
IF Read v2 code = read_2
    IF data_provider = England Vision (1) OR data provider = Wales (4)
        Neutrophills = value1

    ELSE IF data_provider = Scotland (2)
        Neutrophills = value2
        units = value3

ELSE IF CTV3 code = read_3 
    IF data_provider = England TPP (3)
        Neutrophills = value1
```
    


| Terminology   | Read code   | Read term                 |
|---------------|-------------|---------------------------|
| read2         | 42J..00     | Neutrophil count          |
| read2         | 42JZ.00     | Neutrophil count NOS      |
| read2         | 42J..11     | Granulocyte count         |
| read2         | 42J2.00     | Neutropenia               |
| read2         | 42J1.00     | Neutrophil count normal   |
| read2         | 42J3.00     | Neutrophilia              |
| read2         | 42J4.00     | Neutrophil count abnormal |
| ctv3          | 42J..       | Neutrophil count          |
| ctv3          | 42JZ.       | Neutrophil count NOS      |
| ctv3          | 42J2.       | Neutropenia               |
| ctv3          | 42J1.       | Neutrophil count normal   |
| ctv3          | 42J3.       | Neutrophilia              |
| ctv3          | 42J4.       | Neutrophil count abnormal |

<hr>

## Platelets <a name='Platelets'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | Platelets |
| Category | Blood count
| Type | Biomarker |
| UK Biobank field | [30080](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=30080) |
| Units | 10^9/L ([UO_0000317](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0000317))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 12|
| Definition | Platelet count. Excludes platelet distribution width measurements. |
| Version | alpha | 



### Implementation 


```
IF Read v2 code = read_2
    IF data_provider = England Vision (1) OR data provider = Wales (4)
        Platelets = value1

    ELSE IF data_provider = Scotland (2)
        Platelets = value2
        units = value3

ELSE IF CTV3 code = read_3 
    IF data_provider = England TPP (3)
        Platelets = value1
```
    


| Terminology   | Read code   | Read term               |
|---------------|-------------|-------------------------|
| read2         | 42P..00     | Platelet count          |
| read2         | 42P1.00     | Platelet count normal   |
| read2         | 42PZ.00     | Platelet count NOS      |
| read2         | 42P2.00     | Thrombocytopenia        |
| read2         | 42P3.00     | Thrombocythaemia        |
| read2         | 42P4.00     | Platelet count abnormal |
| ctv3          | 42P..       | Platelet count          |
| ctv3          | 42P1.       | Platelet count normal   |
| ctv3          | 42PZ.       | Platelet count NOS      |
| ctv3          | XE24o       | Thrombocytopenia        |
| ctv3          | 42P3.       | Thrombocythaemia        |
| ctv3          | 42P4.       | Platelet count abnormal |

<hr>

## RBC <a name='RBC'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | RBC |
| Category | Blood count
| Type | Biomarker |
| UK Biobank field | [30010](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=30010) |
| Units | 10^12/L ([UO_0000317](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0000317))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 12|
| Definition | Red blood cell (RBC) count excluding nucleated RBC values. |
| Version | alpha | 



### Implementation 


```
IF Read v2 code = read_2
    IF data_provider = England Vision (1) OR data provider = Wales (4)
        RBC = value1

    ELSE IF data_provider = Scotland (2)
        RBC = value2
        units = value3

ELSE IF CTV3 code = read_3 
    IF data_provider = England TPP (3)
        RBC = value1
```
    


| Terminology   | Read code   | Read term                   |
|---------------|-------------|-----------------------------|
| read2         | 426..00     | Red blood cell (RBC) count  |
| read2         | 426Z.00     | RBC count NOS               |
| read2         | 4261.00     | RBC count normal            |
| read2         | 4263.00     | RBC count low               |
| ctv3          | 426..       | Red blood cell count        |
| ctv3          | 426Z.       | RBC count NOS               |
| ctv3          | 4261.       | RBC count normal            |
| ctv3          | 4263.       | RBC count low               |
| read2         | 4262.00     | RBC count borderline low    |
| read2         | 4264.00     | RBC count raised            |
| read2         | 4267.00     | RBC count abnormal          |
| read2         | 4265.00     | RBC count borderline raised |

<hr>

## SBP <a name='SBP'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | SBP |
| Category | Physical measures
| Type | Biomarker |
| UK Biobank field | [93](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=93) |
| Units | mmHg ([UO_0000272](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0000272))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 0|
| Definition | Systolic blood pressure. |
| Version | alpha | 



### Implementation 



```
IF data_provider = England Vision (1)
    IF read_2 = “246..00 O/E - blood pressure reading”' 
        SBP = value1
        DBP = value2

ELSE IF data_provider = Scotland (2)
    IF read_2 = “246..00 O/E - blood pressure reading”
        DBP = value1
        SBP = value2
    ELSE IF read_2 = “2469.00 O/E - Systolic BP reading”
        SBP = value1
    ELSE IF read_2 = “246A.00 O/E - Diastolic BP reading”
        DBP = value1

IF data_provider = England TPP (3)
    IF read_3 = “2469.00 O/E - Systolic BP reading” 
        SBP = value1
    ELSE IF read_3 = “246A.00 O/E - Diastolic BP reading” 
        DBP = value1

IF data_provider = Wales (4)
    IF read_2 = “246..00 O/E - blood pressure reading”
        SBP = value1
        DBP = value2
    ELSE IF read_2 = “2469.00 O/E - Systolic BP reading”
        SBP = value1
    ELSE IF read_2 = “246A.00 O/E - Diastolic BP reading”
        DBP = value1
```



<hr>

## Total bilirubin <a name='Totalbilirubin'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | Total bilirubin |
| Category | Blood biochemistry
| Type | Biomarker |
| UK Biobank field | [30840](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=30840) |
| Units | umol/L ([UO_0010003](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0010003))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 15|
| Definition | Serum bilirubin level. Excludes conjugated bilirubin levels. |
| Version | alpha | 



### Implementation 


```
IF Read v2 code = read_2
    IF data_provider = England Vision (1) OR data provider = Wales (4)
        Total bilirubin = value1

    ELSE IF data_provider = Scotland (2)
        Total bilirubin = value2
        units = value3

ELSE IF CTV3 code = read_3 
    IF data_provider = England TPP (3)
        Total bilirubin = value1
```
    


| Terminology   | Read code   | Read term                   |
|---------------|-------------|-----------------------------|
| read2         | 44EC.00     | Serum total bilirubin level |
| read2         | 44E..00     | Serum bilirubin level       |
| read2         | 44E3.00     | Total bilirubin             |
| read2         | 44E1.00     | Serum bilirubin normal      |
| read2         | 44EZ.00     | Serum bilirubin NOS         |
| read2         | 44E2.00     | Serum bilirubin raised      |
| read2         | 44E6.00     | Serum bilirubin borderline  |
| ctv3          | XaERu       | Serum total bilirubin level |
| ctv3          | 44E..       | Serum bilirubin level       |
| ctv3          | XE2qu       | Total bilirubin level       |
| ctv3          | XE2qu       | Total bilirubin             |
| ctv3          | 44E1.       | Serum bilirubin normal      |
| ctv3          | 44EZ.       | Serum bilirubin NOS         |
| ctv3          | 44E2.       | Serum bilirubin raised      |
| ctv3          | 44E6.       | Serum bilirubin borderline  |

<hr>

## Triglycerides <a name='Triglycerides'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | Triglycerides |
| Category | Blood biochemistry
| Type | Biomarker |
| UK Biobank field | [30870](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=30870) |
| Units | mmol/L ([UO_0010003](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0010003))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 15|
| Definition | Serum triglycerides measurements. Algorithm excludes plasma-derived measurements. Includes fasting/non-fasting/random values. |
| Version | alpha | 



### Implementation 


```
IF Read v2 code = read_2
    IF data_provider = England Vision (1) OR data provider = Wales (4)
        Triglycerides = value1

    ELSE IF data_provider = Scotland (2)
        Triglycerides = value2
        units = value3

ELSE IF CTV3 code = read_3 
    IF data_provider = England TPP (3)
        Triglycerides = value1
```
    


| Terminology   | Read code   | Read term                        |
|---------------|-------------|----------------------------------|
| read2         | 44Q..00     | Serum triglycerides              |
| read2         | 44Q4.00     | Serum fasting triglyceride level |
| read2         | 44Q5.00     | Serum random triglyceride level  |
| read2         | 44QZ.00     | Serum triglycerides NOS          |
| read2         | 44Q1.00     | Serum triglycerides normal       |
| read2         | 44Q3.00     | Serum triglycerides raised       |
| read2         | 44Q2.00     | Serum triglycerides borderline   |
| ctv3          | XE2q9       | Serum triglycerides              |
| ctv3          | XE2q9       | Serum triglyceride levels        |
| ctv3          | 44Q4.       | Serum fasting triglyceride level |
| ctv3          | 44Q5.       | Serum random triglyceride level  |
| ctv3          | 44QZ.       | Serum triglycerides NOS          |
| ctv3          | 44Q1.       | Serum triglycerides normal       |
| ctv3          | 44Q3.       | Serum triglycerides raised       |
| ctv3          | 44Q2.       | Serum triglycerides borderline   |

<hr>

## Urea <a name='Urea'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | Urea |
| Category | Blood biochemistry
| Type | Biomarker |
| UK Biobank field | [30670](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=30670) |
| Units | mmol/L ([UO_0010003](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0010003))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 17|
| Definition | Serum / plasma urea level |
| Version | alpha | 



### Implementation 


```
IF Read v2 code = read_2
    IF data_provider = England Vision (1) OR data provider = Wales (4)
        Urea = value1

    ELSE IF data_provider = Scotland (2)
        Urea = value2
        units = value3

ELSE IF CTV3 code = read_3 
    IF data_provider = England TPP (3)
        Urea = value1
```
    


| Terminology   | Read code   | Read term                     |
|---------------|-------------|-------------------------------|
| read2         | 44J9.00     | Serum urea level              |
| read2         | 44J8.00     | Blood urea                    |
| read2         | 44J..11     | Urea - blood                  |
| read2         | 44JA.00     | Plasma urea level             |
| read2         | 44J..00     | Blood urea/renal function     |
| read2         | 44J1.00     | Blood urea normal             |
| read2         | 44J2.00     | Blood urea abnormal           |
| read2         | 44J..13     | Serum urea level              |
| read2         | 44JZ.00     | Blood urea/renal function NOS |
| read2         | 44J8.11     | Urea - blood                  |
| ctv3          | XM0lt       | Serum urea level              |
| ctv3          | X771P       | Blood urea                    |
| ctv3          | X771P       | Urea - blood                  |
| ctv3          | XaDvl       | Plasma urea level             |
| ctv3          | 44J1.       | Blood urea normal             |
| ctv3          | 44J2.       | Blood urea abnormal           |
| ctv3          | 44JZ.       | Blood urea/renal function NOS |

<hr>

## WBC <a name='WBC'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | WBC |
| Category | Blood count
| Type | Biomarker |
| UK Biobank field | [30000](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=30000) |
| Units | 10^9/L ([UO_0000317](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0000317))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 19|
| Definition | Total white cell count. Excludes polymorphonuclear leukocyte count. |
| Version | alpha | 



### Implementation 


```
IF Read v2 code = read_2
    IF data_provider = England Vision (1) OR data provider = Wales (4)
        WBC = value1

    ELSE IF data_provider = Scotland (2)
        WBC = value2
        units = value3

ELSE IF CTV3 code = read_3 
    IF data_provider = England TPP (3)
        WBC = value1
```
    


| Terminology   | Read code   | Read term                            |
|---------------|-------------|--------------------------------------|
| read2         | 42H..00     | Total white cell count               |
| read2         | 42H..11     | White blood count                    |
| read2         | 42H..12     | White cell count                     |
| read2         | 42H7.00     | Total white blood count              |
| read2         | 42H1.00     | White cell count normal              |
| read2         | 42HZ.00     | Total white cell count NOS           |
| read2         | 42H3.00     | Leucocytosis -high white count       |
| read2         | 42H8.00     | Total WBC (IMM)                      |
| read2         | 42H2.00     | Leucopenia - low white count         |
| read2         | 42H5.00     | White cell count abnormal            |
| ctv3          | XaIdY       | Total white blood count              |
| ctv3          | 42H..       | White blood cell count               |
| ctv3          | 42H..       | White blood cell count - observation |
| ctv3          | 42H1.       | White cell count normal              |
| ctv3          | 42H3.       | Leucocytosis                         |
| ctv3          | 42HZ.       | Total white cell count NOS           |
| ctv3          | XaIdZ       | Total WBC (IMM)                      |
| ctv3          | 42H2.       | Leucopenia                           |
| ctv3          | 42H5.       | White cell count abnormal            |

<hr>

## Weight <a name='Weight'></a> 

### Metadata 


[]() | |        
|------|----------|
| Name | Weight |
| Category | Physical measures
| Type | Biomarker |
| UK Biobank field | [21002](http://biobank.ctsu.ox.ac.uk/crystal/field.cgi?id=21002) |
| Units | Kg ([UO_0000009](https://www.ebi.ac.uk/ols/ontologies/uo/terms?iri=http://purl.obolibrary.org/obo/UO_0000009))
| Data source | UK Biobank | 
| Sex | Male/female |
| Controlled clinical terminologies | Read v2, Clinical Terms Version 3 |
| Total terms | 18|
| Definition | Weight |
| Version | alpha | 



### Implementation 


    
IF read_2 in phenotype codes
    IF data_provider = England Vision (1) OR data_provider = Wales (4)
        Weight = value1

    ELSE IF data_provider = Scotland (2)
        IF read_2 = '22A.. O/E - weight' 
            Weight = value2

ELSE IF read_3 in phenotype codes
    IF data_provider = England TPP (3)
        Weight = value1


| Terminology   | Read code   | Read term                      |
|---------------|-------------|--------------------------------|
| read2         | 22A..00     | O/E - weight                   |
| read2         | 22AZ.00     | O/E - weight NOS               |
| read2         | 22A4.00     | O/E - weight 10-20% over ideal |
| read2         | 22A3.00     | O/E - weight within 10% ideal  |
| read2         | 22A5.00     | O/E - weight > 20% over ideal  |
| read2         | 22A4.11     | O/E - overweight               |
| read2         | 22A5.11     | O/E - obese                    |
| read2         | 22A6.00     | O/E - Underweight              |
| ctv3          | 22A..       | O/E - weight                   |
| ctv3          | 22AZ.       | O/E - weight NOS               |
| ctv3          | XE1h3       | O/E - weight 10-20% over ideal |
| ctv3          | XM1YD       | O/E - overweight               |
| ctv3          | 22A3.       | O/E - weight within 10% ideal  |
| ctv3          | 222A.       | O/E - obese                    |
| ctv3          | 22A6.       | O/E - Underweight              |
| read2         | 1622.00     | Weight increasing              |
| read2         | 22A2.00     | O/E -weight 10-20% below ideal |
| read2         | 22A1.00     | O/E - weight > 20% below ideal |

<hr>

# Units <a name="units"></a>

| Raw value       | Cleaned        |
|-----------------|----------------|
| MEA000          |                |
| MEA001          | %              |
| MEA016          | /hour          |
| MEA021          | /mL            |
| MEA026          | 1              |
| MEA031          | 10*12/L        |
| MEA035          | 10*6/L         |
| MEA037          | 10*9/L         |
| MEA038          | 10*9/mL        |
| MEA047          | fL             |
| MEA056          | g/dL           |
| MEA057          | g/L            |
| MEA058          | h              |
| MEA061          | IU/L           |
| MEA062          | IU/mL          |
| MEA071          | L/min          |
| MEA080          | mg             |
| MEA082          | mg/dL          |
| MEA083          | mg/L           |
| MEA086          | mg/mmol        |
| MEA090          | mL/min         |
| MEA093          | mm(Hg)         |
| MEA095          | mmol/d         |
| MEA096          | mmol/L         |
| MEA097          | mmol/mol       |
| MEA099          | mol/L          |
| MEA104          | ng             |
| MEA106          | ng/mL          |
| MEA110          | nmol/L         |
| MEA114          | pg             |
| MEA116          | pg/dL          |
| MEA124          | s              |
| MEA127          | U/L            |
| MEA142          | umol/L         |
| MEA151          | ratio          |
| MEA153          | 10*9           |
| MEA154          | L              |
| MEA156          | mmol           |
| MEA161          | 1/1            |
| MEA169          | mIU/L          |
| MEA178          | ug/mL          |
| MEA183          | 10*-2          |
| MEA184          | 10*-3          |
| MEA185          | L/L            |
| MEA187          | nmol/g         |
| MEA194          | titre          |
| MEA205          | nmol/gHb/h     |
| MEA210          | #G ( )/L       |
| MEA215          | %Hb            |
| MEA252          | mmol/g(dry wt) |
| x10^9/l         | 10^9/L         |
| 10^9/L          | 10^9/L         |
| x10^9/L         | 10^9/L         |
| 10^9/l          | 10^9/L         |
| 10 ^9/L         | 10^9/L         |
| x10^9 /L        | 10^9/L         |
| x10-9/l         | 10^9/L         |
| 10*9/L          | 10^9/L         |
| x10 ^9/L        | 10^9/L         |
| x10 9/L         | 10^9/L         |
| X10 9/L         | 10^9/L         |
| *10^9/l         | 10^9/L         |
| 10 ^9/l         | 10^9/L         |
| 10*9/l          | 10^9/L         |
| x10^12/l        | 10^12/L        |
| 10^12/L         | 10^12/L        |
| x10^12/L        | 10^12/L        |
| 10 ^12/L        | 10^12/L        |
| 10^12/l         | 10^12/L        |
| x10-12/l        | 10^12/L        |
| 10*12/L         | 10^12/L        |
| fl              | fL             |
| g/l             | g/L            |
| mmHG            | mmHg           |
| mm/Hg           | mmHg           |
| mm Hg           | mmHg           |
| mg/l            | mg/L           |
| g/dl            | g/dL           |
| l               | L              |
| litre           | L              |
| litres          | L              |
| Litres          | L              |
| mmol/l          | mmol/L         |
| mmol/L          | mmol/L         |
| mmol/mol Hb     | mmol/mol       |
| MMOL/L          | mmol/L         |
| umol/L          | umol/L         |
| umol/l          | umol/L         |
| Mmol/mol        | mmol/L         |
| nmol/l          | nmol/L         |
| %Hb             | %              |
| per cent        | %              |
| Ratio           | ratio          |
| % total Hb      | %              |
| %total Hb       | %              |
| µmol/L          | umol/L         |
| u/l             | U/L            |
| IU/L            | U/L            |
| iu/l            | U/L            |
| No UOM assigned |                |
| Unknown         |                |
