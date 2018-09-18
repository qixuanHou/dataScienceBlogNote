## Characterizing Smoking and Drinking Abstinence from Social Media
### ABSTRACT
* GAP - the lack of longitudinal self-reported data on long-term abstinence has challenged addiction research. 
* What is done - 
  * We leverage the activity spanning almost eight years on two prominent communities on Reddit: StopSmoking and StopDrinking.  
  * We use the self-reported “badge” information of nearly a thousand users as gold standard information on their abstinence status to characterize long-term abstinence. 
  * We build supervised learning based statistical models that use the linguistic features of the content shared by the users as well as the network structure of their social interactions. 
* Results - 
  * Our findings indicate that long-term abstinence from smoking or drinking (∼one year) can be distinguished from short-term abstinence (∼40 days) with 85% accuracy. 
  * We further show that language and interaction on social media offer powerful cues towards characterizing these addiction- related health outcomes. 
* Goal and Further study -
  * We discuss the implications of our find- ings in social media and health research, and in the role of social media as a platform for positive behavior change and therapy.

### INTRODUCTION
main contribution
* We collect and study a novel dataset from Reddit that describes 1,153 users’ self-reported information on their duration of smoking or drinking abstinence via the badges. We use the badge information to identify short-term and long-term abstainers.
* We formulate and identify the key linguistic and interaction characteristics of short-term and long-term abstainers based on activity spanning eight years, from 2006 to 2014.
* We build a supervised learning framework based on the characteristics above to distinguish long-term abstinence from short- term abstinence with over 85% accuracy, 88% precision, and 82% recall.
* Our findings present a number of significant discoveries that may help researchers better understand the role of social media language and interactions in assessing and determining tobacco or alcohol use. We find that:
  * the nature of affect manifested in Reddit posts and comments as well as the tenure of participation in Reddit communities are indicative of short-term or long-term abstinence;
  * the network properties of the users (e.g., indegree) based on their interaction patterns also bear significant explanatory power towards characterizing these addiction-related health outcomes.

### BACKGROUND AND PRIOR WORK
#### Behavioral Science and Addiction
#### Social Media, Health, and Addiction

### DATA
#### Data Collection
#### Ground Truth Creation
* To identify the suitable durations to qualify for short-term or long-term abstinence, 
  The CDFs show stable patterns before the 30 percentile and after the 70 percentile. The 30 percentile mark for SS is 43 days while it is 44 days for SD; the 70 percentile mark is 350 days and 333 days for SS and SD, respectively. 

### STATISTICAL METHOD
* **Response variable.**  Our binary response variable represents if a user is a short-term or a long-term abstainer of smoking/drinking.
* **Explanatory variables (Language).** the top-100 most frequent unigrams, bigrams, and trigrams. sentiment of the posts
* **Explanatory variables (Addiction).** we utilized a snowball approach in which we seeded the dictionary searches with “smok*” and “alco- hol*”. We followed the “related words” returned by the dictionary results on these two seed words. We recursively adopted this ap- proach over three more iterations. 
* **Explanatory variables (Interaction).** Our third set of explanatory variables focuses on the various aspects of interaction.
 * (1) Activity measures. 
 * (2) Participation in related subreddits.
 * (3) Graph measures. 
* **Statistical models.** We employ Ridge regression [18] to classify our binary response variable (short-term or long-term smoking/drink- ing abstinence). 

### RESULTS
### Deviance Results
list different phrases, and describe which phrases are more likely to be seen in which group of people
#### Classification Results

### DISCUSSION
#### Clinical Relevance
Our findings indicate that linguistic and interaction cues gleaned from activity in SS and SD forums may be used to understand short- term or long-term abstinence tendencies among users.
#### Implications for Social Media Research
Design Considerations. We believe our findings have strong design- related implications for social media research. Below, we describe several design ideas inspired by our research, which may help tai- lor social media platforms to cater to individuals aiming to abstain from smoking or drinking. 
#### Limitations and Future Directions

### CONCLUSION
We presented a computational framework to understand smok- ing and drinking abstinence of individuals from social media. We compiled and studied a previously unexplored source of data— activity on the Reddit communities StopSmoking and StopDrink- ing. We leveraged the badge feature in these forums to construct self-reported ground truth information on the abstinence status of users to characterize long-term abstinence. Our statistical mod- els incorporated a variety of language and interaction attributes to distinguish long-term abstinence from smoking or drinking from short-term abstinence with 85% accuracy. We found that linguis-tic cues like affect, activity cues like tenure, and network features like indegree to be indicative of short-term or long-term abstinence. Through our findings, we provided insights into how social media may be leveraged to tackle addiction-related health challenges.




https://www.cc.gatech.edu/~dchau/papers/15-ht-relapse.pdf

