# Will the Customer Accept the Coupon?

## Project Overview

This project analyzes customer coupon acceptance behavior using data from a survey conducted on Amazon Mechanical Turk. The goal is to identify patterns and characteristics that distinguish customers who accept driving coupons from those who don't.

## Dataset Description

The dataset contains survey responses describing different driving scenarios including:
- **Contextual factors**: destination, weather, time, temperature, passenger
- **User demographics**: age, gender, marital status, education, occupation, income
- **User behavior**: frequency of visits to bars, coffee houses, restaurants
- **Coupon details**: type (Bar, Coffee House, Restaurant<$20, Restaurant $20-$50, Carry out & Take away), expiration time

The target variable `Y` indicates whether the customer accepted the coupon (1) or not (0).

## Key Findings

### Overall Coupon Acceptance
- **Overall acceptance rate**: ~57% of customers accepted coupons
- **Most popular coupon types**: Coffee House and Restaurant(<$20) coupons

### Bar Coupon Analysis

Drivers who accepted bar coupons showed distinct patterns:

1. **Frequency matters**: Customers who visit bars more than 3 times a month have a significantly higher acceptance rate (~77%) compared to those visit 3 or fewer times (~37%)

2. **Age and frequency**: Drivers over 25 who go to bars more than once a month show a much higher acceptance rate (~69%) compared to all others (~34%)

3. **Occupation and passengers**: Drivers who go to bars more than once a month, don't have kids as passengers, and work in non-farming/fishing/forestry occupations have higher acceptance rates

4. **Combined factors**: The highest acceptance rates are seen when multiple favorable conditions align:
   - Frequent bar-goers (>1/month) who are under 30
   - Frequent bar-goers with non-kid passengers who aren't widowed
   - Frequent restaurant-goers (<$20) with income <$50K

**Hypothesis**: Bar coupon accepters are typically younger, social individuals who already frequent bars regularly and are likely driving without children. They view the coupon as an opportunity to continue their regular social habits.

### Coffee House Coupon Analysis

For coffee house coupons, distinct patterns emerged:

1. **Overall acceptance**: Coffee house coupons have an acceptance rate of ~50%

2. **Frequency impact**: Regular coffee house visitors (4+ times/month) show a much higher acceptance rate (~68%) vs. infrequent visitors (~43%)

3. **Time of day**: Morning coupons (7AM, 10AM) have higher acceptance rates (~55%) compared to afternoon/evening (~47%)

4. **Passenger influence**: Drivers alone or with friends are more likely to accept (~52%) vs. those with kids (~41%)

5. **Demographics**:
   - Students and young professionals (21-30) show the highest acceptance rates
   - Income level has a moderate positive correlation with acceptance
   - Singles and unmarried partners more likely to accept than married individuals

**Hypothesis**: Coffee house coupon accepters are likely busy professionals and students who already have coffee as part of their routine. They're more receptive during commute times (morning) and when not family obligations (driving kids).

## Project Structure

```
├── data/
│   └── coupons.csv          # Raw survey data
├── images/                   # Reference images for GitHub setup
├── visualizations/           # Generated plots and charts
├── prompt.ipynb              # Original assignment notebook
├── analysis.ipynb            # Complete data analysis notebook
└── README.md                 # This file
```

## Technologies Used

- **Python 3.x**
- **pandas**: Data manipulation and analysis
- **matplotlib**: Data visualization
- **seaborn**: Statistical data visualization
- **numpy**: Numerical computing

## How to Run

1. Clone this repository:
   ```bash
   git clone <your-repository-url>
   cd assignment5_1_starter
   ```

2. Install required packages:
   ```bash
   pip install pandas matplotlib seaborn numpy jupyter
   ```

3. Launch Jupyter Notebook:
   ```bash
   jupyter notebook analysis.ipynb
   ```

4. Run all cells to reproduce the analysis

## Analysis Methodology

1. **Data Exploration**: Examined dataset structure, missing values, and distributions
2. **Data Cleaning**: Handled missing values through appropriate imputation or removal
3. **Exploratory Analysis**: Created visualizations to understand patterns
4. **Targeted Analysis**: Deep-dived into specific coupon types (Bar, Coffee House)
5. **Statistical Comparison**: Compared acceptance rates across different customer segments
6. **Hypothesis Formation**: Developed data-driven hypotheses about customer behavior

## Future Work

- Develop a predictive model to forecast coupon acceptance
- Analyze seasonal and weather-based patterns more deeply
- Study the interaction effects between multiple variables
- Investigate the optimal coupon expiration times
- Create customer personas for targeted marketing

## Author

Built as part of UC Berkeley Professional Certificate in ML & AI coursework.

## License

This project is for educational purposes.
