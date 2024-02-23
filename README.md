# Hair Loss Analysis

## Table of Content

 - [Project](#project-overview)
 - [Data Source](#data-source)
 - [Questions to Explore](#questions-to-explore)
   - [Query Sample](#query-sample)
 - [Key Findings](#key-findings)
 - [Visualization](#visualization)
 - [Conclusion](#conclusion)
 - [Links](#links)

## Project Overview

I opted to go for Hair Loss Analysis project with aims to explore the factors contributing to hair loss and understand their impact on hair health. By leveraging data analysis techniques and visualization tools, the project seeks to uncover patterns, correlations, and insights that can inform strategies for managing and mitigating hair loss.

## Data Source

The project utilizes a dataset sourced from Kaggle, containing information on various factors potentially influencing hair health. The dataset includes attributes such as genetics, hormonal changes, medical conditions, medications and treatments, nutritional deficiencies, stress levels, age, poor hair care habits, environmental factors, smoking habits, weight loss, and hair loss severity. [Data Source](https://www.kaggle.com/datasets/amitvkulkarni/hair-health/data)

## Questions to Explore

1. What is the distribution of hair loss severity among different age groups?
2. Are certain medications and treatments associated with increased or decreased hair loss severity?
3. Is there a correlation between stress levels and the severity of hair loss?
4. How do factors, such as genetics, hormonal changes, environmental changes, smoking, poor hair care habits and weight loss, contribute to hair loss severity?
5. Are individuals with specific medical conditions more likely to experience hair loss?

### Query Sample

4. How do factors, such as genetics, hormonal changes, environmental changes, smoking, poor hair care habits and weight loss, contribute to hair loss severity?
```
SELECT
    CORR(CASE WHEN genetics = 'Yes' THEN 1 ELSE 0 END, hair_loss::integer) AS genetic_correlation,
	CORR(CASE WHEN weight_loss = 'Yes' THEN 1 ELSE 0 END, hair_loss::integer) AS weight_loss_correlation,
	CORR(CASE WHEN hormonal_changes = 'Yes' THEN 1 ELSE 0 END, hair_loss::integer) AS hormonal_changes_correlation,
	CORR(CASE WHEN poor_hair_care_habits = 'Yes' THEN 1 ELSE 0 END, hair_loss::integer) AS poor_hair_care_habits_correlation,
	CORR(CASE WHEN environmental_factors = 'Yes' THEN 1 ELSE 0 END, hair_loss::integer) AS environmental_correlation,
	CORR(CASE WHEN smoking = 'Yes' THEN 1 ELSE 0 END, hair_loss::integer) AS smoking_correlation
    
FROM  predict_hair_fall;
```

## Key Findings

**Stress and Hair Loss:** High stress levels correlate with increased hair loss severity, emphasizing the importance of stress management for maintaining healthy hair.

**Genetic Predispositions:** Certain genetic factors may contribute to hair loss susceptibility, highlighting the role of genetics in hair health.

**Effectiveness of Treatments:** Certain medications and treatments show associations with hair loss severity, suggesting varying effectiveness in addressing hair loss.

**Nutritional Deficiencies:** Nutritional deficiencies, such as vitamin and mineral deficiencies, are identified as potential contributors to hair loss, underscoring the significance of a balanced diet for hair health.

**Medical Conditions:** Specific medical conditions, such as Androgenetic Alopecia, Psoriasis, and Alopecia Areata, are associated with increased hair loss severity, indicating the impact of underlying health conditions on hair health.

**Age-Related Patterns:** Hair loss severity varies across different age groups, with older demographics exhibiting higher rates of hair loss, indicating age-related factors influencing hair health.


## Visualization

The Hair Loss Analysis Dashboard provides an interactive visualization of factors contributing to hair loss. Users can explore various dimensions such as stress levels, genetics, hormonal changes, smoking habits, environmental factors, poor hair care habits, weight loss, and hair loss due to medical conditions. The dashboard aims to uncover patterns and correlations between these factors and hair loss severity.
![1](https://github.com/Sanjeev-Lama/Hair-Loss-Analysis/assets/158605914/9c8229bb-2592-4612-9245-93c24c4bc8f4)



## Conclusion

This project has delved into various facets of hair health and loss, shedding light on the intricate interplay of factors influencing hair conditions. Through meticulous data preparation, exploratory analysis, and statistical examinations using tools like PostgreSQL and Tableau, we have unearthed significant findings. High stress levels, genetic predispositions, specific medical conditions, and nutritional deficiencies have emerged as crucial contributors to hair loss severity, underscoring the multifactorial nature of this phenomenon. 

Additionally, insights gleaned from age-related patterns highlight the dynamic changes in hair health across different life stages. By synthesizing these insights, individuals can better understand the complexities of hair loss and make informed decisions regarding stress management, lifestyle choices, and treatment strategies to nurture healthier hair. 

The interactive visualizations crafted in Tableau, showcased in the Hair Loss Analysis Dashboard, serve as a powerful tool for disseminating these insights and empowering individuals to take proactive steps towards preserving and enhancing their hair health.

## Links
Help from [ChatGPT](https://chat.openai.com/share/181a28ed-3537-443d-9eec-ed6dd99ea794)
Full Queries [Here](https://docs.google.com/document/d/1wTqrQ5PP8jc8IcAaxmM6ubTsI3z7qkYxejxAlaWYGUs/edit?usp=sharing)
[Tableau Dashboard](https://public.tableau.com/app/profile/sanjeev.lama/viz/HairLoss/Dashboard1?publish=yes)
