# Hospital-Clinic-Analysis

## Overview

This repository contains the analysis of a basic Hospital / Clinic's dataset to demonstrate skills: creating nodes on Graph and retrieve insights on Neo4j in Cypher and do the same way in SQL on Azure.

## Languages and Tools:

- `Cypher`

- `Graph`

- `Neo4j`

- `SQL`

- `Azure`

## Nodes on Neo4j

### Patients: Nodes

Create a graph database that has 20 patients with 3 properties – 10 should be females and 10 males:

•	Name
•	Age
•	Sex

![1st 5 females](https://user-images.githubusercontent.com/70437668/161478794-4f98996a-49cb-4a68-b04d-e96ad5f1627a.jpg)

Name: "Orren graph"	Age: 25	Sex: "M" 
Name: "Joe graph"	Age: 27	Sex: "M" 
Name: "Paul graph"	Age: 55	Sex: "M" 
Name: "David graph"	Age: 42	Sex: "M" 
Name: "Peter graph"	Age: 35	Sex: "M" 
Name: "Andrew graph"	Age: 26	Sex: "M" 
Name: "Henry graph"	Age: 29	Sex: "M" 
Name: "Patrick graph"	Age: 34	Sex: "M" 
Name: "John graph"	Age: 21	Sex: "M" 
Name: "Michael graph"	Age: 67	Sex: "M" 
Name: "Patsy graph"	Age: 44	Sex: "F" 
Name: "Joan graph"	Age: 55	Sex: "F" 
Name: "June graph"	Age: 33	Sex: "F" 
Name: "April graph"	Age: 22	Sex: "F" 
Name: "May graph"	Age: 12	Sex: "F" 
Name: "Betty graph"	Age: 19	Sex: "F" 
Name: "Theresa graph"	Age: 67	Sex: "F" 
Name: "Claudette graph"	Age: 88	Sex: "F" 
Name: "Cheryl graph"	Age: 27	Sex: "F" 
Name: "Pamela graph"	Age: 73	Sex: "F" 

```
CREATE (patient1: Patient {patientID: "1", fullName: "Orren graph", Age: "25", Sex: "M"})
CREATE (patient2: Patient {patientID: "2", fullName: "Joe graph", Age: "27", Sex: "M"})
CREATE (patient3: Patient {patientID: "3", fullName: "Paul graph", Age: "55", Sex: "M"})
CREATE (patient4: Patient {patientID: "4", fullName: "David graph", Age: "42", Sex: "M"})
CREATE (patient5: Patient {patientID: "5", fullName: "Peter graph", Age: "35", Sex: "M"})
CREATE (patient6: Patient {patientID: "6", fullName: "Andrew graph", Age: "26", Sex: "M"})
CREATE (patient7: Patient {patientID: "7", fullName: "Henry graph", Age: "29", Sex: "M"})
CREATE (patient8: Patient {patientID: "8", fullName: "Patrick graph", Age: "34", Sex: "M"})
CREATE (patient9: Patient {patientID: "9", fullName: "John graph", Age: "21", Sex: "M"})
CREATE (patient10: Patient {patientID: "10", fullName: "Michael graph", Age: "67", Sex: "M"})
CREATE (patient11: Patient {patientID: "11", fullName: "Patsy graph", Age: "44", Sex: "F"})
CREATE (patient12: Patient {patientID: "12", fullName: "Joan graph", Age: "55", Sex: "F"})
CREATE (patient13: Patient {patientID: "13", fullName: "June graph", Age: "33", Sex: "F"})
CREATE (patient14: Patient {patientID: "14", fullName: "April graph", Age: "22", Sex: "F"})
CREATE (patient15: Patient {patientID: "15", fullName: "May graph", Age: "12", Sex: "F"})
CREATE (patient16: Patient {patientID: "16", fullName: "Betty graph", Age: "19", Sex: "F"})
CREATE (patient17: Patient {patientID: "17", fullName: "Theresa graph", Age: "67", Sex: "F"})
CREATE (patient18: Patient {patientID: "18", fullName: "Claudette graph", Age: "88", Sex: "F"})
CREATE (patient19: Patient {patientID: "19", fullName: "Cheryl graph", Age: "27", Sex: "F"})
CREATE (patient20: Patient {patientID: "20", fullName: "Pamela graph", Age: "73", Sex: "F"})
```

### Create 10 disease conditions with property “Type” for the following:

•	Heart disease
•	Kidney disease
•	Diabetes
•	Breast Cancer
•	Lung Cancer
•	Blood Pressure
•	Obesity 
•	Pancreatic Cancer
•	Crohns Disease
•	Prostrate Cancer 

![1st 5 females](https://user-images.githubusercontent.com/70437668/161478800-79a2d445-3d05-40cf-9b72-68dc6b9cc35d.jpg)

```
CREATE (disease1: Disease {diseaseID: "1", diseaseType: "Heart Disease"})
CREATE (disease2: Disease {diseaseID: "2", diseaseType: "Kidney Disease"})
CREATE (disease3: Disease {diseaseID: "3", diseaseType: "Diabetes"})
CREATE (disease4: Disease {diseaseID: "4", diseaseType: "Breast Cancer"})
CREATE (disease5: Disease {diseaseID: "5", diseaseType: "Lung Cancer"})
CREATE (disease6: Disease {diseaseID: "6", diseaseType: "Blood Pressure"})
CREATE (disease7: Disease {diseaseID: "7", diseaseType: "Obesity"})
CREATE (disease8: Disease {diseaseID: "8", diseaseType: "Pancreatic Cancer"})
CREATE (disease9: Disease {diseaseID: "9", diseaseType: "Crohns Disease"})
CREATE (disease10: Disease {diseaseID: "10", diseaseType: "Prostate Cancer"})
```

### Create 4 doctors with 4 properties two should be family doctors and two should be specialists:

•	Name 
•	Age
•	Sex 
•	Speciality “Family Doctor”,” Specialist” 

![1st 5 females](https://user-images.githubusercontent.com/70437668/161478830-0eb49e6c-e364-4db9-8ec8-c2b5727103e9.jpg)

Name: "Dr Jones"	Age: 45	Sex: "M"	Speciality: "Family Doctor" 
Name: "Dr Moses"	Age: 35	Sex: "M"	Speciality: "Specialist" 
Name: "Dr Ann"	Age: 55	Sex: "F"	Speciality: "Family Doctor" 
Name: "Dr Susan"	Age: 42	Sex: "F"	Speciality: "Specialist"

```
CREATE (doctor1: Doctor {doctorID: "1", Name: "Dr Jones", Age: "45", Sex: "M", Specialty: "Family Doctor"})
CREATE (doctor2: Doctor {doctorID: "2", Name: "Dr Moses", Age: "35", Sex: "M", Specialty: "Specialist"})
CREATE (doctor3: Doctor {doctorID: "3", Name: "Dr Ann", Age: "55", Sex: "F", Specialty: "Family Doctor"})
CREATE (doctor4: Doctor {doctorID: "4", Name: "Dr Susan", Age: "45", Sex: "F", Specialty: "Specialist"})
```

## Relationships

### 1/ Create a relationship “Has_Disease”  and associate  10 patients (the first 5 men and the first 5 women)  with “Kidney disease”, “Heart Disease” and “Blood Pressure”  

![1st 5 males](https://user-images.githubusercontent.com/70437668/161478687-531d5723-45ec-4702-aeb0-aad78b3ea791.jpg)

#### 1// Orren
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Orren graph" AND d. diseaseType = "Kidney Disease" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```

```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Orren graph" AND d. diseaseType = "Heart Disease" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```

```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Orren graph" AND d. diseaseType = "Blood Pressure" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```

#### 2// Joe
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Joe graph" AND d. diseaseType = "Kidney Disease" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Joe graph" AND d. diseaseType = "Heart Disease" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Joe graph" AND d. diseaseType = "Blood Pressure" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```

#### 3// Paul
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Paul graph" AND d. diseaseType = "Kidney Disease" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Paul graph" AND d. diseaseType = "Heart Disease" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Paul graph" AND d. diseaseType = "Blood Pressure" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```

#### 4// David
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "David graph" AND d. diseaseType = "Kidney Disease" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "David graph" AND d. diseaseType = "Heart Disease" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "David graph" AND d. diseaseType = "Blood Pressure" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```

#### 5// Peter

```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Peter graph" AND d. diseaseType = "Kidney Disease" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Peter graph" AND d. diseaseType = "Heart Disease" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Peter graph" AND d. diseaseType = "Blood Pressure" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```

![1st 5 females](https://user-images.githubusercontent.com/70437668/161478701-f25cdc90-b042-494c-9cef-02670c1d32a7.jpg)

#### 11// Patsy
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Patsy graph" AND d. diseaseType = "Kidney Disease" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Patsy graph" AND d. diseaseType = "Heart Disease" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Patsy graph" AND d. diseaseType = "Blood Pressure" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```

#### 12// Joan
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Joan graph" AND d. diseaseType = "Kidney Disease" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Joan graph" AND d. diseaseType = "Heart Disease" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Joan graph" AND d. diseaseType = "Blood Pressure" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```

#### 13// June
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "June graph" AND d. diseaseType = "Kidney Disease" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "June graph" AND d. diseaseType = "Heart Disease" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "June graph" AND d. diseaseType = "Blood Pressure" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```

#### 14// April
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "April graph" AND d. diseaseType = "Kidney Disease" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "April graph" AND d. diseaseType = "Heart Disease" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "April graph" AND d. diseaseType = "Blood Pressure" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```
#### 15// May
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "May graph" AND d. diseaseType = "Kidney Disease" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "May graph" AND d. diseaseType = "Heart Disease" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "May graph" AND d. diseaseType = "Blood Pressure" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```

### 2/ Your next 3 female (Patsy, Cheryl, Pamela) patients should have the relationship “Has_Disease” associated with “Breast Cancer”.
![3 females breast cancer](https://user-images.githubusercontent.com/70437668/161478883-f7294c9e-bd5d-4a2d-afc0-2a26aee149fb.jpg)

```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Patsy graph" AND d.diseaseType = "Breast Cancer" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Cheyrl graph" AND d.diseaseType = "Breast Cancer" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Pamela graph" AND d.diseaseType = "Breast Cancer" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```

### 3/ Add 3 male patients (Parick, John, Michael) with the relationship to ”Prostate Cancer”
