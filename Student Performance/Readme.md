# Student Performance Visualization Project

## Project Overview
The project examines student academic performance trends based on an exam score and demographic data dataset.
The objective is to exercise a three-step workflow — **ingest → process → analyze** — and generate understandable, reproducible visualizations.
Five research questions are limited to specific domains of investigation where data cleaning, visualization, and interpretation provide the answer.

---
## Dataset
- **Source**: Students Performance dataset (CSV file provided).  
- **Size**: ~1,000 records, each containing exam scores and student attributes.  
- **Attributes**:
  - Gender  
  - Race/ethnicity  
  - Parental level of education  
  - Lunch type (standard vs free/reduced)  
  - Test preparation course (completed vs none)
- Scores in **math**, **reading**, and **writing**  

The raw dataset is stored in:  

---

## ⚙️ Workflow

### 1. Ingestion
- Imported the dataset using `pandas`.  
- Verified the shape, columns, and data types.  
- Checked for missing values (none were found).  

### 2. Preprocessing
- Cleaned column names where necessary.
- Assigned a new variable `overall_avg = (math + reading + writing) / 3` to be used later.
- Converted all scores to numeric format.

### 3. Analysis & Visualization
Five of the questions of study were answered using visualizations:

1. V1 — Math vs Reading Gender Differences 

This visualization compares the distribution of math and reading scores between male and female students using side-by-side boxplots.
Each box shows the median, interquartile range, and potential outliers for each subject by gender.
From the plot, we can typically see that female students tend to perform slightly higher in reading, while male students often have marginally higher math scores.
The spread of scores also indicates the variability within each gender group.
A wider box means more variation in performance, while a narrow box means more consistent scores.
The median line helps identify which gender performs better in each subject overall.
This plot helps identify performance gaps that may be influenced by learning preferences or social factors.
Overall, it visually summarizes gender-based performance differences across core subjects.

V2 — Test Preparation Impact on Math

This chart compares math scores of students who completed a test preparation course with those who did not.
It helps determine whether participation in test prep programs has a measurable impact on math performance.
Usually, students who completed test prep show a higher median score and a smaller spread, indicating both improvement and consistency.
The “no test prep” group often has a wider range of scores and a lower median.
This suggests that structured preparation can boost performance in quantitative subjects.
The chart helps educators assess the effectiveness of test prep interventions.
It can also highlight the value of additional support programs for low-performing students.
Overall, the visualization provides a clear comparison of math achievement based on preparation level.

V3 — Type of Lunch and Average Performance 

This visualization displays the average overall scores (combining math, reading, and writing) grouped by type of lunch.
Typically, “standard lunch” students outperform those receiving “free/reduced lunch.”
This pattern may reflect socioeconomic differences that influence access to educational resources.
Each bar shows the mean score for each subject category, grouped by lunch type for easy comparison.
The gap between the bars demonstrates how nutrition and financial stability might relate to academic outcomes.
This visualization emphasizes the potential link between socioeconomic status and learning performance.
It can help schools identify areas where additional academic or nutritional support might be needed.
Overall, it provides insight into how external factors beyond the classroom affect student achievement.

V4 — Subject Correlations 

The heatmap shows the correlation coefficients among math, reading, and writing scores.
Each cell represents how strongly two subjects are linearly related, ranging from -1 (negative) to +1 (positive).
In most student performance datasets, all three subjects show strong positive correlations.
This means that students who perform well in one subject tend to perform well in the others.
The darkest color regions represent the strongest relationships, usually between reading and writing.
Math is slightly less correlated with language-based subjects but still shows a moderate positive relationship.
This correlation pattern suggests that general academic ability and study habits influence success across multiple domains.
Overall, the heatmap visually summarizes the interconnectedness of academic skills across different subjects.

V5 — Math vs Reading with Trend Lines by Test Preparation 

This scatterplot compares math and reading scores for all students, separated by test preparation status.
Each point represents an individual student’s scores in both subjects.
Two regression lines—one for students who completed test prep and one for those who did not—show the general performance trends.
The slope and position of these lines help determine whether test prep improves both math and reading simultaneously.
Typically, the “completed test prep” group has a higher intercept, meaning they start from stronger overall performance levels.
A tighter cluster of points around the line suggests more consistent outcomes for prepared students.
In contrast, the “no prep” group might show a wider spread, indicating greater variability in performance.
Overall, this visualization highlights how preparation impacts overall academic consistency and cross-subject improvement.

All the plots are **800×600 px, 300 DPI** with appropriate titles, axis labels, legends, and legible ticks.

