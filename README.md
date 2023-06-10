# Algorithmic Trading Bot
Module 14 Challenge

## Overview

The goal of this project is to use machine learning to create a trading bot that learns and adapts to new data and evolving markets. This project can be broken down into 3 sections:
1. Build an algorithmic trading strategy that utlizes machine learning to automate trade decisions
2. Optimize the trading algorithm by adjusting the input parameters
3. Train a new model and compare its performance to a baseline model (the first model built)

## Installation

This project uses Python 3.9 and requires the following packages:
- pandas
- numpy
- hvplot
- scikit-learn
- matplotlib

To install the above packages, please run the following commands in your terminal: 
```python
pip install pandas
pip install numpy
pip install scikit-learn
pip install matplotlib
pip install hvplot
```

## Results

**Baseline Performance**

![actual_vs_strategy_returns](https://github.com/jonnycw/Module_14_Challenge/assets/120538932/c8f6268a-5667-4812-b261-d7bef3ae4132)

According to the plot, the baseline model performed similarly to that of the actual results until about half-way through 2018. At that point, the baseline model outfperformed the actual results. The SVM model produced higher results than the actual returns.

 **Tuned Period**
 
![actual_vs_strategy_returns_tuned_period](https://github.com/jonnycw/Module_14_Challenge/assets/120538932/2cf88887-5e6c-46be-8447-8916dea5f0ac)

The strategy with the longest training window (6 months) had significantly higher returns than the other two strategies and significally outperformed the actual returns.

**Tuned Window**

![actual_vs_strategy_returns_tuned_window](https://github.com/jonnycw/Module_14_Challenge/assets/120538932/7e6d06b8-8022-4377-babd-61a3d7cdadcb)

Doubling the SMA windows had a significant negative impact on returns and products a result that is similar to multiplying the original strategy by -1.

**LogisticRegression**

![actual_vs_strategy_returns_lr](https://github.com/jonnycw/Module_14_Challenge/assets/120538932/0288b6fe-feb3-436e-a41e-912cc91c1287)

The LogisticRegression strategy produced similar results to the actual returns until Q3 of 2017. From the end of 2017 to mid-2018, the strategy underperformed against the actual results. I believe it's important to note that from 2019 to mid-2020, the strategy significantly outperformed the actual results. The strategy ended up underperforming in 2021.


## Summary

The tuned period with a 6-month training window provided the best cumulative results. Doubling the SMA window producted the worst results, and the LogisticRegression was the least consistent strategy out of the 4. Next steps for this project would be to further investigate and tune the Tuned Period strategy with 6-month training window.

