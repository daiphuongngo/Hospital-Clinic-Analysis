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

 Name | Age | Sex
------|------
Orren graph | 25 | M 
| Joe graph | 27 | M 
| Paul graph | 55 | M 
| David graph | 42 | M 
| Peter graph | 35 | M |
| Andrew graph | 26 | M |
| Henry graph | 29 | M |
| Patrick graph | 34 | M |
| John graph | 21 | M |
| Michael graph | 67 | M |
| Patsy graph | 44 | F |
| Joan graph | 55 | F |
| June graph | 33 | F |
| April graph | 22 | F |
| May graph | 12 | F |
| Betty graph | 19 | F |
| Theresa graph | 67 | F |
| Claudette graph | 88 | F |
| Cheryl graph | 27	| F |
Pamela graph | 73	| F |

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

### Create 4 doctors with 4 properties two should be family doctors and two should be specialists:

•	Name 
•	Age
•	Sex 
•	Speciality “Family Doctor”,” Specialist” 



