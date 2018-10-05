---
id: 22_Project_ideas
title: Project_ideas
sidebar_label: Project ideas
---

## 1. Code auto refactoring
```
 1. Let it collect all pass trhu data while tests are executing 
 2. Then figure out possible `code refactoring` and test and run tests after refactor , compare result 
    if same then save those refactoring.
    
 3. Apply when somebody is modifying code to that file as a pre commit hook like what `pretty print` does
```

## 2. Stock Sell Timing advice
```
1. Ask people to input their Stock holdings, they can choose to mask true holding with percentage like 10%, 25% 50% etc..

2. INPUT : a) Date bought, b) number of stocks(mask %) -- same mask % for each stock holding, 
            so it reflects their REAL protifolio. They can choose to INPUT only 3 stocks or 8 stocks etc.. that is fine. 
            
           c) what is the planning sellig Time window, d) profit gain % looking for
           e) Max drawdown they can stomach f) do they want to Re-vest sales if there is good oppertunity

3. System :
   DATA
   - mined data: a) Yahoo one year target price  b)Zacks Momentum/Value/Growth scores 
                 c) Finviz analyst target price mean & Up grade/Down grade data
   - derived data : calcualte technical Analysis TA indicator values  MA20 , MA50, MA200 , RSI, STOCastic, ATR
   
   ALGORITHM : see if we can have a either a Supervised Learning ML system to begin with. 
               In Phase 2 think RL Reinforment Learing system

4. Testing Hypothosis :
    - users : Srini Wag, Subba Rami R, Our Pad
```


