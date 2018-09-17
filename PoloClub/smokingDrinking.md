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
Social media research has indicated that individuals’ psychologi- cal states and social support status relating to health and well-being may be gleaned via analysis of language and conversational pat- terns. These include utilizing social media, largely Twitter, to un- derstand conditions and symptoms related to diseases [33], cyber- bullying and teenage distress [10], postpartum depression [8], men- tal health [9, 32, 19, 7], obesity and public health [1], exercise and mental health [11]. Broadly, this body of work investigated the role of linguistic attributes in describing or predicting health challenges.
We extend this body of research by examining the role of both language and social interactions gleaned from social media. Specif- ically, we build statistical language models that go beyond dictio- nary approaches. Additionally, we explore how network measures (e.g., indegree, neighborhood density, centrality, etc.) derived out of social interactions may bear explanatory power in the context of tobacco or alcohol addiction. Furthermore, we focus on Reddit, which remains underexplored in comparison to other social media platforms like Twitter.
There has been some research examining addiction behavior man- ifested on social media, however this body of work is limited. Re- lationship between displayed alcohol use on Facebook and self- reported information on alcohol abuse was examined in [26, 3, 27]. The authors in [4] explored sentiment manifested by individuals in Twitter by following a pro-marijuana profile. The structure of so-cial circles of prescription drug abusers was investigated in [16]. Using Twitter, the authors in [29] examined perceptions of tobacco products. Another work conducted a study examining characteris- tics of individuals who express a desire to quit smoking on Twitter [28]. More recently, researchers have studied the prescription drug abuse recovery community Forum77 [23]. In a method similar to [28], they identified dictionary-based linguistic attributes of indi- viduals in various phases of recovery, and were able to characterize recovery trajectory of these individuals.
With the exception of [27] and [23], none of the above pieces of research focuses on predicting health challenges related to addic- tion. Furthermore, it is important to note that, the ground truth la- bels on recovery in [28] and [23] were obtained via crowdsourcing. Simply looking at social media posts may not always allow third- party judges to reliably capture abstinence status. Additionally, reasons such as idiosyncratic or personal usage patterns of social media as well as differential social norms and stigma may motivate or preclude some individuals from explicitly reporting abstinence information in social media content. Hence, self-reported absti- nence information is extremely valuable. In this paper, we leverage self-reported abstinence information on smoking and drinking.





https://www.cc.gatech.edu/~dchau/papers/15-ht-relapse.pdf
