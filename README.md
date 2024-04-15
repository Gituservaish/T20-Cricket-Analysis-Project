# T20-Cricket Analysis - Overall Best 12 Players Selection Project


## Overview

This project aims to identify the overall best 12 players from the 2022 T20 World Cup cricket tournament based on their performance metrics. Python's pandas library is used for data transformation and manipulation, and the processed data is exported to CSV format. Power BI is then utilized for visualization and to determine the best 12 players.

### Table Of Contents
  - [Data Source](#data-source)
  - [Tools](#tools)
  - [Steps](#steps)
  - [Usage](#usage)
  - [Contributing](#contributing)
  - [Acknowledgments](#acknowledgments)

## Data Source

The data used for this project is sourced from [ESPN Cricinfo, codebasics.io]. It includes various performance metrics such as batting average, strike rate, bowling average, economy rate, etc., for players participating in the T20 World Cup 2022.

## Tools

- Python 
- Power BI

## Python Libraries Used

- **Pandas**: For data manipulation and transformation.

## Steps

1. **Data Collection**: Obtained the T20 World Cup 2022 curated json files from codebasics.io .
2. **Data Preprocessing**: Clean the data, handle missing values, and perform necessary transformations using Python pandas.
3. **Feature Engineering**: Compute additional metrics if required, such as player strikr rate, out/not-out on performance metrics.
4. **Export to CSV**: Export the processed data into a CSV file using pandas.
5. **Visualization in Power BI**: Import the CSV data into Power BI and create visualizations to determine the overall best 11 players.

## Usage

1. Import the required dependencies:

```bash
#import neccessary libraries
import pandas as pd
import json
```

2. Run the Python script to perform data processing and manipulation:

```bash
with open('t20_Json_files/t20_wc_batting_summary.json') as f:
    data = json.load(f)
    
    all_records = []
    
    for rec in data:
        all_records.extend(rec['battingSummary'])
        
df_batting = pd.DataFrame(all_records)
df_batting.head()
```

3. code for importing into csv
   
 ```python
   df_batting.to_csv('t20_csv_files/fact_batting_summary.csv')
   ```

4. Open Power BI and import the CSV file to create visualizations of the overall best 12 players.

   - **visuals**

   ![Cricket Analysis-1](https://github.com/Gituservaish/T20-Cricket-Analysis-Project/assets/160588103/38d7f9f2-6520-4fd4-9ea7-225af1ec44b0)
   
   ![Cricket Analysis-6](https://github.com/Gituservaish/T20-Cricket-Analysis-Project/assets/160588103/6e273127-1668-4f88-8216-e167147d5f2c)

   

## Contributing

Contributions are welcome! If you have any ideas for improvement or want to add new features, feel free to submit a pull request.


## Acknowledgments

- [ESPN Cricinfo](https://www.espncricinfo.com/) and [codebasics](https://codebasics.io/resources/data-analytics-project-for-beginners) for providing cricket statistics and data.

---
