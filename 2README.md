# YouTube Trending Videos Analysis (India)

This is a beginner-level data science project where I analyzed YouTube trending video data from India.  
It's my attempt to explore, clean, and gain insights using Python and Pandas.

---

## Dataset

- File used: INvideos.csv (Indian YouTube trending data)
- Columns include: title, channel_title, views, likes, and more

---

## What I Did

### 1. Cleaned the Data  
- Removed rows with missing values using dropna().

### 2. Explored the Data  
- Displayed dataset info using df.info() to get a feel of what I'm working with.

### 3. Analyzed Top 10 Most Viewed Videos  
```python
df.sort_values(by='views', ascending=False).head(10)

### 4. Found the most viewed channel

###calcilated Like-Views rati to find twhuch videos had the better content

df['channel_title'].value_counts().head(1)
df['likes_to_views_ratio'] = df['likes'] / df['views']
