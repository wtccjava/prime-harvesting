This is a series of retirement financial simulations and investigations, initially
inspired by Michael McClung's book [Living Off Your Money].

[Living Off Your Money]: https://www.amazon.com/Living-Off-Your-Money-Retirement/dp/0997403411

QUICKSTART
==========

 $ virtualenv .
 $ bin/pip install --requirement requirements.txt
 $ bin/jupyter-notebook


JUPYTER NOTEBOOKS
=================
- [Prime Harvesting][1]. The one that started the project. A comparison of Prime Harvesting and
  Annual Rebalancing. [Blog post][Medium prime].
- [EM vs. VPW][2]. A comparison of portfolio values and incomes for EM and VPW (from bogleheads).
- [Inverted Withdrawals][3]. A look at [Inverted Withdrawals][inverted] and [blog post][Medium inverted].
- [Liability Matching Portfolio][4]. _Haven't done anything with this one yet..._
- [Sleep Well At Night][5]. A first look at bond levels with Prime Harvesting. [Blog post][Medium averages].
- Monthly Harvesting. The difference between checking annually and checking monthly. [Blog post][Monthly harvesting].

[1]: https://github.com/hoostus/prime-harvesting/blob/master/Prime%20Harvesting.ipynb
[2]: https://github.com/hoostus/prime-harvesting/blob/master/EM%20vs%20VPW.ipynb
[3]: https://github.com/hoostus/prime-harvesting/blob/master/Inverted%20Withdrawal%20Rates.ipynb
[inverted]: http://www.advisorperspectives.com/articles/2016/05/17/inverted-withdrawal-rates-and-the-sequence-of-returns-bonus
[Medium inverted]: https://medium.com/@justusjp/inverted-withdrawals-and-risk-aversion-8d165247c92a#.x6u540qsn
[4]: https://github.com/hoostus/prime-harvesting/blob/master/LMP.ipynb
[5]: https://github.com/hoostus/prime-harvesting/blob/master/Sleep%20Well%20At%20Night.ipynb
[Medium averages]: https://medium.com/@justusjp/prime-harvesting-bond-levels-the-problem-with-averages-7a21518b6f57#.8c7mk68y5
[Medium prime]: https://medium.com/@justusjp/prime-harvesting-vs-rebalancing-graphs-2687930a995b#.enlcxwdny
[Monthly harvesting]: https://medium.com/@justusjp/prime-harvesting-with-monthly-vs-annual-returns-64d6d748c36f#.yt519zjoq

DATA SOURCES
============
CSV imports are easier for the code to deal with, so I've frequently munged original
data source into CSV files.

- [1871_returns.csv] comes from Simba's backtesting spreadsheet on [bogleheads][6]
- [2004-period-life-table.csv] comes from https://www.kitces.com/joint-life-expectancy-and-mortality-calculator/
- [PortfolioChart.com 'simulated indexes'][7]. The blog post introducing them is
  https://portfoliocharts.com/stock-index-calculator/

[1871_returns.csv]: https://github.com/hoostus/prime-harvesting/blob/master/1871_returns.csv
[6]: https://www.bogleheads.org/wiki/Simba's_backtesting_spreadsheet
[2004-period-life-table.csv]: https://github.com/hoostus/prime-harvesting/blob/master/2004-period-life-table.csv
[7]: https://github.com/hoostus/prime-harvesting/blob/master/stock-index-calculator-20160620-v2.csv

I've also included local copies of some of the Excel sheets the CSV files were derived from.

- [Simba's backtesting spreadsheet][8]
- PortfolioChart.com 'simulated indexes' [raw Excel file][9]

[8]: https://github.com/hoostus/prime-harvesting/blob/master/Backtest-Portfolio-returns-rev15c.xlsx
[9]: https://github.com/hoostus/prime-harvesting/blob/master/stock-index-calculator-20160620-v2.xlsx

FUTURE IDEAS
============
https://www.kitces.com/blog/Renaming-The-Outcomes-Of-A-Monte-Carlo-Retirement-Projection/

- Probability of Failure should be called Probability of Adjustment
- Probability of Success should be called Probability of Excess
- Do a comparison of 3 states: probability of adjustment, probability of excess, and
the Goldilocks "just right". How to define "just right"? Similar to the Sleep
Well At Night Number...
- "Sleep Well At Night" is an absolute number? Based on estimated number of
years left alive?
- Probability of failure and SIZE of failure might be different. You might
choose the plan with the higher probability of failure because the size of
failure is smaller.
- Try to tie together Prime Harvesting and valuations better.
- Implement the autoregressive model for returns from Blanchett, Finke, Pfau in
"Low Bond Yields and Safe Portfolio Withdrawal Rates"
- My WER calculations always seem very far off.
- Implement Blanchett's formula from "Simple Formulas to Implement Complex Withdrawal Strategies"