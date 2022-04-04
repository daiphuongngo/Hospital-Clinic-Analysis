# Hospital-Clinic-Analysis

## Overview

This repository contains the analysis of a basic Hospital / Clinic's dataset to demonstrate skills: creating nodes on Graph and retrieve insights on Neo4j in Cypher and applying the same way in SQL on Azure to design tables and retrieve insights

## Languages and Tools:

- `Cypher`

- `Graph`

- `Neo4j`

- `SQL` (in progress)

- `Azure` (in progress)

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

![3 males prostate cancer](https://user-images.githubusercontent.com/70437668/161479087-f6c96b38-e5ae-4f53-b895-b9181bfc84a9.jpg)

```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Patrick graph" AND d.diseaseType = "Prostate Cancer" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "John graph" AND d.diseaseType = "Prostate Cancer" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Michael graph" AND d.diseaseType = "Prostate Cancer" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```

### 4/ Andrew has “Obesity”, ”Diabetes”, ”Chrons”. 
![Andrew](https://user-images.githubusercontent.com/70437668/161479513-1c783a34-4561-4b25-982b-d8ccc81cb1bc.jpg)

```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Andrew graph" AND d.diseaseType = "Obesity" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Andrew graph" AND d. diseaseType = "Diabetes" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Andrew graph" AND d. diseaseType = "Crohns Disease" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```

### Henry has “Lung cancer”, ”Pancreatic”.
![Andrew](https://user-images.githubusercontent.com/70437668/161479520-a5866aed-d646-474b-98fb-fc6b5c946132.jpg)

```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Henry graph" AND d. diseaseType = "Lung Cancer" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Henry graph" AND d. diseaseType = "Pancreatic Cancer" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```


### Betty has “Lung Cancer”, “Diabetes”. 
![Andrew](https://user-images.githubusercontent.com/70437668/161479526-de80a79c-c062-4a9d-a5e4-c420b115d932.jpg)

```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Betty graph" AND d. diseaseType = "Lung Cancer" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```
```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Betty graph" AND d. diseaseType = "Diabetes" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```

### Theresa has “Crohns”. 
![Theresa](https://user-images.githubusercontent.com/70437668/161479532-2a4fd2f3-84da-4df8-b431-9f54b217f074.jpg)

```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Theresa graph" AND d. diseaseType = "Crohns Disease" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```

### Claudette has “Diabetes”.
![Claudette](https://user-images.githubusercontent.com/70437668/161479541-6b0b4813-9df8-4e1c-884a-e14706412799.jpg)

```
MATCH (p:Patient), (d:Disease) WHERE p.fullName = "Claudette graph" AND d. diseaseType = "Diabetes" 
CREATE (p)-[r: Has_Disease]->(d) 
RETURN p, d
```

### 5/ Create the relationship “Treats_Disease” associate the two specialists with “Breast Cancer”, ”Pancreatic Cancer”, ”Lung Cancer”, ”Prostate Cancer”. 

![4 doctors](https://user-images.githubusercontent.com/70437668/161480044-213c12a6-0330-44f7-b192-15928a223a1b.jpg)

#### Dr Moses & Dr Susan
```
MATCH (dr:Doctor), (d:Disease) WHERE dr.Specialty = "Specialist" AND d. diseaseType = "Breast Cancer" 
CREATE (dr)-[r: Treats_Disease]->(d) 
RETURN dr, d
```
```
MATCH (dr:Doctor), (d:Disease) WHERE dr.Specialty = "Specialist" AND d. diseaseType = "Pancreatic Cancer" 
CREATE (dr)-[r: Treats_Disease]->(d) 
RETURN dr, d
```
```
MATCH (dr:Doctor), (d:Disease) WHERE dr.Specialty = "Specialist" AND d. diseaseType = "Lung Cancer" 
CREATE (dr)-[r: Treats_Disease]->(d) 
RETURN dr, d
```
```
MATCH (dr:Doctor), (d:Disease) WHERE dr.Specialty = "Specialist" AND d. diseaseType = "Prostate Cancer" 
CREATE (dr)-[r: Treats_Disease]->(d) 
RETURN dr, d
```

### Then associate the two Family Doctors  with “Heart Disease”, ”Kidney Disease”, ”Diabetes”, ”Blood Pressure”, ”Obesity”, ”Crohns Disease” 

#### Dr Ann & Dr Jones
```
MATCH (dr:Doctor), (d:Disease) WHERE dr.Specialty = "Family Doctor" AND d. diseaseType = "Heart Disease" 
CREATE (dr)-[r: Treats_Disease]->(d) 
RETURN dr, d
```

```
MATCH (dr:Doctor), (d:Disease) WHERE dr.Specialty = "Family Doctor"  AND d. diseaseType = "Kidney Disease" 
CREATE (dr)-[r: Treats_Disease]->(d) 
RETURN dr, d
```
```
MATCH (dr:Doctor), (d:Disease) WHERE dr.Specialty = "Family Doctor"  AND d. diseaseType = "Diabetes" 
CREATE (dr)-[r: Treats_Disease]->(d) 
RETURN dr, d
```
```
MATCH (dr:Doctor), (d:Disease) WHERE dr.Specialty = "Family Doctor" AND d. diseaseType = "Blood Pressure" 
CREATE (dr)-[r: Treats_Disease]->(d) 
RETURN dr, d
```
```
MATCH (dr:Doctor), (d:Disease) WHERE dr.Specialty = "Family Doctor" AND d. diseaseType =  "Obesity" 
CREATE (dr)-[r: Treats_Disease]->(d) 
RETURN dr, d
```
```
MATCH (dr:Doctor), (d:Disease) WHERE dr.Specialty = "Family Doctor" AND d. diseaseType = "Crohns Disease" 
CREATE (dr)-[r: Treats_Disease]->(d) 
RETURN dr, d
```

## Analytical Questions

### 1 - Which patients do “Dr Moses” treats? 

![Q1 - Dr Moses](https://user-images.githubusercontent.com/70437668/161480741-d1d9b8bb-b035-48c7-b71b-0a9a423913d9.jpg)

```
MATCH (dr:Doctor)-[:Treats_Disease]->(d:Disease)<-[:Has_Disease]-(p:Patient)
WHERE dr.Name = "Dr Moses"
RETURN DISTINCT dr.Name AS Doctor_Name,  p.fullName as Patient_Name
```

![Q1 - Dr Moses](https://user-images.githubusercontent.com/70437668/161480752-96895d6d-bfe4-4643-85d5-97936589a79c.jpg)

```
MATCH (dr:Doctor)-[:Treats_Disease]->(d:Disease)<-[:Has_Disease]-(p:Patient)
WHERE dr.Name = "Dr Moses"
RETURN DISTINCT dr, d, p
```


### 2 - Which doctors treat patients over 40, show the doctor’s name and patient name  
![Q1 - Dr Moses](https://user-images.githubusercontent.com/70437668/161480766-1407bff3-ea87-4ba6-9fd3-5645411e4b3a.jpg)

```
MATCH (dr:Doctor)-[:Treats_Disease]->(d:Disease)<-[:Has_Disease]-(p:Patient)
WHERE toInteger(p.Age) > 40
RETURN DISTINCT p.fullName as Patient_Name
```

![Q1 - Dr Moses](https://user-images.githubusercontent.com/70437668/161480775-dbe76b06-a408-4a26-9bfa-71e06676261b.jpg)

```
MATCH (dr:Doctor)-[:Treats_Disease]->(d:Disease)<-[:Has_Disease]-(p:Patient)
WHERE toInteger(p.Age) > 40
RETURN DISTINCT dr, d, p
```

### 3 - Find all the doctors that treat “Betty Johnson” and show what they are treating her for – show both the graph and then the table with doctor’s name, patient Name and Disease Type 

![Q1 - Dr Moses](https://user-images.githubusercontent.com/70437668/161480797-6b07c2c0-7b80-4aab-b5b3-34320c93ad56.jpg)

```
MATCH (dr:Doctor)-[:Treats_Disease]->(d:Disease)<-[:Has_Disease]-(p:Patient)
WHERE p.fullName = "Betty graph"
RETURN DISTINCT dr.Name AS Doctor_Name, p.fullName as Patient_Name, d.diseaseType as Disease_Type
```

![Q1 - Dr Moses](https://user-images.githubusercontent.com/70437668/161480803-d7d4e0ba-eca5-4e6f-b040-a4daf2ae2287.jpg)

```
MATCH (dr:Doctor)-[:Treats_Disease]->(d:Disease)<-[:Has_Disease]-(p:Patient)
WHERE p.fullName = "Betty graph"
RETURN DISTINCT dr, d, p
```


### 4 – Show me all the patients who have a female doctor

![Q4 - female doctor graph](https://user-images.githubusercontent.com/70437668/161480821-5f2692ba-a40b-4ed8-bd62-0c020e741630.jpg)

```
MATCH (dr:Doctor)-[:Treats_Disease]->(d:Disease)<-[:Has_Disease]-(p:Patient)
WHERE dr.Sex = "F"
RETURN DISTINCT dr, d, p
```

![Q4 - female doctor graph](https://user-images.githubusercontent.com/70437668/161480837-6b98dd4c-f134-445f-ae34-7df787368624.jpg)

```
MATCH (dr:Doctor)-[:Treats_Disease]->(d:Disease)<-[:Has_Disease]-(p:Patient)
WHERE dr.Sex = "F"
RETURN DISTINCT dr.Name AS Doctor_Name, p.fullName as Patient_Name, d.diseaseType as Disease_Type
```

### 5 – Show me all the patients who have a female doctor and that has any form of cancer 

![Q5 - female doctor cancer graph](https://user-images.githubusercontent.com/70437668/161480843-fc5209ec-1def-4e05-a870-6e739ecd12bf.jpg)

```
MATCH (dr:Doctor)-[:Treats_Disease]->(d:Disease)<-[:Has_Disease]-(p:Patient)
WHERE dr.Sex = "F" AND dr.Specialty = "Specialist"
RETURN DISTINCT dr, d, p
```

![Q5 - female doctor cancer graph](https://user-images.githubusercontent.com/70437668/161480852-d0edb47e-ee93-4e3e-88b3-ce1242a0742a.jpg)

```
MATCH (dr:Doctor)-[:Treats_Disease]->(d:Disease)<-[:Has_Disease]-(p:Patient)
WHERE dr.Sex = "F" AND dr.Specialty = "Specialist"
RETURN DISTINCT dr.Name AS Doctor_Name, p.fullName as Patient_Name, d.diseaseType as Disease_Type
```

