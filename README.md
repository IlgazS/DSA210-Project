# YouTube Watch History Analysis
**DSA210: Introduction to Data Science Course Project**  
Sabanci University Fall 2024  

## Project Overview  
This project is part of the **DSA210: Introduction to Data Science** course at Sabanci University. The primary goal is to analyze my personal YouTube watch history to uncover insights about my viewing patterns, habits, and interests. Using data collected via Google Takeout, I performed exploratory data analysis (EDA) to identify trends in my behavior and understand how external factors like time of day or academic commitments might influence my choices.  

---

## Table of Contents  
- [Motivation](#motivation)  
- [Data Source](#data-source)  
- [Data Analysis Techniques](#data-analysis-techniques)  
- [Visualizations](#visualizations)  
- [Findings](#findings)  
- [Limitations and Future Work](#limitations-and-future-work)  

---

## Motivation  
I wanted to explore my interaction with YouTube, one of the platforms I use frequently, and gain deeper insights into my preferences, time management, and habits. By analyzing my watch history, I aimed to answer specific questions about my interests, time-based patterns, and how my viewing habits evolve under different circumstances, such as during an academic semester.  

---

## Data Source  
The data was obtained via [**Google Takeout**](https://takeout.google.com/), which provides YouTube watch history in an HTML format. Additional video details were fetched using the **YouTube API**, including metadata such as video duration, category, and tags. The dataset includes records from **July to December 2024** and consists of the following fields:  
- `videoURL`, `title`, `channelName`, `timeWatched`, `tags`, `duration`, `categoryName`, `publishedAt`, `defaultAudioLanguage`, `viewCount` and more.  

The final dataset was structured as a pandas DataFrame after preprocessing.  

---

## Data Analysis Techniques  
### Data Processing [Extraction Script](Data_Extraction.ipynb)
- Extracted HTML data and transformed it into a structured tabular format.
- Merged metadata fetched via the YouTube API.
- Preprocessed columns like `tags` and `duration` for further analysis.  

### Data Analysis and Visualizations [Analysis Script](Data_Analysis.ipynb)
The analysis was conducted using Python libraries such as pandas, seaborn, matplotlib, and plotly. Specific techniques included:  
- **Exploratory Data Analysis**: Identified trends in time of day, day of the week, and categories.  
- **Statistical Tests**: Evaluated hypotheses such as differences in video duration on weekends vs. weekdays.  

---

## Visualizations  
### Key Visualizations  
1. 
3. **Watch frequency over the hours of the day**  
   ![Polar Chart](PolarChart.png)  
4. **Distribution of tags across day segments (morning vs. night)**  
   ![Sankey Diagram](SankeyDiagram.png)  
5. **Proportion of "Education" videos before and during the academic semester**
   ![Slope Chart](slope_chart.png)  
6. **Frequently occurring words in video titles**  
   ![Word Cloud](word_cloud.png)  
7. **Total number of videos watched per month by category**  
   ![Stacked Bar Chart](stacked_bar_chart.png)  
8. **Video duration vs. view count** 
   ![Scatterplot](ScatterPlot.png)  
9. **Video duration on weekdays vs. weekends**  
   ![Boxen Plot](BoxenPlot.png)  
10. **Percentage of videos watched by category**  
   ![Pie Chart](PieChart.png)  
 

---

## Findings  
### Time-Based Patterns  
- **Daily Routines**: Most active viewing times were late evening and night, peaking between 8 PM and 12 AM.  
- **Weekend vs. Weekday**: Video durations differed significantly, with longer videos watched on weekends (p < 0.05).  

### Content Preferences  
- **Categories**: Dominant categories included "People & Blogs" (39%) and "Entertainment" (26%).  
- **Tags**: Morning and night viewing had distinct tag distributions, as highlighted in the Sankey diagram.  

### Behavioral Insights  
- **Academic Influence**: Proportion of "Education" videos slightly decreased during the semester.  

---

## Limitations and Future Work  
### Limitations  
- **Data Range**: The dataset spans only six months, limiting insights into long-term patterns.  
- **Granularity**: YouTube does not provide data on how much of each video was watched.    

### Future Work  
- **Yearly Trends**: Collect data over a full year for comprehensive insights.  
- **Advanced Analytics**: Incorporate machine learning for content recommendation analysis.  
- **Visualization Enhancements**: Build an interactive dashboard to make findings more accessible.  

---

This analysis offered valuable insights into my YouTube habits and preferences. For further details, please explore the scripts and visualizations in this repository.  
