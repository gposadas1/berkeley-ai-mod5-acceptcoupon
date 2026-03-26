# Coupon Acceptance Prediction (Module 5)

## 📌 Overview
This project addresses Module five requirements.  It analyses the acceptance rate of two coupon types from dataset from the UCI Machine Learning repository that was collected via a survey on Amazon Mechanical Turk.  Coupon type 'Bar' was analyzed by following assignment prompts.  Coupon type 'Carry out & Take away' was analyzed individually by following Bar coupon analysis as analysis guide.

This work was completed as part of the UC Berkeley Machine Learning & AI program.

---

## 📊 Dataset
This data comes to us from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios including the destination, current time, weather, passenger, etc., and then ask the person whether he will accept the coupon if he is the driver. Answers that the user will drive there ‘right away’ or ‘later before the coupon expires’ are labeled as ‘Y = 1’ and answers ‘no, I do not want the coupon’ are labeled as ‘Y = 0’. There are five different types of coupons -- less expensive restaurants (under 20), coffee houses, carry out & take away, bar, and more expensive restaurants (
20 - $50).

The dataset includes user and contextual information such as:

- Demographics (age, income, marital status)
- Driving context (time of day, destination, passengers)
- Coupon type (restaurant, coffee house, etc.)
- Historical behavior (frequency of visits)

Data file not loaded to avoid large file load.


---

## 📓 Notebooks
https://github.com/gposadas1/berkeley-ai-mod5-acceptcoupon/blob/main/notebooks/01_prompt.ipynb


---
## 🎯 Problem Statement
What are the factors that determine whether a driver accepts the coupon once it is delivered to them?

- Which features have higher influence of coupon acceptance?
- Which groups withing fetures are more likely to accept coupon? 


---

## 🧠 Summary of Findings (Carry out & Take away)
Summary of findings for independent investigation for coupon type 'Carry out & Take away'.

- Acceptance rate for lower education levels is much greater than higher education levels.  There is a 28.4% difference in acceptance rate between Some Highschool and Graduate degree with Some High School having an acceptance rate of 93.8%

- Combining features gender and marital status reveal large acceptance differences between Male_Divorced acceptance rate of 96% and Femal_Devorced rate of 65.1% a difference of 30.9%.  Also, between Femal_Widowed  with acceptance rate of 89.5% and Male_Widowed with acceptance rate of 71.4 a difference of 18.1.

- Original hypothesis was that convenience and drivers with kids would be more likely to accept coupon type. However, this was not supported by data.

  - Convenience
    - *direction_opp* had a higher acceptance rate than direction_same by 4.7% 
    - *time* does support original hypothesis noon and 6pm which are traditional meal times
  - Children
      - *has_children* - have and have not are only 0.8% apart in acceptance rate
      - *passenger* - when kids were the passenger this was actually the lowest acceptance rate of the group

### Next steps:
- Refine hypothesis based on findings.
- Find actual correlation to determine if findings are statisticaly relevant.
- Look for additional feature combinations which might expose high and low acceptance rate combined groups (like gender_maritalStatus).
- Determin if findings support creation of predictive model


---

## 🛠️ Tech Stack
- Python
- Pandas
- NumPy
- Matplotlib / Seaborn