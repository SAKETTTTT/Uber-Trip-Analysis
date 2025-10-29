# Uber Trip Analysis

## Overview
This project analyzes Uber trip data to extract meaningful insights about ride patterns, purposes, and timing. The analysis includes data preprocessing, visualization, and feature engineering to understand various aspects of Uber rides.

## Dataset
The dataset (`UberDataset.csv`) contains information about Uber trips with the following features:
- START_DATE: Start time of the trip
- END_DATE: End time of the trip
- CATEGORY: Purpose category (Business/Personal)
- START: Starting location
- STOP: Destination location
- MILES: Distance traveled in miles
- PURPOSE: Specific purpose of the trip

## Features
- Data cleaning and preprocessing
- Handling missing values and duplicates
- Date-time feature engineering
- Categorical data encoding
- Visualization of trip patterns
- Analysis of trip purposes and categories
- Day/Night pattern analysis

## Technologies Used
- Python 3.x
- Libraries:
  - pandas: Data manipulation and analysis
  - numpy: Numerical computations
  - matplotlib: Data visualization
  - seaborn: Statistical data visualization
  - scikit-learn: Machine learning tools (for one-hot encoding)

## Installation
1. Clone this repository
```bash
git clone https://github.com/SAKETTTTT/Uber-Trip-Analysis.git
```

2. Install required packages
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

## Usage
1. Open `UberData-2.ipynb` in Jupyter Notebook or VS Code with Jupyter extension
2. Ensure `UberDataset.csv` is in the same directory
3. Run the cells sequentially to perform the analysis

## Analysis Highlights
- Trip categorization by purpose and business/personal use
- Temporal analysis showing trip patterns across different times of day
- Distance analysis for different trip purposes
- Visualization of key patterns and trends

## Visualizations
The notebook includes several visualizations:
- Distribution of trip categories
- Day/Night pattern analysis
- Purpose-wise trip distribution
- Category-wise purpose analysis

## Contributing
1. Fork the repository
2. Create a new branch for your feature
3. Commit your changes
4. Push to the branch
5. Create a new Pull Request

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details

## Author
- [@SAKETTTTT](https://github.com/SAKETTTTT)

## Acknowledgments
- Data provided by Uber
- Inspiration from various data analysis projects
- Open source community for the amazing tools and libraries