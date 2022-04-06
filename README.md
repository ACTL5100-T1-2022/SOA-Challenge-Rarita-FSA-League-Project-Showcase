![](https://github.com/ACTL5100-T1-2022/github-showcase-page-group-exemption/blob/859fdceb6559c4af0c8ab88335304dbdb18a83c5/Banner.png)

# Table of Content
> 
* [Executive Summary](https://github.com/ACTL5100-T1-2022/github-showcase-page-group-exemption#executive-summary)
* [Team selection](https://github.com/ACTL5100-T1-2022/github-showcase-page-group-exemption#team-selection)
* [Economic Impacts](https://github.com/ACTL5100-T1-2022/github-showcase-page-group-exemption#Economic-Impact)
* [Implementation Plan](https://github.com/ACTL5100-T1-2022/github-showcase-page-group-exemption#Implementation-Plan)
* [Assumptions](https://github.com/ACTL5100-T1-2022/github-showcase-page-group-exemption#Assumptions)
* [Risk & Risk Mitigations](https://github.com/ACTL5100-T1-2022/github-showcase-page-group-exemption#Risk)
* [Data & Data Limitations](https://github.com/ACTL5100-T1-2022/github-showcase-page-group-exemption#Data-&-Data-Limitations)
* [References](https://github.com/ACTL5100-T1-2022/github-showcase-page-group-exemption#References)

# Executive Summary
![Football](https://user-images.githubusercontent.com/72643422/161918841-a6490287-15a6-4821-ab5e-ebada58b00dc.gif)

> This report focuses on the creation of a competitive national football team for Rarita. The decision to create a national team might, at first, seem to be a sound one. In the UK for instance, the value added to the economy by the Premier League grossed 7.6 billion pounds in 2019/20 (EY, 2022). However, the implementation will not be an easy one. Indeed, to generate a positive cash flow for the country, we must take into consideration the allocated budget to fund the team, while making sure that the brand created around the latter generates a positive income stream.

**Throughout this report, we will:**
* Undertake a team selection analysis by creating a player performance index. 
* Underline key risks and limitations that would prevent Rarita from reaching its goal and how to potentially mitigate them. 

**Objectives**
* Creation of a nationally competitive team for Rarita
* Creation of a brand around the team

# Team selection
* **Two Measurements**
    * Player Performance Index (PPI): Measure the ability of player. It is weighted average score based on ranking in different statistics. Click it to see more details.
![](https://github.com/ACTL5100-T1-2022/github-showcase-page-group-exemption/blob/main/PPI.png)
    * Salary Efficiency (SE): Measure whether a player is worth the salary he received.
![](https://github.com/ACTL5100-T1-2022/github-showcase-page-group-exemption/blob/main/SE.png)
* **3-Round Selection**
```mermaid
flowchart LR;
    A(Round 1: Top 50% of SE)-->B(Round 2: Rarita Players in Top 10% of PPI)--the team is not full-->C(Round 3: Add foreign players with top PPI)
    B--the team is full-->D(Round 3: Remove excess players with lowest PPI)
```
* **Team Selection Results**
![](https://github.com/ACTL5100-T1-2022/github-showcase-page-group-exemption/blob/main/team%20selection.png)

* **Competitive Testing**
    - Step 1: Pick players randomly from the competitive couuntries to build a team with same combination of Rarita Team.
    - Step 2: Simulate 5000 times to create a dstribution of the teams' average PPI.
    - Step 3: Test if the distribution is normal distribution using Shapiro Test.
    - Step 4: If normal, calculate the probability for Rarita Team to be competitive using the fitted disrtibution.

* **Testing Result**: [Result of Shapiro Test](https://github.com/ACTL5100-T1-2022/github-showcase-page-group-exemption/blob/main/test.png) indicates that [the distribution](https://github.com/ACTL5100-T1-2022/github-showcase-page-group-exemption/blob/main/distribution.png) is normal and the probability for Rarita Team to be competitive is close to 1.

* **R code**: click to the outcomes of [r code](https://github.com/ACTL5100-T1-2022/github-showcase-page-group-exemption/blob/main/Poisson-Loves-Exponential-RCode.pdf)

# Economic Impact
### Rarita's Economy 
According to given Rarita's economic data, several trends are observed:
* Declining GDP![1](https://user-images.githubusercontent.com/102961370/161916581-6e6d4b76-9f0a-41ba-99d5-e976eaf318de.png)
* Decreasing Inflation Rates![2](https://user-images.githubusercontent.com/102961370/161916610-5461e2f3-3804-4b34-9827-aee02a702c8b.png)
* Decreasing Spot Rates (across different maturities)![3](https://user-images.githubusercontent.com/102961370/161916692-547c4336-71b3-45ad-bede-b1b4a185ab6b.png)
<br>
From economic perspective, Rarita seems to be at contraction phase. 

### Analysis of Revenues, Expenses and Salaries
The expected revenue table demonstrates that the chosen football team will generate significant amount of revenues throughout the following 10 years in an increasing trend. ![4](https://user-images.githubusercontent.com/102961370/161916813-cfb60b24-c58c-4c79-98f3-ebe71aa8bf78.png)
<br>Then, expected expense & salary table also provides a brief estimations of the possible future outgoings. 
![5](https://user-images.githubusercontent.com/102961370/161916926-d3b1efc4-4bae-4f62-be3b-ff240ebbeaab.png)
<br>What is noteworthy is that the salary expenses are expected to decline in the future which means that in the long term, Rarita is expected to receive higher profit due to decreased salary expenses.
![6](https://user-images.githubusercontent.com/102961370/161917030-72f6a848-5589-4fcd-ada1-b6d33346e1d4.png)


### Indirect Economic Impacts
* Construction and urban Development
<br>New football team will raise the demand of stadiums and relevant infrastructures. Accordingly, this will benefit urban development of Rarita. 
* Tourism
<br>Research shows that during 2002 FIFA World Cup in South Korea, above 50% of total tourist arrivals can be classified as attracted by the World Cup and this generates great economic growth to South Korea’s economy. Similarly, for Rarita, tourism will also become an important source of indirect economic revenues and benefit Rarita's economy. 
* National Brand
<br>Prosperity of football will benefit Rarita’s nation branding and operate greater international perceptions of Rarita. With a much closer relation with football, Rarita is expected to have a more positive image by people. 

# Implementation Plan
### Team Renewal Plan
Benchmark above can be continuously used to update the team roster regularly under the assumption that the benchmark will remain the same for the next ten years. Before each tournament, team management should use the PPI and SE of the previous league as indicators to execute the three-round selection mentioned in the team selection part. It is pertinent to note that teams should use foreign players with discretion because of the loan restrictions. The decision to borrow foreign players to fill the vacant positions will be made after the first two rounds of the draft.
### Fund-Raising Strategy 
The most common way is to sell football match tickets. Furthermore, another way is to loan out redundant players to other countries. Though this method will generate revenues, one should be careful of lending high-ranking players during on-seasons. Moreover, in an attempt to raise funds, we could also design and sell unique merchandise like headbands, t-shirts, and even player trading cards.
 
### Marketing Strategy 
To increase the team’s recognition, we may build a brand about the team. Designating the most famous players to promote the brand’s apparel to promote the team should also be advocated. Moreover, social media platforms like Twitter, Instagram, and even Facebook are good ways to update fans about the latest news concerning the team. In addition, we can increase community involvement to enhance the team’s recognition, this can be done through volunteering or make-a-wish events. Further, while giving back is a reward in itself, community participation will not only help in fostering relationships between the players but could also unify the country around the national team.

# Assumptions
As the data given are limited, hence a few assumptions have been made for further analysis. With the current economic status in Rarita, we would assume that the economy would remain stable with no unexpected events such as the COVID-19 pandemic in 2020 which affected Rarita's future economic predictions. 

Assumptions regarding the prediction of the inflation rate, interest rate, revenue, and expenses are a linear relationship against time using a linear regression model for the simplicity of our modeling. The team selection process is also based on the assumption that the performance of the players is the same in the future with the time of estimation when selections were made.

# Risk
* **Health-related risks & risk mitigation techniques**

According to Arab News, footballers are likely to suffer from heart conditions, which can lead to them collapsing, and even dying. These health problems can directly affect the player’s performance during a competition. The death of a player caused by sudden heart attack during a competition will directly affect the team’s morale and the outcome of the game. To detect risks, routine health checks will be conducted. Health problems can be financially costly for both teams and individuals, in which the use of life and health insurance will help facilitate the transfer of financial risk. Furthermore, to prevent footballers’ injury, we could encourage them to wear full and proper equipment, and increase nutrition interventions (Gatorade Sports Science Institute, n.d.). 

* **The general environmental risk & risk mitigation techniques**

The Covid-19 breakout postponed the Tokyo Olympic Games originally held in 2020 to 2021 which resulted in a delay for players to obtain success in the competition. This implies that the payback period of the investment will be stretched out. Peace can create fortune while war will destroy fortune. With the recent war between Russia and Ukraine, it has affected the inflation rate to change and increase (The Economist, 2022). Faced with the risk of the general environment, teams can only implement a policy of risk retention. In addition, the cycle of economic as well as social development is predictable, hence, team management should adjust the risk exposure promptly, including investment and team promotion.

### Risk summary
Injuries to player health cause higher expected loss for the team than exposure to systemic risk. The game is very intense, so the incidence of health problems in professional players is much higher than the likelihood of adverse changes in the general environment. Health risk mitigation is easier to take control of and the past injured players’ statistical figures can determine the severity. However, general environmental risks are usually unexpected and can only be retained. Thus health risks that are convenient to control are the primary risks and the broader environmental risks are secondary risks. 

# Data & Data Limitations
* **Data Cleaning**
    * The raw data consist of negative values in variables such as Standard Free Kicks, Standard shots on target per 90 minutes, etc. Removing it would be reasonable as it would be impossible to have negative number of shots. Click [here](https://github.com/ACTL5100-T1-2022/github-showcase-page-group-exemption/blob/main/2022-student-research-case-study-player-data%20202234.xlsx) to have a look.
    * Percentages higher than the standard 100% has been removed as the playtime is too short to be considered.
 
<p align="center">
![Data Limitation](https://user-images.githubusercontent.com/72643422/161919592-21d8a002-7c69-4be4-bf1f-f1761c3e59ba.gif)
</p>
* **Data Limitation**
    * Removing data based on such analysis would result in misleading or inaccurate results as we may remove important information which provides high significance to our analysis.
    * In 2021, players are transferred between clubs resulting in multiple information for the same player, however, only the value with the highest salary and PPI calculated will be used. This may not fully reflect the potential and the performance of the player on the soccer team.
    * The Shapiro-Wilk test is used to test the normality of the benchmark regarding our comparison between the constructed soccer team against those ‘competitive teams’. Consequently, it is not sensitive to outliers when testing for normalities of the distribution and can only handle up to 5000 simulated results.
    * Prediction of inflation for future salaries of each player is done based on a linear regression which describes the relationship between time and inflation rates. Such a model does not account for variation on some variables such as employability of that position, players’ performance, the experience of players, etc. 
 
**Thank you for reading our report and we hope you have a pleasant day!** 
<br>
![giphy](https://user-images.githubusercontent.com/72643422/161918286-b48964f4-f912-40b1-a60c-16330e2c64b2.gif)

# References 
* Allmers, S., & Maennig, W. (2009). Economic impacts of the FIFA Soccer World Cups in France 1998, Germany 2006, and outlook for South Africa 2010. Eastern Economic Journal, 35(4), 500–519. https://doi.org/10.1057/eej.2009.30

* EY (Ed.). (2022). Premier League: Economic and social impact. Retrieved from https://resources.premierleague.com/premierleague/document/2022/01/17/b61d9bb0-1488-4cd1-be25-82be98073252/EYUK-000142222_PL-economic-and-social-contribution_28_Spread_HR_2.pdf?utm_source=premier-league-website&utm_campaign=website&utm_medium=link.

* Heart attacks, sudden deaths in football must force authorities to raise safety bar. (2022, January 3). Retrieved from Arab News website: https://www.arabnews.com/node/1997221/sport

* Lee, C.-K., & Taylor, T. (2005). Critical reflections on the economic impact assessment of a mega-event: the case of 2002 FIFA World Cup. Tourism Management, 26(4), 595–603. https://doi.org/10.1016/j.tourman.2004.03.002

* Medina, D., Lizarraga, A. & Drobnic, F. (2014). Injury Prevention and Nutrition in Football. Gatorade Sports Science Institute. Retrieved from https://www.gssiweb.org/sports-science-exchange/article/sse-132-injury-prevention-and-nutrition-in-football#articleTopic_7

* The inflationary consequences of Russia’s war will spread. (2022, March 19). Retrieved from The Economist website: https://www.economist.com/finance-and-economics/the-inflationary-consequences-of-russias-war-will-spread/21808192
