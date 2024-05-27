# Introduction
This project aims to showcase proficiency in data cleaning and exploratory data analysis techniques using Python Pandas. Through various methodologies, the data was meticulously cleansed and scrutinized to unveil valuable patterns. An array of tools was leveraged throughout the project to accomplish these tasks effectively.

Check out the python file here: [Query folder](/Query/).

# Background
The dataset utilized in this project is a CSV file containing records of ultra marathon data. The dataset encompasses various information about the races and the participants, including race names, locations, dates, distances, times, and participants' demographics and performance.

You can access the raw data by following [this link](https://www.kaggle.com/datasets/aiaiaidavid/the-big-dataset-of-ultra-marathon-running/discussion/420633).

### Goals for this project:

1. **Demonstrate Proficiency:** Showcase adeptness in data cleaning and exploratory data analysis techniques, highlighting the ability to extract meaningful insights from raw datasets.
2. **Identify Patterns and Trends:** Utilize various analytical tools and methodologies to uncover notable patterns and trends within the dataset, focusing on participant demographics, race performances, and other relevant metrics.
3. **Inform Decision-Making:** Provide actionable insights by presenting clear and concise findings regarding ultra marathon data, facilitating informed decision-making processes.

# Tools I Used
During my thorough exploration of this data cleaning and exploratory data analysis endeavor, I utilized several essential tools to extract insights efficiently. These tools encompassed:

- **Python (Pandas)**: Essential for data manipulation and analysis, allowing for efficient data cleaning, transformation, and exploratory data analysis.
- **Jupyter Notebook**: Used for an interactive data analysis environment, facilitating the process of documenting and visualizing the analysis.
- **Git & GitHub**: Essential for version control and fostering collaboration, Git and GitHub facilitated seamless sharing of scripts and analyses, ensuring effective project tracking and collaborative workflows.

# Data Cleaning
The data cleaning phase of this project adhered to a structured process to ensure comprehensive consideration and implementation of crucial data cleaning procedures. The steps are as follows:

1. **Eliminate Duplicate Entries:** Ensure that there are no repeated records to maintain data integrity.
2. **Standardize Data:** Harmonize different formats and representations within the data.
3. **Handle Null and Empty Values:** Address missing values appropriately to prevent analysis inaccuracies.
4. **Eliminate Redundant Rows or Columns:** Remove unnecessary data to streamline analysis.

### 1. Eliminate Duplicate Entries
To eliminate duplicate entries, the dataset was checked for any repeated records based on relevant columns.

```python
# Remove duplicates
df.drop_duplicates(inplace=True)
```

### 2. Standardize Data
Standardizing data involved correcting inconsistencies within the dataset.

- **Trimming Whitespace:** Ensuring no extra spaces are present in string fields.
- **Consistent Formatting:** Harmonizing date formats and other categorical data representations.

```python
# Standardize data
df['column_name'] = df['column_name'].str.strip()
df['date'] = pd.to_datetime(df['date'], format='%Y-%m-%d')
```

### 3. Handle Null and Empty Values
Handling null and empty values involved strategies such as filling missing values with appropriate substitutes or removing records where critical data is missing.

```python
# Fill or drop null values
df['column_name'].fillna('Unknown', inplace=True)
df.dropna(subset=['important_column'], inplace=True)
```

### 4. Eliminate Redundant Rows or Columns
Removing redundant rows and columns streamlined the dataset for analysis.

```python
# Drop redundant columns
df.drop(columns=['redundant_column'], inplace=True)
```

# Exploratory Data Analysis
The objective of this section is to identify patterns within the data, which will facilitate the extraction of valuable insights.

### Participant Demographics
Analyzing participant demographics such as age, gender, and nationality provides insights into the diversity and characteristics of ultra marathon runners.

```python
# Participant demographics
age_distribution = df['age'].value_counts()
gender_distribution = df['gender'].value_counts()
```

### Race Performances
Examining race performance metrics such as completion times, distances, and participation rates can reveal trends and benchmarks in ultra marathon running.

```python
# Race performance metrics
average_time = df['time'].mean()
distance_distribution = df['distance'].value_counts()
```

### Geographic Analysis
Understanding the geographic distribution of races and participants helps identify popular locations and regional trends.

```python
# Geographic analysis
race_locations = df['location'].value_counts()
participant_nationalities = df['nationality'].value_counts()
```

### Temporal Trends
Analyzing the data over time reveals trends in race participation, performance improvements, and other temporal patterns.

```python
# Temporal trends
df['year'] = df['date'].dt.year
yearly_participation = df.groupby('year')['participant_id'].count()
```

# What I Learned
Throughout this project, I've gained valuable insights into analyzing ultra marathon data across various dimensions such as participant demographics, race performances, geographic distributions, and temporal trends. Here are some key takeaways:

1. **Data Cleaning Importance:** Ensuring data integrity through meticulous cleaning is crucial for accurate analysis.
2. **Demographic Insights:** Understanding participant demographics provides a comprehensive view of the community and trends within ultra marathon running.
3. **Performance Trends:** Analyzing race performances helps identify benchmarks and improvements over time.
4. **Geographic Patterns:** Geographic analysis reveals popular locations and regional participation trends.
5. **Temporal Analysis:** Observing trends over time offers insights into the evolution and growth of ultra marathon events.
6. **Python Proficiency:** Working with Python and Pandas for data manipulation and analysis has enhanced my proficiency in handling and analyzing large datasets.

# Conclusion
### Summarized Insight

1. **Participant Demographics:**
   - Age and gender distributions provide insights into the diversity of ultra marathon participants.
   - Analyzing nationalities helps understand the global appeal and participation in these events.

2. **Race Performance Trends:**
   - Average completion times and distance distributions reveal performance benchmarks.
   - Temporal analysis indicates trends and improvements in race performances over the years.

3. **Geographic Patterns:**
   - Identifying popular race locations and participant origins helps understand regional trends.
   - Geographic analysis supports event planning and marketing strategies.

4. **Temporal Trends:**
   - Trends in participation and performance over time provide insights into the growth and popularity of ultra marathons.

This project has deepened my understanding of data analysis techniques and their application in understanding the ultra marathon community. Through meticulous data cleaning and exploratory data analysis, valuable insights were extracted to inform decision-making processes and enhance our knowledge of ultra marathon events.

## Contact Information

For any questions or suggestions, feel free to reach out to:

- Name: James Onyejekwe
- Email: jj.onyejekwe@gmail.com
- GitHub: [jamesmuse02](https://github.com/jamesmuse02)