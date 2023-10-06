# Data Scientist Project - Regional Survey Analysis

This project involves the analysis of a regional survey dataset. We explore various aspects of the data, including demographics, interests, and regional distributions.

## Table of Contents

- [Dataset Overview](#dataset-overview)
- [Data Cleaning](#data-cleaning)
- [Data Exploration](#data-exploration)
- [Data Visualization](#data-visualization)
- [Interest Analysis](#interest-analysis)
- [Age Categorization](#age-categorization)
- [Regional Analysis](#regional-analysis)
- [Contributing](#contributing)
- [License](#license)

## Dataset Overview

### Data Description

- **Data Type**: `pandas.core.frame.DataFrame`
- **Index**: RangeIndex with 425,332 entries from 0 to 425,331.
- **Columns (Total 9 Columns)**:
  1. `id`: 425,332 non-null entries with data type 'object'.
  2. `name`: 425,329 non-null entries with data type 'object'.
  3. `age`: 265,035 non-null entries with data type 'float64'.
  4. `age_range`: 265,035 non-null entries with data type 'object'.
  5. `province`: 317,301 entries with data type 'object'.
  6. `city`: 317,301 entries with data type 'object'.
  7. `gender`: 374,451 entries with data type 'object'.
  8. `interest`: 425,332 entries with data type 'object'.
  9. `interest_detail`: 122,838 entries with data type 'object'.

This provides detailed information about the dataset, including data types, the number of entries, and missing data in each column.

### Missing Data

To identify missing data in each column, we calculate the count of missing values:

```python
# Calculate missing data in each column
missing_data = dataset.isna().sum()
print(missing_data)
```

Here are the results:

- Column "id" has no missing data (missing data count = 0).
- Column "name" has 3 missing data.
- Column "age" has 160,297 missing data.
- Column "age_range" also has 160,297 missing data.
- Column "province" has 108,031 missing data.
- Column "city" also has 108,031 missing data.
- Column "gender" has 50,881 missing data.
- Column "interest" has no missing data (missing data count = 0).
- Column "interest_detail" has 302,494 missing data.

This information is essential for determining the next steps in data processing, such as handling or filling missing data.

## Data Cleaning

Based on the analysis, we have decided to remove the "interest_detail" column as it can be represented by the "interest" column, and the "age" column can be represented by the "age_range" column. After removing rows with missing values and duplicates, we proceed with the cleaned dataset.

## Data Exploration

We explore various aspects of the dataset, including gender distribution, age range distribution, and regional analysis.

- **Gender Distribution**: We visualize the distribution of gender using a pie chart.

![Gender Distribution](images/gender_distribution.png)

- **Age Range Distribution**: We visualize the distribution of age ranges using a count plot.

![Age Range Distribution](images/age_range_distribution.png)

## Data Visualization

We perform regional analysis by grouping data by province and city. We create pie charts to show the distribution of cities within each province.

## Interest Analysis

We analyze common interests using word clouds. We visualize common interests in Jawa Barat and Jawa Tengah.

![Common Interests in Jawa Barat](images/wordcloud_jabar.png)

![Common Interests in Jawa Tengah](images/wordcloud_jateng.png)

## Age Categorization

We categorize ages into different groups (e.g., Gen Z, Gen Millennial, Gen X, Baby Boomers, Gen Alpha) and visualize the distribution.

![Age Category Distribution](images/age_category_distribution.png)

## Regional Analysis

We perform regional analysis for specific provinces, such as Jawa Barat and Jawa Tengah, and visualize gender and age range distributions.

## Contributing

If you would like to contribute to this project, please open an issue or submit a pull request. We welcome contributions from the community.

## License

This project is licensed under the [Your License](LICENSE).

```