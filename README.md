<br/>
<p align="center">
  <a href="https://github.com/erkutkoral/Diabetes-FeatureEngineering">
    <img src="https://www.wallstreetmojo.com/wp-content/uploads/2023/05/Feature-Engineering.png" alt="Logo" width="600" height="400">
  </a>

  <h3 align="center">Diabetes Feature Engineering</h3>

  <p align="center">
    Performed EDA, Data Preprocessing, Feature Engineering, Modeling and Feature Importance steps in Kaggle's Titanic Dataset.Let's get started.
    <br/>
    <br/>
    <a href="https://github.com/erkutkoral/Diabetes-FeatureEngineering"><strong>Explore the docs »</strong></a>
    <br/>
    <br/>
    <a href="https://github.com/erkutkoral/Diabetes-FeatureEngineering/issues">Report Bug</a>
    .
    <a href="https://github.com/erkutkoral/Diabetes-FeatureEngineering/issues">Request Feature</a>
  </p>
</p>

![Contributors](https://img.shields.io/github/contributors/erkutkoral/Diabetes-FeatureEngineering?color=dark-green) ![Issues](https://img.shields.io/github/issues/erkutkoral/Diabetes-FeatureEngineering) 

## Table Of Contents

* [About the Project](#about-the-project)
* [Technologies-Libraries-Frameworks](#technologies-libraries-frameworks)
* [Roadmap](#roadmap)
* [Conclusion](#conclusion)
* [Authors](#authors)

## About The Project

The sinking of the Titanic is one of the most infamous shipwrecks in history. On April 15, 1912, during her maiden voyage, the widely considered “unsinkable” RMS Titanic sank after colliding with an iceberg. Unfortunately, there weren’t enough lifeboats for everyone onboard, resulting in the death of 1502 out of 2224 passengers and crew. While there was some element of luck involved in surviving, it seems some groups of people were more likely to survive than others.

## Technologies-Libraries-Frameworks

Python Libraries: Numpy, Pandas, Matplotlib, Seaborn, Scikit-Learn.

## Roadmap

1. Exploratory Data Analysis
2. Base Model
3. Handling Missing Values
4. Handling Outliers
5. Feature Extraction
6. Feature Importance

## Conclusion
- **Exploratory Data Analysis Insights:**
  - There are no duplicate rows.
  - Pregnancies: It has a right-skewed distribution. There are too many observations with 0 values in the variable. It may also be normal to have an observation with a value of 0 in this variable that defines the number of pregnancies.
  - Glucose: The variable distribution is very close to the normal distribution except for observations with a value of 0, and a person with a Glucose value of 0 does not make sense. These observations may be direct errors or outliers.
  - When we subtract 1.5 IQR from the Q1 value, we get a value greater than 0. This structure is not a outlier. There may be a missing value.
  - Similar structures exist in BloodPressure, SkinThickness, Insulin and BMI variables. The conclusion drawn here is that observations with a value of 0 are missing observations. These variables also contain contradictory observations.
  - Pregnancies variable has a 60% positive correlation with the Age variable.
  - Glucose variable has a 50% positive correlation with the target variable.
  - The SkinThickess variable has a positive correlation of nearly 50% with the Insulin and BloodPressure variables.

- **Feature Engineering Insights**:
  - Examined outliers with a box plot, but the box plot calculates outliers based on 25% - 75% quarters. - Outliers were suppressed by 5% - 95% in order not to affect the distribution in the data set too much.
  - There was no missing observation structure in the data set, but it was seen from the distributions and structure that the values were related to missing observations.0 values were changed to nan and suppressed with the median to avoid affecting the distribution.
  - 8 new variants were produced, these are:
    - Categorical Age: 21-50 --> mature 50+ --> senior
    - Categorical BMI: 18,5 < underweight, 18.5 - 24.9 --> normal, 24.9 - 29.9 --> Overweight and 30+ Obese
    - Categorical Glucose: Normal, Prediabetes, Diabetes
    - Categorical Age x BMI: underweightmature, underweightsenior, healthymature, healthysenior, overweightmature, overweightsenior, obesemature, obesesenior
    - Categorical Age x Glucose: lowmature, lowsenior, normalmature, normalsenior, hiddenmature, hiddensenior, highmature, highsenior
    - Categorical Insulin: Normal, Abnormal
    - Glucose x Insulin
    - Glucose x Pregnancies
    - Glucose x Insulin and Glucose x Pregnancies variables have become high-performance variables.
  - Some classes did not affect performance in the Age x Glucose variable.
  - One class did not affect performance in the Age x BMI variable


## Authors

* **Erkut Koral** - [LınkedIn](https://www.linkedin.com/in/erkutkoral/)
