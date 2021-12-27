<h2 align="center">Dating App Popularity</h2>

Dating apps have always intrigued me. Without them, we're relying on some level of serendipity to connect with others romantically.

Pre-dating apps, my social circle met through friends or in college. Heck, when I was out for dinner recently, I overheard a conversation of daughters asking their mom how she met their dad. The mom replied, “We met through church friends and your god mother introduced us thinking your dad and I would hit it off. She hosted a dinner, invited the both of us, and we started dating after that.”

How cute!

As of Fall 2021, I read three consecutive "How We Met" stories on Zola and The Knot of former coworkers and acquaintances that described meeting their match on Bumble and Tinder. 

Is this a mere coincidence or will it be an ongoing trend?

What do you foresee Heimdall?

<p align="center">
<img src="images/Heimdall.jfif" width=500>
</p>

In speaking to Heimdall, he references a Feb 2020 article from  [Pew Research](https://www.pewresearch.org/internet/2020/02/06/the-virtues-and-downsides-of-online-dating/). Pew surveyed US Adults and found that 12% have been married or in a committed relationship with someone they met through online dating.

<p align="center">
<img src="images/Pew.jfif" width=400>
</p>

If we dive deeper by age segmentation, the same proportion (16-17%) of US Adults in both age groups 18-29 and 30-49 have been in a committed relationship or married to someone they met on a dating site or app. According to this survey, there is a 58% decrease among Americans over 50 who use online dating.

As to whether dating apps are becoming more popular over time, Pew writes that "The share of Americans who have used these platforms – as well as the share who have found a spouse or partner through them – has risen over time,” from 3% of Americans in 2013 to 12% in 2019. (Note: There were some changes in question wording between Pew’s 2013 and 2019 surveys, as well as differences in how these surveys were fielded.)
 
The growth in self-reported online dating may even underestimate its true impact, because there is likely a lag between online dating use today and the number of committed relationships and marriages via online dating in the years to come.

In addition to surveys, let's examine other data sources to understand each app's popularity and trends over time. 

Which leads me to the central question of this blog post: 


### Which dating app is the most popular?


My hypothesis is Tinder is the most popular dating app. 

Tinder invented the swipe gesture, a cultural phenomenon of 'swipe left' and 'swipe right' to accept or reject a match, which has since been adopted in other mobile products. Also, anecdotally, among my friends and family, Tinder is the most well-known. 

My ideal metric to measure popularity would be the number of matches (serious relationships) that each app generates. Since this cannot be measured directly, this analysis will rely on survey data, Google Trends, Statista and SEC data sources as proxies.

For this analysis, I will examine the following 5 apps:

1.	Tinder
2.	Bumble
3.	Hinge
4.	OkCupid
5.	Match 

We can first look at US search interest data from Google Trends using the Pytrends API. I hypothesize dating app search trends are correlated to user app downloads and actual app engagement time. After all, a user would perform a Google search when they have a question related to the app, technical or informational. The strength of the correlation between google trends, app download, and app revenue is currently unknown, so we might as well explore it in this analysis now that our relationship is this deep in ;). 


### 1. Time series analysis

Our data series begins when the last app Bumble launched in December 2014. It appears Tinder has always held a consistent lead in Google search popularity for the entire 2014-2021 period. Match.com and OkCupid have steadily declined since 2014 as Bumble and Hinge became more popular. The spike in Bumble search in 2021 is most likely due to the IPO on February 10th, 2021.

<p align="center">
<img src="images/Time Series Analysis.JPG" width=400>
</p>


### 2. Search interest by region

I'm surprised at the search interest regional patterns of each dating app. 

-	I'm curious about the sensitivity of the regional rankings the more I tinker with the date range. 
-	Bumble and Hinge are relatively more popular in Texas and NY respectively; this could be due to the fact that the companies are headquartered in these states. 
-	OkCupid is most popular in Oregon+Washington and in Massachusetts+Washington DC. 
-	Match.com is quite popular in the midwestern states.

<img src="images/Tinder Search by Region.JPG" width=250>

### 3. App Downloads and Revenue 

The number of app downloads and gross revenue are two additional metrics of dating app popularity.  It is reasonable to assume that app downloads are positively correlated with user engagement and the number of matches/relationships generated by each dating app. I obtained both Apple store and Google Play store data from Statista.com for Tinder and Bumble North and Latin America regions.

<p align="center">
<img src="images/Statista.JPG">
</p>

<p align="center">
<img src="images/App Downloads v. App Rev.JPG">
</p>
 
### 4. Graph Theory and Revenue Growth - Does linear trend still hold?

Even though we observe a linear trend between app downloads and revenue, it is possible that revenues will scale non-linearly if users on larger apps can find exponentially-more matches. Graph analysis shows that as the number of users (nodes) increases, the number of potential connections between users (edges) increases at an accelerating rate. 2 users have 1 potential connection; 3 users have 2; 4 users have 6; and 5 users have 10.

<p align="center">
<img src="images/Graph Theory.JPG" width=400>
</p>


### 5. Correlation between Google Trends, app downloads, and revenue

After diving deeper into Tinder and Bumble's search popularity, app downloads, and revenue, there appears to be moderate correlation between Tinder search popularity and app downloads, weak correlation between Bumble search popularity and app downloads, and a high correlation between app downloads and revenue. This tells us that app downloads is more reliable than Google Trends in measuring dating app popularity.

<p align="center">
<img src="images/Tinder Search Popularity v Monthly Downloads (2018-2020).JPG" width=425>
</p>

<p align="center">
<img src="images/Bumble Search Popularity v Monthly Downloads (2018-2020).JPG" width=425>
</p>

<p align="center">
<img src="images/Tinder Corr Map.JPG" width=425>
</p>



<p align="center">
<img src="images/Bumble Corr Map.JPG" width=425>
</p>


### 6. SEC 10-K Data

Match Group owns Tinder, Hinge, OkCupid, Match.com, and other dating sites (POF, Our Time, etc.). Match Group has categorized all other brands but Tinder in an "Other Brands" category. I cannot disaggregate results for Hinge, OkCupid, and Match.com.

The 10-K data shows that Tinder and Bumble have displayed a double digit YOY revenue growth trajectory for two consecutive years, and that Tinder is by far the highest-revenue dating app.

<p align="center">
<img src="images/Dating App Revenue using Plotly.png" width=825>
</p>

### 7. So what is the most popular dating app?

Based on Google Trends: 
1. Tinder
2. Match.com
3. Bumble
4. Hinge
5. OkCupid

The biggest takeaway from this is that while Match.com and OkCupid have once had a lead in the past, they are trending downwards. If this continues, it is likely that Bumble and Hinge will outpace them in popularity over time. It makes sense as I have not seen as much publicity with Match.com and OkCupid relative to Bumble and Hinge.

Tinder google searches have a 46% correlation with Tinder monthly downloads. Bumble google searches have a 15% correlation with Bumble monthly downloads. Because search popularity scores do fluctuate, that means dating app downloads is a more reliable indicator of dating app popularity.

### 8. Limitations
There were challenges faced when collecting and analyzing the data. 

1. The search popularity score on Google Trends is not static. Depending on when I run a given search, even with the same keyword and time range, the score can change for a given month. However, Google Trends is still a good proxy for public interest.
2. In validating the keywords, I'm confident I have chosen the best keywords related to the dating app. When querying directly from Google Trends, the related queries were in line. However, there's always a possibility of noise.
3. Except for Google Trends, we have incomplete information to consistently compare across 5 apps. Statista has more information on Bumble and Tinder and I can't disaggregate Match Group's 10-K for Hinge, OkCupid, and Match.com to understand each app's revenue. It would be interesting to compare monthly app downloads vs. monthly app revenue. Because only annual app revenue was available, monthly downloads was annualized and then the correlation was measured for 2018-2020. This means only 3 data points were used to compare Tinder and Bumble's app downloads vs. app revenue, which is why the strength of this correlation appears high.
4. Revisiting if there is a lag between online dating use today and the number of committed relationships and marriages via online dating, such outcomes are difficult to track because results take too much time. 

One idea (and only with prior user consent to opt in) is similar to how instagram uses phone number to make suggestions of who you know, it would be interesting if The Knot and Zola did such syncing with a unique identifier to track how our known contacts met, got married, and/or the duration of their courtship. This would help attribute positive outcomes to specific dating apps to better understand their overall impact to society. The other method is to rely on anecdotal evidence and surveys. I do believe there is a middle ground between user privacy and gaining more transparency of outcomes in the future.


<p align="center">
<img src="images/Dr.Strange Christine Wedding.JPG" width=500>
</p>

<h6 align="center"> I'm sure Marvel fans are curious where Christine met her new beau in the trailer for Multiverse of Madness premiering May 6, 2022. </h6>

### 9. Bonus: Brand Differentiation

What's interesting about Tinder is its steady popularity over multiple years on Google Trends. Is it because the platform caters to a variety of connections that the others do not? Or is it that their large user base is more enticing?  

To that point, each app is branded differently, which will attract different users to their platform. 

#### Dating App Taglines

•	Tinder: The #1 place to spark new connections.

•	Bumble: Women make the first move.

•	Hinge: Designed to be deleted.

•	Match.com: Start something real.

•	OkCupid: Dating deserves better.


Each app must build their features with their brand in mind.

Tinder is clearly trying to be the #1 place to spark connections. Their features are thoughtful regarding the many possible motives and methods that people want to connect with one another. Their investment in interactivity like Swipe Night, which is a choose your own adventure on Sundays between 6pm-12am can take users away from a prime time slot to use other apps. The Tinder Explore page allows a user to match based on interest. Hot Takes takes place every night from 6pm-12am, which is a form of blind speed dating, where a user can message before deciding to match. If a user doesn't match, then that person can also speed date someone else. The user can not see the other person until a match is made. Not responding in 30 seconds to the other side ends the game. It forces users to spend that time in conversation as opposed to not messaging after matching.

Bumble's Women Make the First Move branding is very solutions elegant. In fact, if you just look at the entire app, the devil is in the details. Bumble gives a lot of power to the user, from choosing whether to apply the Smart Photo algorithm, to choosing the first ice breaker question or giphy to say hi. The video feature feels like a real date! If one is in New York, one can also choose a date location to meet up that's synced to a yelp like page. What I think is great about their features is while women make the first move, Bumble has created multiple features to break the ice or propose a date that even if a user is at lost for words, that person can get the ball rolling with a match.

The perception of Hinge users is that they are looking for a commitment, which is why the Design to be Deleted branding attracts them. Hinge uses the Gale Shapley Algorithm which is the solution to the stable marriage problem. When this algorithm was used to match people on college campuses via a project called the [Marriage Pact](https://www.npr.org/2021/03/02/972943944/the-marriage-pact), some outcomes that occurred were they were matched with their siblings or they ultimately matched with people they became good friends with. Features are oriented toward writing thoughtful answers to prompts and being authentic. Hinge has recently heavily promoted a voice prompt where a user can record their voice so one can hear a person's voice prior to matching. Podcasters have joked that only use this feature if the user has a good voice. It's a sweetener but not necessarily the deciding factor of why someone would match with another.


### Summary
In summary, having more users on a dating app is better because it creates more potential connections. However, there are many reasons why people use dating apps which creates multiple niches companies can exploit. While number of users might attract users to an app, having a positive user experience is what keeps users coming back and factors into popularity. Positive experience can mean connecting with good matches, having fun, seeing progress/momentum, or not getting harassed. 

While Tinder is clearly the most popular having grown the largest user base, if an app continues to create positive user experiences, that app can also be a contender in this market. 

With this, I'm excited to see how these trends play out over time!

### Python Libraries Used
- Pandas
- Matplotlib
- Seaborn
- Plotly
- NetworkX
- Datetime

### Methods
- Data Visualization
