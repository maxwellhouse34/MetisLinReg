# Abstract

Every year, U.S. students are saddled with billions of dollars of student loan debt for undergraduate degrees. As the costs of these degrees skyrockets, their inherent value is called into question. Prospective high school students, their parents, and schools themselves all have a stake in a fair price for education.

The goal of this project is to identify the relative value of a particular college based on various metrics provided by the schools, focusing on tuition.

## Design

The project assumes that tuition price is the best representation of a school’s inherent value, hence it being the target variable. All U.S. Colleges offering a bachelor's degree will be used, to control for exchange rates and other factors.

## Data

The data for this project was scraped from the Integrated Postsecondary Education Data System within the National Center for Education Statistics, provided by the US Department of Education.
The following features were pulled for each college:
- School location
- Grad student count
- Public vs Private
- Population
- State
- Student to Faculty
- 2020-21 
  - Tuition (in and out of state)
  - Room and board and other on campus
  - Room and board and other off campus
  - Books
  - Other Costs
- Financial Aid
  - % receiving aid
  - Grants
- Loans
  - Average receiving aid
  - Grants
- Enrollment
  - Full time %
  - Gender
  - Race
  - Student age % (above/below24)
  - In-State
  - Out-State
- Applications
  - Male Submissions
  - Female Submissions
  - Male % Accepted
  - Female % Accepted
- Requirements:
  - GPA
  - Rank

- SAT/ACT
  - SAT
    - 25%
    - 75%
  - ACT
    - 25%
    - 75%
-Retention
  - First year
  - Graduation
    - M
    - F
- Athlete count
- On-Campus criminal count
Many of these features were dropped with practice.

## Algorithms:
Feature Engineering:
Dummy variables for school location
Clean/Dropped multi-percentage features into binary percentages
Tested multiple polynomial relationships
Created relationship features for population/financial aid, public/test scores, crime/population, interaction of demographics
Models:
Data was split into train and test sections using an 80/20 split. 5-fold cross validation was used to examine Linear Regression, Polynomial Regression, Lasso Regression, and Ridge Regression. Lasso was ultimately chosen for having a similar weight to the others, but greater explainability. All iterations of feature engineering were tested.

## Tools
Beautiful Soup and Regex to Scrape the data
Pandas and Python to clean and perform the analysis.
SciKitLearn was used for modeling
Matplotlib and Seaborn will be used to present my findings visually.
No other tools should be needed as the analysis should be relatively straightforward, but I am open to other tools for geolocating schools.

## Visualization

![Best Graph](https://user-images.githubusercontent.com/67508938/128523572-f1f80621-f235-4f01-9af4-80feb0fad0b9.png)


![Coefficients](https://user-images.githubusercontent.com/67508938/128523578-fce18588-49ec-404b-a833-68a1b9bd11ab.png)

Before examining public/private vs. test scores

![good](https://user-images.githubusercontent.com/67508938/128523605-14003751-0d11-4b6e-9704-86b71e8d1626.png)

After

![better](https://user-images.githubusercontent.com/67508938/128523576-1d187396-91a7-4b6d-aa48-a7cc0488b5ab.png)



