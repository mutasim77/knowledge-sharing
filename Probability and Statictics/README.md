<p align="center">
   <img src="https://github.com/mutasim77/knowledge-sharing/assets/96326525/222d4c2b-8771-4f8d-9afe-54991b348646"/>
</p>

# Foundations of Probability and Statistics 🧮 

Hey there! This is my handbook where I share what I've learned about `Statistics and Probability`. I'll explain things in the simplest and easiest 
way possible. Also, let's see about why math, statistics, and probability are super important in computer 
science(in some fields). Some people(like me before), might think math is useless, but actually, math is everything and everywhere. 
Let's get started:

## Table of Contents: 📜
- [Introduction to Probability and Statistics 📊](#introduction-to-probability-and-statistics-)
- [Types of Statistical Analysis 📈](#types-of-statistical-analysis-)
- [Techniques of Sampling 🎯](#techniques-of-sampling-)
- [The Measure of Center of Tendency 🎯](#the-measure-of-center-of-tendency-)
- [The Measure of Dispersion 📏](#the-measure-of-dispersion-)


## Introduction to Probability and Statistics 📊
Probability and statistics are like the tools in a detective's kit, helping us make sense of the world's mysteries by providing clues and evidence. Probability deals with the likelihood of events occurring, similar to predicting the chances of certain outcomes. Meanwhile, statistics is like a magnifying glass, allowing us to closely examine data to uncover hidden patterns and trends.

#### Analogy: 🪄
Imagine you're planning a picnic, and you want to know the likelihood of it raining. Probability is like checking the weather forecast to estimate the chances of rain. If the forecast says there's a 30% chance of rain, you can use that probability to decide whether to bring an umbrella or not.

#### Real-world Example: 🌍 
Consider a `coin` toss. When you flip a fair coin, there are two possible outcomes: `heads` or `tails`. The probability of getting `heads` is `1/2` (or 0.5), and the probability of getting `tails` is also `1/2` (or 0.5). This simple example demonstrates how probability helps us understand the likelihood of outcomes in random events.

In statistics, let's say you're analyzing the grades of students in a class. By collecting and analyzing the data, you can calculate measures like the average grade, the most common grade, or the spread of grades. These statistics provide valuable insights into the performance of the class and help make decisions about teaching methods or curriculum adjustments.

Probability and statistics work hand in hand to provide us with tools to understand uncertainty and make informed decisions in various aspects of our lives, from weather forecasting to business planning.

---

## Types of Statistical Analysis 📈
There are two main statistical methods used in data analysis(There are actually more types, but we're focusing on these for now.):

### Descriptive Statistics: 📊📉
**Descriptive statistics** are like taking a snapshot of your data. They help you summarize and describe the main features of a dataset in a simple and straightforward way. It's like looking at a photo album that gives you a quick overview of what's inside. For example, if you're studying the incomes of people in a city, you might use descriptive statistics to find out the average income, the range of incomes, and how spread out the incomes are. It's all about giving you a clear picture of what your data looks like without getting into complex analysis.

### Inferential Statistics: 🎲🔮
**Inferential statistics** take you beyond the data you have and into the realm of making educated guesses or predictions about a larger population based on a sample. It's like being a detective who uses clues to solve a mystery. For instance, imagine you have a bowl of candies, but you can only see a few candies at a time. Based on those few candies, you try to make an educated guess about the entire bowl's composition. Similarly, with inferential statistics, you use the information from a `sample` to make conclusions or predictions about the entire `population`. For example, if you have data on the test scores of a group of students, you might use inferential statistics to make predictions about the performance of all students in the school. It's about using the power of probability and logic to draw conclusions that extend beyond the data you have.

![Descriptive_statistics_and_inferential_statistics](https://datatab.net/assets/tutorial/Descriptive_statistics_and_inferential_statistics.png)

---

### Samples and Populations: 📋🌍

#### Sample: 📋🔍
A sample is a subset of the population that we observe or collect data from. It's like a smaller group selected from the larger population to study specific characteristics or behaviors. 

#### Population: 🌍🔍
The population is the entire group we want to draw conclusions about. It includes every individual or element that meets the criteria of interest. The population represents the bigger picture from which the sample is drawn. 

### Techniques of Sampling 🎯
Sampling techniques are methods used to pick a group of individuals or items from a larger population. Different techniques are used depending on what you're studying and who you're studying.
1. **Simple Random Sampling:** 🎩
   - Like drawing names out of a hat, every person or item in the population has an equal chance of being chosen.

3. **Stratified Sampling:** 🎯
   - The population is divided into different groups based on specific traits, and then random samples are chosen from each group.

5. **Cluster Sampling:** 🌐
   - The population is split into clusters or groups, and then some of those clusters are randomly picked. Everyone in the chosen clusters is included in the sample.

4. **Systematic Sampling:** 📝
   - Individuals or items are picked at regular intervals from a list or sequence, like every 5th person or item.
5. **Convenience Sampling:** 🚶‍♂️
   - People or items are chosen based on easy access, which might not give a fair representation of the whole population.

---

## The Measure of Center of Tendency 🎯
When we talk about the center of a set of numbers, we're looking for a representative value that summarizes where most of the data points lie. There are three common measures we use:

### Mean (Average): 🧮
- The mean is simply the sum of all the numbers in a dataset divided by the total count of numbers. It gives us a general idea of the typical value in the dataset.
- **Formula:** `Mean (μ) = (Sum of all numbers) / (Total count of numbers)`
- **Example:** Consider the following set of numbers: 3, 5, 7, 9, 11. To find the mean, we add up all the numbers (3 + 5 + 7 + 9 + 11 = 35) and then divide by the total count of numbers (5). So, the mean is 35 / 5 = 7.

### Median: 📏
- The median is the middle value when the dataset is arranged in `ascending or descending order`. If there's an even number of data points, the median is the average of the two middle values.
- **Example:** Let's use the same set of numbers: 3, 5, 7, 9, 11. When arranged in ascending order, the `middle value` is 7. So, the median is 7.
- **Note:** If we had an `even number` of data points, say, 3, 5, 7, 9, 11, 13, then the median would be the `average of the two middle values: (7 + 9) / 2 = 8`.

### Mode: 📊
- The mode is the value that appears most frequently in the dataset. A dataset can have one mode, more than one mode (if multiple values occur with the same highest frequency), or no mode at all if all values occur with equal frequency.
- **Example:** Consider the set of numbers: 3, 5, 5, 7, 9, 11, 11, 11. Here, the number 11 appears most frequently, so the mode is 11.

---

## The Measure of Dispersion 📏
When we talk about dispersion, we're referring to how spread out or varied the data points are in a dataset. It tells us about the variability or diversity of the values. There are several measures we use to quantify dispersion:

### Range: 📏
- The range is the simplest measure of dispersion. It's the difference between the `largest` and smallest values in the dataset. It gives us an idea of how spread out the entire range of values is.
- **Formula:** `Range = Largest value - Smallest value`

### Variance: 📊
- Variance measures the `average squared` deviation from the `mean`. It tells us how much each data point differs from the `mean` on average. A higher variance indicates greater dispersion.
- **Formula:** `Variance = Σ((xi - μ)^2) / n`

### Standard Deviation: 📈
- The standard deviation is the `square root of the variance`. It gives us a measure of the average deviation of data points from the mean. A larger standard deviation implies greater variability in the dataset.
- **Formula:** `Standard Deviation = √(Variance)`

### Interquartile Range (IQR): 📊
- The interquartile range is the `range of the middle 50%` of the data. It's the difference between the third quartile (Q3) and the first quartile (Q1). It's useful because it's not affected by extreme values or outliers.
- **Formula:** `IQR = Q3 - Q1`

These measures of dispersion help us understand how much the data points deviate from the central tendency measures like mean, median, and mode. They give us insights into the spread or variability within the dataset, which is crucial for making interpretations and decisions based on the data.
