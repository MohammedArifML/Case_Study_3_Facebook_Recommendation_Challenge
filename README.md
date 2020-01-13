# Social network Graph Link Prediction - Facebook Challenge

## 1. Problem statement:
Given a directed social graph, have to predict missing links to recommend users (Link Prediction in graph)

## 2. Data Overview
Taken data from facebook's recruting challenge on kaggle https://www.kaggle.com/c/FacebookRecruiting
data contains two columns source and destination eac edge in graph

- Data columns (total 2 columns):  
- source_node         int64  
- destination_node    int64  
## 3. Mapping the problem into supervised learning problem:
Generated training samples of good and bad links from given directed graph and for each link got some features like no of followers, is he followed back, page rank, katz score, adar index, some svd fetures of adj matrix, some weight features etc. and trained ml model based on these features to predict link.
### 3.1 Some reference papers and videos :
https://www.cs.cornell.edu/home/kleinber/link-pred.pdf
https://www3.nd.edu/~dial/publications/lichtenwalter2010new.pdf
https://kaggle2.blob.core.windows.net/forum-message-attachments/2594/supervised_link_prediction.pdf
https://www.youtube.com/watch?v=2M77Hgy17cg
### 3.2 Business objectives and constraints:
No low-latency requirement.
Probability of prediction is useful to recommend ighest probability links
### 3.3 Performance metric for supervised learning:
Both precision and recall is important so F1 score is good choice
Confusion matrix
