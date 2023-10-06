### Goul:

Our main goal in collecting the Arab Employee dataset is to learn more about what affects how much Arab professionals get paid. We want to gather information about their qualifications, where they live, and how much experience they have. This data will help organizations and policymakers make better decisions about managing talent, planning for the future workforce, and making sure pay is fair in the Arab region.

### Here are two specific goals we have for this dataset:

**Classification Goal**: We want to group employees into different categories based on their qualifications, country location, and experience. By doing this, we can see patterns and trends among different groups. This will help us understand if there are differences in pay based on qualifications and experience, and it will help us identify talented individuals. With this information, we can develop strategies to support career growth and make sure people are being paid fairly.

**Defect Prediction Goal:** We want to use machine learning and statistical techniques to create models that can predict any issues or anomalies with employee salaries. This could include things like unfair pay practices, wage gaps, or differences based on qualifications or experience. By catching these problems early, we can fix them and make sure everyone is being treated fairly. This analysis will help us improve compensation policies and make better decisions about managing talent.

#### By achieving these goals, we can:

Understand how salaries are distributed among different employee groups. Identify any biases or unfairness in pay based on qualifications, experience, or location. Develop strategies for hiring, developing, and keeping talented employees. Make sure pay practices are fair and transparent. Catch and fix salary-related issues before they become bigger problems. Plan for the future workforce and allocate resources effectively. Make better decisions about pay and talent management in the Arab region. Overall, collecting the Arab Employee dataset with information about salary, qualifications, location, and experience is really important. It will help us analyze the data and make fair decisions that create a good working environment for Arab professionals.

**Source of the dataset:** Kaggle

**link of the dataset:** <https://www.kaggle.com/datasets/qusaybtoush1990/employes>

### General Information about Employees dataset:

Our dataset contains 10 attributes (See Table 1), and 740 objects. Furthermore, class lables the class label for our dataset is Salary.

*Table 1: General Information about the attributes for Employees dataset.*

| **Attributes name** | **Description**                   | **Data type** | **Possible values**                  |
|------------------|-------------------|------------------|------------------|
| ID                  | Employee id                       | Nominal       | 6 values                             |
| Education           | Education level for the employee  | Nominal       | Prof-Doctor-Bachelor\...             |
| Department          | Department that employee works in | Nominal       | FSL-NEI-IT\...                       |
| Job status          | Employment situation              | Nominal       | Full time-part time-cotract          |
| Location            | The location of the job           | Nominal       | saudi arabia-United Arab Emirates... |
| Start date          | Date to start the job             | Nominal       | 7Jan11-1Jan20                        |
| Years               | Years of work                     | Numeric       | 0-9                                  |
| Salary              | Salary of the employee            | Numeric       | 650-25000                            |
| Job rate            | Employee evaluation               | Numeric       | 1-13                                 |
| Permission          | The access rights and privileges  | Numeric       | 1-14                                 |

---
title: "R Notebook"
output: html_notebook
---
#Sample of row
```{r}
View(Employees)

```

#statiscal summarise -Nominal-
```{r}
summary(Employees$Education)
```

```{r}
summary(Employees$Department)
```

```{r}
summary(Employees$'Job Status')
```

```{r}
summary(Employees$Location)
```

#statiscal summarise -Numerical-
```{r}
summary(Employees$Years)
```

```{r}
summary(Employees$Salary)
```

```{r}
summary(Employees$'Job Rate')
```

```{r}
summary(Employees$Permissions)
```

#Code for variance
```{r}
var(Employees$Salary)
```

#Graphs

#Boox plot for salary and years
```{r}
boxplot(Employees$Salary)
```
Description for Salary boxplot:
The Salary boxplot illustrates that there are no outliers in Salary attribute, and it shows that the salaries are evenly distributed around the middle point, indicating a relatively balanced salary distribution.

```{r}
boxplot(Employees$Years)
```
Description for Years boxplot:
The Years of Work boxplot illustrates how the values in the dataset have relatively balanced around the median value of 4. Also, there are no outliers found. So, no need for preprocessing.
```{r}
boxplot(Employees$'Job Rate')
```
Description for Job rate boxplot:
The Job rate boxplot is relatively balanced around the median value of 5. In a more comprehensive analysis, no outliers exist in the Job rate attribute. However, there is a spread in the job rates above 50% of the dataset.

```{r}
boxplot(Employees$Permissions)
```
Description for Permissions boxplot:
The Permissions boxplot reveals several important insights about the distribution of Permissions. It illustrates that the values of the attribute are almost balanced near to the median. In addition to this, there is no outliers that must be removed in preprocessing stage.

#Histogram for permission 
```{r}
Permissions <- Employees$Permissions
hist(Permissions)
```
Description for Permissions histogram.:
The frequency of Permissions for the employees in the dataset is represented by the histogram. After observation, we noticed that the most values lie in approximately from 1 permission to 2. As for the rest of the employees, their Permissions range from 3 to 14 permission.

# pie chart fo job status 
```{r}
tab <- Employees$'Job Status' %>% table()
precentages <- tab %>% prop.table() %>% round(3) * 100 
txt <- paste0(names(tab), '\n', precentages, '%') 
pie(tab, labels=txt)
```
Description for Job Status pie chart:
The pie chart shows that more than half of the employees work as a full-time jub. In addition to this, it will helps us determine salaries for each employee according to their Job Status.

#Bar chart for Education 
```{r}
bb <- Employees$Education %>% table() %>% barplot(axisnames=F, main='Education', ylab='Frequency',col=c('pink', 'blue', 'lightgreen'))
text(bb, tab/2, labels=txt, cex=0.5)
```
