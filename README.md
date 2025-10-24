# 🎬 Netflix Dataset Analysis

A comprehensive data analysis project exploring Netflix's content library, uncovering insights about content distribution, ratings, release trends, and geographical patterns.

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Latest-green.svg)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Latest-orange.svg)
![Seaborn](https://img.shields.io/badge/Seaborn-Latest-yellow.svg)

---

## 📊 Project Overview

This project performs an in-depth exploratory data analysis (EDA) on a Netflix dataset containing 7,789 titles. The analysis reveals patterns in content production, popular genres, rating distributions, and temporal trends in Netflix's content strategy.

### Key Findings
- 📈 Analyzed **4,811 titles** after data cleaning
- 🎥 **97% Movies** vs **3% TV Shows** in the dataset
- 🌍 **United States** leads content production with 1,655 titles
- ⭐ **TV-MA** is the most common rating (1,668 titles)
- 📅 Peak content release observed around **2019-2020**

---

## 🎯 Features

- **Data Cleaning & Preprocessing**: Handled missing values across multiple columns (Directors, Cast, Country, etc.)
- **Statistical Analysis**: Comprehensive descriptive statistics and value counts
- **Temporal Analysis**: Yearly trends of content releases
- **Geographical Insights**: Top content-producing countries
- **Duration Analysis**: Average duration by genre with intelligent season-to-minutes conversion
- **Visual Analytics**: Multiple chart types including heatmaps, pie charts, line plots, and lollipop charts

---

## 🛠️ Technologies Used

- **Python 3.8+**
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Matplotlib**: Data visualization
- **Seaborn**: Statistical visualizations
- **Jupyter Notebook**: Interactive development environment

---

## 📁 Dataset Information

**Original Shape**: 7,789 rows × 11 columns  
**After Cleaning**: 4,811 rows × 11 columns

### Columns:
- `Show_Id`: Unique identifier
- `Category`: Movie or TV Show
- `Title`: Content title
- `Director`: Director name(s)
- `Cast`: Main cast members
- `Country`: Country of production
- `Release_Date`: Release date on Netflix
- `Rating`: Content rating (TV-MA, PG-13, etc.)
- `Duration`: Runtime in minutes or number of seasons
- `Type`: Genre categories
- `Description`: Content synopsis

---

## 📈 Visualizations

The project includes several insightful visualizations:

1. **Rating Distribution by Category**: Countplot showing rating patterns for Movies vs TV Shows
2. **Top 20 Content-Producing Countries**: Horizontal countplot
3. **Genre Duration Analysis**: Pie chart of top 10 genres by average duration
4. **Rating vs Duration Heatmap**: Correlation between content ratings and duration
5. **Temporal Trends**: Line plot showing yearly content release patterns
6. **Top 10 Countries**: Lollipop chart for better visual impact

---

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/netflix-analysis.git
cd netflix-analysis
```

2. Install required packages
```bash
pip install -r requirements.txt
```

3. Launch Jupyter Notebook
```bash
jupyter notebook
```

4. Open `Netflix_Analysis.ipynb` and run all cells

---

## 💡 Key Insights

### Content Distribution
- Movies dominate Netflix's library at 97.2% of all content
- The United States produces more content than the next 4 countries combined

### Rating Patterns
- Mature content (TV-MA) is most prevalent, indicating Netflix's focus on adult audiences
- TV-14 and R ratings follow as the next most common categories

### Temporal Trends
- Significant growth in content additions from 2015 onwards
- Peak content release period observed in January 2020

### Duration Analysis
- Average movie duration: **~102 minutes**
- Intelligent conversion of TV show seasons to equivalent minutes for comparison
- Drama and International genres have the longest average durations

---

## 📊 Sample Code Snippet

```python
# Duration conversion logic for TV shows
mean_duration = df.loc[df['Duration'].str.contains('min', na=False), 
                       'Duration_num'].mean()

def convert_duration(x):
    if 'min' in x:
        return int(x.replace('min', '').strip())
    elif 'Season' in x:
        n_seasons = int(''.join(filter(str.isdigit, x)) or 1)
        return n_seasons * mean_duration
```

---

## 🎓 Skills Demonstrated

- Data Cleaning & Preprocessing
- Exploratory Data Analysis (EDA)
- Statistical Analysis
- Data Visualization
- Python Programming
- Pandas & NumPy Operations
- Problem-solving (duration conversion logic)

---

## 📝 Future Enhancements

- [ ] Add sentiment analysis on descriptions
- [ ] Implement machine learning models for content recommendation
- [ ] Create interactive dashboards using Plotly/Dash
- [ ] Analyze correlation between cast/director and content success
- [ ] Time series forecasting for future content trends

---

## 👤 Author

**Ramya Rastogi**

- GitHub: [@ramya-rastogi](https://github.com/ramya-rastogi)
- LinkedIn: [Ramya Rastogi](https://www.linkedin.com/in/ramya-rastogi)

