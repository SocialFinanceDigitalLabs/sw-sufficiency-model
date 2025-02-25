# RCC v1 Dataset

## Overview
This repository contains the **RCC v1 dataset**, which includes structured data related to [briefly describe the dataset purpose]. The data is stored in an Excel file (`RCC_v1.xlsx`) with multiple sheets.

## File Contents
The dataset consists of the following sheets:
- **Sheet1**

### Columns in the Main Sheet (`Sheet1`)
Here are the key columns available in the main sheet:
- `Section`
- `Field`
- `Description`
- `Options`
- `Stage of data collection (Home search or IPA)`
- `Example`
- `TYPE (string, category, free etc etc) `

## Sample Data
Below is a preview of the dataset:

```markdown
| Section               | Field                                       | Description                                                                                                                                       | Options            | Stage of data collection (Home search or IPA)   | Example             | TYPE (string, category, free etc etc)    |
|:----------------------|:--------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------|:------------------------------------------------|:--------------------|:-----------------------------------------|
| Identifying the child | Child ID                                    | Please enter the unique ID used in your Case Mgmt System                                                                                          | ID no.             | Home search                                     | 12346               | integer                                  |
| nan                   | Local Identifier                            | Whatever ID you use to refer to the child (e.g. initials). This is not used in the data analysis.                                                 | free text          | Home search                                     | TR                  | String                                   |
| nan                   | Is this a planned or emergency home search? | Please specify whether or not this is an emergency search.                                                                                        | Planned/ emergency | Home search                                     | Planned             | Boolean                                  |
| nan                   | Latest date for placement to start by​       | What date does the child need to find a home/ be placed by? If no exact date specified, please add an approximate.                                | date               | Home search                                     | 2024-03-30 00:00:00 | date                                     |
| nan                   | Number of siblings to place with            | How many siblings does the child have to be placed together with? If child has no siblings/ does not need to be placed with siblings then input 0 | number             | Home search                                     | 2                   | integer                                  |
```

## Usage Instructions
To use this dataset:
1. **Download the file** from GitHub.


