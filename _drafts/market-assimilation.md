---
layout: post
title: Market Assimilation
subtitle: A Smarter way to calculate The Market Absorption Rate
# cover-img: /assets/img/path.jpg
thumbnail-img: /assets/img/borg-thumb.jpg
# share-img: /assets/img/path.jpg
readtime: true
tags: [theory, statistics]

---

## Hypothesis
Can we develop a better algorithm for determining the Market Absorption Rate and Months Supply of Inventory that considers the constantly changing inventory and days on market?  Could this lead this into insight into how expired and withdrawn listings affect the change in inventory?


## Overview
If you have been in real estate, or interested in real estate, you have probably heard about Market Absorption Rates.  Or you know about the more common term, Months Supply of Inventory, which is related to the Market Absorption Rate.  We will get into these both, and talk about how they don't give the whole story.

## What is the Market Absorption Rate?
Basically, the Market Absorption Rate, or what I am calling MAR for brevity, is the rate at which homes sell compared to the number of homes for sale within a specified timeframe.  This gives an easy way to see how fast or slow the market is moving.  [The rule of thumb is that a rate below 15% indicates a buyer's market, and a rate above 20% signals a seller's market, where the middle represents a balanced market.](https://www.investopedia.com/terms/a/absorption-rate.asp)

### Calculating MAR
Now, for a real-world example, if there are 2,646 homes active on the market, and 934 of them sold last month, we would calculate the MAR to be 35.3%.  

\\[ 0.353 = \frac{934}{2646} \\]

Generalizing we get:

\\[ MAR = \frac{SOLDS}{ACTIVE} \\]

What this means is that 35.3% of the market was "absorbed" by selling properties.

### Calculating MAR by average sold
Some calculations of MAR take the average homes sold per month over the last 12 months.  If we had 9,495 homes sell over the past 12 months, with an average of 791.25 homes sold every month.  You would then calculate MAR using 791.25 as the homes sold in the month, not 934, the actual number of homes sold.  If we have 2,646 homes for sale, we can calculate the MAR as follows:

\\[ 791.25 = \frac{9495}{12} \\]
\\[ 0.30 = \frac{791.25}{2646} \\]


This means that the average number of homes sold in the winter is the same as in the summer.  This might not be accurate in your area, and I would argue this method is worse (and I do!).

Both methods show we are in a seller's market.  The results are pretty close, a little over a 5% difference.  But then again, 5% is the difference between a seller's market and a buyer's market.  Which method do you use?  Which method is used?

## What is Months Supply of Inventory?
Before we get into how these methods don't show the entire picture, let's talk about Months Supply of Inventory or MSI.  MSI tells you how many months it will take to sell all the homes currently for sale, not taking into account any new inventory.

### Calculating MSI
Using our MAR calculation, we can deduce that if 35.3% of the 2,646 homes are sold in one month, it will take 2.8 months to sell 100% of the 2,646 homes.  We calculate the MSI thusly:

\\[ 0.353x = 1 \\]
\\[ x=\frac{1}{0.353} \\]
\\[ x=2.8 \\]

Generalizing the equation, we get:

\\[ MSI = \frac{1}{MAR} \\]
\\[ MSI = \frac{1}{\frac{SOLDS}{ACTIVE}} \\]
\\[ MSI = \frac{ACTIVE}{SOLDS} \\]

You can see that MAR and MSI are two sides of the same coin.  They are, in fact, inverses of each other.

Using the numbers from the monthly average calculation, if 30% of the homes are sold in one month, it will take \\(\frac{2646}{791.25} = 3.34\\), about 3 months and 10 days to sell all the active inventory.


## Buyer's or Seller's Market
[A buyer's market is where supply exceeds demand](https://www.investopedia.com/terms/b/buyersmarket.asp). This gives the buyer an advantage over the seller in pricing and terms.  Likewise, a seller's market is where demand exceeds supply.  This gives the seller the advantage.

When looking at MAR, anything at or below 15% is a buyer's, and anything at or above 20% is a seller's market.  This makes sense, if 15% or less of the inventory is selling, the market has slowed down.  This reduces demand, and therefore increasing supply.  On the other hand, if the market is at or above 20%, this is a faster selling market.  This means that demand is high, and reducing supply.

It is often stated that a MSI of 6 months is a balanced market, at or below 5 months is a seller's market, and at or above 7 months is a buyer's market.  We would classify a balanced market to be where the supply curve meets the demand curve; [market equilibrium](https://www.mindtools.com/pages/article/newSTR_69.htm).

We can see that if we calculate the MSI, using a MAR of 15% and 20%.

\\[ \frac{1}{0.15} = 6.67 months \\]
\\[ \frac{1}{0.20} = 5 months \\]

We can compare what a buyer's and seller's market look like vis-a-vis real estate.  These characteristics are compared to a balanced market.

Some characteristics of a buyer's market include:
* Homes sell for less.
* Homes sit on the market longer.
* Seller's engage in a pricing war, to attract buyers.

Some characteristics of a seller's market include:
* Homes sell for a higher price.
* Homes sell faster with fewer days on market.
* Buyers engage in a bidding war to compete.


## Why these calculations are incomplete
These rates are a point-in-time calculation.  It doesn't take into account new listings, the active listing pending in the time frame, or how expireds and withdrawns affect the market.  We should also be looking at days on market to kind of qualify what inventory has a higher percentage of selling.  We need to be looking at the changes in the market to get an idea of which way the market is moving.

### Let's do some thought experiments
I want to go over some extreme and no-so extreme thought experiments.  These situations may never happen at the rate I will describe, but it could happen albeit, at a lower rate.

#### 1. We don't take into account the solds as part of active inventory
Every calculation I have found says, find all current active inventory, and solds for the timeframe.  Immediatly, are active homes is low.  Let's say that there are 1000 active homes at the end of the month.  We also find that 200 homes sold that month.  We can calcuate the MAR as \\(\frac{200}{1000} = 0.20\\).  Except when we sold those 200 homes, the total active inventory at the beginning of the month was 1200, not 1000.  This of course assumes no new listings, and the only change in supply was the act of selling a home.  With this new calculation, we see the MAR is now \\(\frac{200}{1200}=0.167\\).  This slight adjustment shows that we are more into a buyer's market than seller's market.

#### 2. We had a lot of expireds or withdrawls from in our timeframe
Since we don't look at expireds or withdrawls, we don't have a clear picture of the current inventory, and the change in inventory.  We could have a lot of expireds or withdrawls near the end of the month, which lowers the inventory.  Before those homes expired or withdrew, they were in the pool of active inventory.  The fact that they were removed from the supply, doesn't change the fact that they *were* there.

Let's assume that at the beginning of the month we had 1000 active homes for sale.  
Near the end of the month, we had 500 homes expire or withdraw.  We had 200 homes sell that month, and our active inventory at the end of the month is 300.  When we calculate the rate we see the MAR is \\(\frac{200}{300}=0.67\\).  Taking into account the solds as part of our inventory, we get \\(\frac{200}{500}=0.40\\).  Yes this example is extreme, but only to highlight the point.

#### 3. A large change in inventory near the end of our timeframe
We only look at the active listings at the end of the month, and not track the changes in supply.  We could get a influx of new listings near the end of the month.  This increases supply, but is not accurately, as these homes were never in the pool for the month.  The homes that sold were from a smaller inventory.

Let's say that at the beginning of the month, we had 200 active listings.  Let's also assume that there are no new listings in the middle of the month (to keep the math easy).  We see that only 20 homes sold that month.  Near the last day of the month, there were 800 new listings, leaving us with a supply of \\(200-20+800=980\\) homes.  If we calculate with the standard formula, we would see at rate of 2%, \\(\frac{20}{980}=0.02\\), when in fact is is nearer to 10%, \\(\frac{20}{200}=0.10\\).

#### 4. What is considered 'Active'?
In our MLS, we have an active status even if the home is under contract, active-pending.  Do we count these 'Active' homes even though they are under contract?  Or do we only count the active inventory that is currently for sale.  While they are in play, and some get backup offers, buyers typically ignore these homes.  If you had a lot of homes go active-pending near the beginning of the month, and nothing new, with escrows taking at least 30 days, your active count at the end of the month is artificially high.  This could trend to a buyer's market, when in fact it could be shifting into a seller's market.

There could be a market shift near the end of the time frame, and we wouldn't know about it until the end of the next time frame.  Good agents can sus this information out, just by how buyers and sellers act.  It would be nice to know this direction and how fast it is changing, on a day-by-day or weekly basis.

#### 5. New inventory went pending during the timeframe.
What if it's a hot market, and the new listings in our timeframe went pending, so we no longer count them as active inventory.  Let's assume we have 100 active homes at the beginning of the month, 100 new listing that month, 100 solds, and 50 went pending.  At the end of our timeframe we have \\(100+100-100-50=50\\) active homes, and 100 solds.  This was give us a MAR of \\(\frac{100}{50}=200\%\\).  We can see that we are in a hyper-seller's market.  We can infer that a lot of sales happened during our time period.  Was this at the beginning of the time period?  Or at the end?  It would be useful to see the trendline to figure out the way the market is heading.

The absorption rate is a point-in-time calculation. It doesn't take into account new listings, expired, or withdrawals.  It also doesn't take into account how long homes stay on the market.

https://realtytimes.com/advicefromtheexpert/item/38353-how-to-determine-if-it-s-a-buyers-sellers-or-a-balanced-real-estate-market