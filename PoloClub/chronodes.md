## Chronodes: Interactive Multifocus Exploration of Event Sequences
### ABSTRACT
We present Chronodes, an interactive system that unifies data mining and human-centric visualization techniques to support explorative analysis of longitudinal mHealth data. Chron- odes extracts and visualizes frequent event sequences that reveal chronological patterns across multiple par- ticipant timelines of mHealth data. It then combines novel interaction and visualization techniques to enable multifocus event sequence analysis, which allows health researchers to interactively define, explore, and compare groups of participant behaviors using event sequence combinations.

### INTRODUCTION
#### Our Contributions
* mHealth data introduces unique challenges that existing tools for analyzing EHRs do not adequately address. Chronodes is one of the first attempts to explore how to best represent and explore mHealth data, combining data mining and human-centric visualization tech- niques to aid data exploration, pattern discovery, and fine-grain analysis of longitudinal mHealth records.
* Chronodes introduces two novel capabilities that help health researchers interactively explore and combine sequences to ask important, complex questions such as “what happens between first lapses that precede high activity, and second lapses that follow low activity but high stress?” 
* We conducted an informal study with 20 expert researchers from a spectrum of mHealth
related disciplines. By summarizing the insights gained, we outline important open re- search and design challenges in developing the mHealth field, and offer recommendations and design guidelines for future research.

### RELATED WORK
#### Visualization of Multiple Timelines
#### Event Alignment
#### Cohort Analysis
An alternate approach to understanding the trends of aggregated mHealth data streams is to con- sider groups of patients as cohorts, or individuals that share certain properties [4, 23]. 
#### Sequence Mining and Pattern Matching
Building machine learning and pattern matching algorithms into interactive visualizations presents promising opportunities for enhancing human pattern-finding abilities. Hochheiser and Shneiderman [18] and Buono et al. [7] demonstrated how users could select specific patterns in quantitative data streams and see where else they were found. 

### DATASET, RESEARCH QUESTIONS, AND DESIGN MOTIVATIONS
* Q1 What are the events preceding and proceeding each instance of smoking lapse [5]?
* Q2 What habitual events or cues (e.g., smoking every day after lunch) are correlated to smok-
ing lapse [25]?
* Q3 What are the correlations between smoking lapse and other physiological factors, such as
stress [2, 10]?
* Q4 What event patterns are specific to individual participants, and otherwise universal to all
participants [26]?

Using these target questions as our point of departure, we identified existing techniques in visual analytics and mHealth data analysis (as elaborated in Section 2) that would assist in answering these questions with respect to the AutoSense data. 
* event alignment
* frequent sequence mining
* recurring event sequences operates 

### CHRONODES OVERVIEW
#### Description of the User Interface 
* The Event Orchestra, fixed to the bottom of the screen (Figure 2B), lists a subset of participants represented by our dataset and displays the series of events that these participants perform over the course of 24-hour days.
* The Sequence Stage is the primary area of user interaction and accounts for the largest amount of space in the Chronodes interface (Figure 2A). It is within the Sequence Stage that the user selects, manipulates, and compares frequent event sequences. To demonstrate how the user performs these operations, we will describe Chronodes’s functionality through a use case scenario.
#### Use Case Walk-Through


https://www.cc.gatech.edu/~dchau/papers/17-tiis-chronodes.pdf
