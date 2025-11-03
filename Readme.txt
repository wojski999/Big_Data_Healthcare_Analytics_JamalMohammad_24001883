Project README – Big Data for Healthcare Analytics

Name: Jamal Mohammad
Student ID: 24001883
Course: Big Data Technologies and Applications
Instructor: Dr. [Instructor Name]
Submission Date: November 2025


This README provides a detailed explanation of the Big Data for Healthcare Analytics project developed by Jamal Mohammad (ID: 24001883) for the course Big Data Technologies and Applications. 
It covers the full workflow: dataset details, environment setup, Spark implementation, data analysis, visualizations, and results interpretation. The document ensures complete technical and conceptual understanding for replicating the entire project.


The dataset used contains 55,500 patient admission records with 14 attributes including demographic, clinical, and financial variables such as Age, Gender, Blood Type, Medical Condition, Admission Type, and Billing Amount.
Data preprocessing steps included removing negative values, converting dates to valid formats, and deriving a new variable Stay_Days to represent hospital duration. The dataset was verified for completeness and schema consistency.


### Environment Setup and Tools

The project was executed in Google Colab using Apache Spark (PySpark) for distributed data analysis. The environment was prepared with the following commands:

!apt-get install openjdk-11-jdk -qq
!pip install pyspark

SparkSession was created and the dataset loaded via:
from pyspark.sql import SparkSession
spark = SparkSession.builder.appName("HealthcareAnalytics").getOrCreate()
df = spark.read.csv("/content/healthcare_dataset_cleaned.csv", header=True, inferSchema=True)

All transformations and analytical operations were conducted using Spark’s DataFrame API, ensuring scalability and reproducibility.


### Workflow Summary

1. Data loading and schema verification.
2. Data cleaning and transformation (handling nulls, parsing dates, calculating Stay_Days).
3. Aggregation and grouping for analytical metrics.
4. Statistical summaries and correlation computations.
5. Visualization using Seaborn and Matplotlib after Spark-to-Pandas conversion.
6. Interpretation of trends and presentation of analytical insights.


### Analytical Findings

The analysis demonstrated several key insights:
- Obesity and Diabetes recorded the highest billing amounts (~25,800 USD average), confirming their high-cost nature.
- The mean patient age across all conditions was approximately 51 years, indicating prevalence of chronic conditions in middle-aged adults.
- Admission types were nearly balanced (Elective, Urgent, Emergency), showing efficient hospital management.
- Test results (Normal, Abnormal, Inconclusive) were evenly distributed (~33% each), confirming consistent diagnostic performance.
- The correlation between Age and Billing (r ≈ –0.004) and Stay_Days and Billing (r ≈ –0.006) revealed weak relationships, suggesting costs depend on treatment complexity more than demographics or stay duration.

PySpark’s distributed framework processed all operations within seconds, validating its capability for big data analytics even in a cloud notebook environment.


### Conclusion

This project successfully showcased how Apache Spark can be applied to healthcare analytics for large-scale data processing and visualization. The results underline the importance of big data tools in improving decision-making and operational efficiency in the healthcare sector. The consistent analytical results, uniform visual outputs, and data-driven conclusions align with the objectives of the Big Data Technologies and Applications course.


Authored by: Jamal Mohammad (ID: 24001883)
Course: Big Data Technologies and Applications
Instructor: Dr. [Instructor Name]
Institution: [University Name]
Submission: November 2025

All analysis, visualizations, and documentation in this README are original and developed solely for academic purposes.

