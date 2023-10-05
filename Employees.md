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

•	Sample of raw data:

<img width="676" alt="Screenshot 2023-10-05 221423" src="https://github.com/Wissayifmk/Employee-IT326/assets/144927134/4002dbec-3098-4855-8ed5-565c55103010">

•	Missing values:

<img width="182" alt="Screenshot 2023-10-05 222010" src="https://github.com/Wissayifmk/Employee-IT326/assets/144927134/d1370f5f-d56f-4b44-9d2c-8f034a8a3e4c">

•	Statistical measures:

<img width="368" alt="Screenshot 2023-10-05 222214" src="https://github.com/Wissayifmk/Employee-IT326/assets/144927134/532cc1dd-951f-4dc5-b7e8-6c363b5d7b6f">

Data preprocessing:
•	Checking for missing values:

<img width="199" alt="Screenshot 2023-10-05 223953" src="https://github.com/Wissayifmk/Employee-IT326/assets/144927134/e4f9413c-458e-42f4-ac68-f94d42adbbba">

•	Detecting and removing the outliers:
Detecting the outliers:

<img width="626" alt="Screenshot 2023-10-05 231058" src="https://github.com/Wissayifmk/Employee-IT326/assets/144927134/1b685fc7-1f4e-477b-b612-781453cbfcae">
<img width="622" alt="Screenshot 2023-10-05 231123" src="https://github.com/Wissayifmk/Employee-IT326/assets/144927134/0bdbbba2-d3af-4391-b84b-cb1c9ea583ac">


<img width="623" alt="Screenshot 2023-10-05 231825" src="https://github.com/Wissayifmk/Employee-IT326/assets/144927134/667ef30f-c45b-4a10-9826-440ed85ff1c9">
<img width="603" alt="Screenshot 2023-10-05 231932" src="https://github.com/Wissayifmk/Employee-IT326/assets/144927134/1140eb1d-2769-46d4-b083-027fd4f13648">

<img width="587" alt="Screenshot 2023-10-05 232300" src="https://github.com/Wissayifmk/Employee-IT326/assets/144927134/5170d5bb-601e-400b-8e17-460c4a742131">
<img width="577" alt="Screenshot 2023-10-05 232317" src="https://github.com/Wissayifmk/Employee-IT326/assets/144927134/8ad51a19-ebe1-40eb-b09e-22baa0b1f0e4">

Removing outliers:

<img width="284" alt="Screenshot 2023-10-05 232928" src="https://github.com/Wissayifmk/Employee-IT326/assets/144927134/413e80a9-69b4-4bc5-af35-1b3e3e60d0bf">

Data before removing the outliers:

<img width="579" alt="Screenshot 2023-10-05 232832" src="https://github.com/Wissayifmk/Employee-IT326/assets/144927134/f4f91b23-929d-408b-badf-33caf07486dd">
<img width="604" alt="Screenshot 2023-10-05 232843" src="https://github.com/Wissayifmk/Employee-IT326/assets/144927134/a362a22e-3eb8-4b23-9d42-1f0b36ad8ede">

Data after removing the outliers:

<img width="580" alt="Screenshot 2023-10-05 233203" src="https://github.com/Wissayifmk/Employee-IT326/assets/144927134/7e130351-38a5-48f0-a966-f739041e79cd">
<img width="616" alt="Screenshot 2023-10-05 233214" src="https://github.com/Wissayifmk/Employee-IT326/assets/144927134/1b4eebf9-2a02-4e50-bf16-2e8846894daf">
