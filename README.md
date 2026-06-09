# ENGR 102 Lab Topic 5 (optional)

## Activities
This **optional** lab consists of one activity. Please submit the following file to Gradescope.

1. [Diabetes Risk](#diabetes-risk)

## Diabetes Risk
Early detection and treatment of type 2 diabetes is important to help reduce the risk of serious complications such as premature heart disease and stroke, blindness, limb amputations, and kidney failure. This score was developed to identify people at risk of having undetected diabetes. It is based on routinely collected information (age, sex, BMI, steroid/antihypertensive medication use, family history of diabetes, and smoking history).

Parameters used in the calculation, parameter (value):
- Sex: Female (0.879), Male (0)
- BMI: Under 25 (0), 25 to 27.49 (0.699), 27.5 to 29.99 (1.97), 30+ (2.518)
- Hypertension medication: On medication (1.222), Not medicated (0)
- Steroids: On medication (2.191), Not medicated (0)
- Smoker: Non-smoker (0), Used to smoke (-0.218), Smoker (0.855)
- Family history: None (0), Parent or sibling (0.728), Parent and sibling (0.753)

Calculation:

$$n = 6.322 + sex - (0.063 * age) - BMI - hypertension - steroids - smoker - history$$

$$risk = 100 / (1 + e^n)$$

Write a program named `diabetes_risk.py` that calculates the risk of developing type-2 diabetes based on user input.

Example output (using inputs: `F`, `37`, `26`, `n`, `n`, `n`, `n`):
```
Enter your sex (M/F): F
Enter your age (years): 37
Enter your BMI: 26
Are you on medication for hypertension (Y/N)? n
Are you on steroids (Y/N)? n
Do you smoke cigarettes (Y/N)? n
Did you used to smoke (Y/N)? n
Do you have a family history of diabetes (Y/N)? n
Your risk of developing type-2 diabetes is 1.5%
```

Revised Summer 2026 SNR
