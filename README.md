# Personalized-Cancer-Diagnosis-Analysis
Our objective was the classification of Cancer Classes based upon the Gene, Variation &amp; Text and the problem statement was to classify the given genetic variations/mutations based on evidence from text-based clinical literature. Various ML model were applied and the results were compared. 

Business constraints: 1.errors can be costly 2.interpretability is very important 3.No low latency is required

Data Overview: 1.training_variants (ID , Gene, Variations, Class) 2.training_text (ID, Text)

Performance matrix: 1.multi class log-loss 2.confusion matrix

+--------------------------------------+----------------------+--------------------+--------------------+---------------------+
|           Models\Paramters           |      Train Loss      |      CV Loss       |     Test Loss      |   Miss-Classified   |
+--------------------------------------+----------------------+--------------------+--------------------+---------------------+
|            Random Model:             |  2.499615818487224   | 2.447143428512841  | 2.5069454835577716 |  0.8872180451127819 |
|                                      |                      |                    |                    |                     |
|    Univa Analy 'Gene'(LR+Calib.)     |  1.0344791998080038  | 1.2263625169777237 | 1.2561123021905696 |  0.9593984962406015 |
|  UniV Analy 'Variation'(LR+Calib.)   |  1.0467179237334998  | 1.7084074341627875 | 1.7187870123341769 |  0.9142857142857143 |
|  UniV Analy 'Text'(tfidf+1HotEncod)  |  0.7001371701802732  | 1.1870662728628807 | 1.1973329448493666 |  0.968421052631579  |
|                                      |                      |                    |                    |                     |
|             Naive Bayes              |  0.9151887243795561  | 1.2679414209037072 | 1.2949910047717403 |  0.3815789473684211 |
|         K-Nearest Neighbour          |  0.6838789439284688  | 1.0925676027867914 | 1.1145938485283275 | 0.37593984962406013 |
|                                      |                      |                    |                    |                     |
|     Log Regre (BoW-Bal. Class)       |  0.3533032245749473  | 0.9820765457740601 | 0.9626411888138315 |  0.325187969924812  |
|    Log Reg.(BoW-w/o Bal. Class)      |  0.3522104206219732  | 0.9824376470582592 | 0.9633440215559156 |  0.325187969924812  |
|                                      |                      |                    |                    |                     |
|    Log Regre (tfidf-Bal. Class)      | 0.35301532769444927  | 0.9790087470396699 | 0.961787335809495  | 0.32142857142857145 |
|   Log Reg.(tfidf-w/o Bal. Class)     | 0.35211357449668595  | 0.9792653584067594 | 0.962320744265082  | 0.31954887218045114 |
|                                      |                      |                    |                    |                     |
|  Log Reg. (1HotEncode-Bal. Class)    |  0.5727049626523608  | 1.1133424526167854 | 1.1128039556993254 |  0.3458646616541353 |
| Log Reg.(1HotEncode-w/o Bal. Class)  |  0.5688670769710756  | 1.1480795839108977 | 1.124399904343643  |  0.3458646616541353 |
|                                      |                      |                    |                    |                     |
|             Linear SVM               |  0.712267445965955   | 1.1560991922644934 | 1.1380111827356068 | 0.37030075187969924 |
|     Random Forest(1HotEncoding)      |  0.6873954778801096  | 1.1227799355482608 | 1.1290006586917964 | 0.36466165413533835 |
|    Random Forest(Response Code)      | 0.055339268402244554 | 1.3589848507706241 |  1.34328846636839  |  0.4567669172932331 |
|                                      |                      |                    |                    |                     |
|      Stacked Model(LR+SVM+NB)        |  0.6498302469206114  | 1.1311077921131338 | 1.1595792179100746 |  0.3879699248120301 |
|           Maximum Voting             |  0.9076965054343864  | 1.2071473560724522 | 1.2104439027495066 | 0.37293233082706767 |
+--------------------------------------+----------------------+--------------------+--------------------+---------------------+

Results of different applied models can be noticed in each corresponding file.

NB: This project was done as a part of assignment for machine Learning course taken at appliedaicourse.com/
