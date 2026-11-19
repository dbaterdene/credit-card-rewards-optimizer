# Credit Card Rewards Optimizer

## Project Overview

The **Credit Card Rewards Optimizer** is a Python-based data analytics project that evaluates credit card rewards based on consumer spending habits.

The project compares credit cards using spending categories, reward rates, annual fees, and welcome bonuses to estimate which card provides the highest financial value.

It also tests different consumer spending profiles to demonstrate how the best credit card can change depending on individual spending behavior.

## Business Problem

Choosing a credit card can be difficult because different cards offer different rewards, fees, and introductory bonuses.

A card with a higher reward rate does not always provide the highest overall value after considering annual fees and spending patterns.

This project addresses the following business questions:

- Which credit card provides the highest annual net value?
- How do annual fees affect the value of credit card rewards?
- How much do welcome bonuses contribute to first-year value?
- Which cards perform best for different spending categories?
- How does the best card change across consumer spending profiles?

## Project Objectives

1. Collect and organize credit card reward information.
2. Analyze consumer spending across different categories.
3. Calculate annual rewards and net financial value.
4. Compare first-year value with ongoing annual value.
5. Perform spending scenario analysis.
6. Create visualizations and an interactive dashboard.
7. Communicate findings through data-driven recommendations.

## Tools and Technologies

| Tool | Purpose |
|---|---|
| Python | Data analysis and calculations |
| Pandas | Data cleaning and manipulation |
| NumPy | Numerical analysis |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization library |
| Plotly | Interactive dashboard |
| CSV | Data storage |
| Git and GitHub | Version control and project sharing |

## Dataset

The project uses two main datasets.

**1. Consumer Spending Profile**

Contains monthly spending estimates for:

- Groceries
- Dining
- Gas
- Travel
- Bills
- Other purchases

**2. Credit Card Information**

Contains:

- Credit card name
- Annual fee
- Reward rates by spending category
- Welcome bonus value
- Welcome bonus spending requirement
- Official issuer source URL
- Data verification date

The current spending profile is illustrative. Credit card terms should be checked against the official issuer pages before relying on the results.

## Methodology

### 1. Data Validation

The project checks:

- Missing values
- Duplicate records
- Invalid spending amounts
- Invalid reward rates
- Missing source URLs
- Data verification status

### 2. Annual Spending Calculation

Annual spending is calculated as:

Annual Spending = Monthly Spending × 12

### 3. Annual Rewards Calculation

Annual Rewards = Sum of (Annual Category Spending × Category Reward Rate)

### 4. Ongoing Net Value

Ongoing Net Value = Annual Rewards − Annual Fee

### 5. First-Year Net Value

First-Year Net Value = Annual Rewards + Eligible Welcome Bonus − Annual Fee

### 6. Scenario Analysis

The model compares different consumer spending profiles:

- Average Consumer
- Grocery and Dining Consumer
- Frequent Traveler
- Gas and Commuting Consumer

## Key Findings

Using the current illustrative spending profile and simplified reward-rate assumptions:

- Wells Fargo Active Cash generates approximately $439.20 in annual rewards.
- Capital One Savor generates approximately $435.60 in annual rewards.
- Chase Freedom Unlimited generates approximately $383.40 in annual rewards.

Assuming the welcome bonus requirements are met and annual fees remain $0:

- Wells Fargo Active Cash has an estimated first-year value of $539.20.
- Capital One Savor has an estimated first-year value of $635.60.
- Chase Freedom Unlimited has an estimated first-year value of $583.40.

These results demonstrate that the card with the highest ongoing rewards may differ from the card with the highest first-year value.

**Important:** These are model estimates, not personalized financial recommendations. They depend on the spending profile, reward-rate assumptions, offer eligibility, and redemption conditions.

## Visualizations

The project generates the following charts:

- Annual Net Value Comparison
- Annual Rewards vs. Annual Fees
- Rewards by Spending Category
- Spending Scenario Comparison

Chart files are stored in the `figures/` directory.

## Interactive Dashboard

The project includes a Plotly dashboard with interactive comparisons of:

- First-year net value
- Ongoing annual net value
- Annual rewards, fees, and welcome bonuses
- Net value across spending scenarios

Dashboard file:

`reports/credit_card_dashboard.html`

## Project Structure

```text
credit-card-rewards-optimizer/
│
├── data/
│   ├── raw/
│   │   ├── spending_profile.csv
│   │   └── credit_cards.csv
│   └── processed/
│
├── figures/
│
├── notebooks/
│
├── reports/
│
├── src/
│   ├── validate_data.py
│   ├── calculate_rewards.py
│   ├── create_visualizations.py
│   ├── scenario_analysis.py
│   ├── advanced_rewards_analysis.py
│   └── create_dashboard.py
│
├── .gitignore
├── README.md
└── requirements.txt
```

## Limitations and Assumptions

The current model uses simplified reward-rate assumptions. It does not fully model:

- Merchant category code restrictions
- Spending caps and rotating reward categories
- Travel portal booking requirements
- Reward redemption restrictions and changing point values
- Interest charges and credit card balances
- Foreign transaction fees
- Welcome bonus eligibility rules and qualifying purchase exclusions
- The exact timing of purchases during a welcome bonus period

Welcome bonus eligibility is estimated from average spending and should not be interpreted as guaranteed qualification.

## Future Improvements

- Add more credit cards from different issuers.
- Model spending caps and rotating reward categories.
- Improve welcome bonus eligibility calculations using transaction-level spending.
- Add multiple-card optimization.
- Add interactive spending inputs.
- Incorporate more detailed reward redemption assumptions.
- Automate updates from official credit card issuer sources.

## Author

**Data Analytics Portfolio Project**

Developed to demonstrate skills in Python, data cleaning, financial analysis, scenario modeling, data visualization, and business decision-making.

