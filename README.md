# Privacy-Preserving AI Framework using Federated Learning

By: Sultan Algarbi
Advisor: Dr. Muhamad Felemban

## Introduction
Regression is a statistical method used in finance, investing, and other disciplines that attempts to determine the strength and character of the relationship between one dependent variable (usually denoted by Y) and a series of other variables (known as independent variables).

Regression helps investment and financial managers to value assets and understand the relationships between variables, such as commodity prices and the stocks of businesses dealing in those commodities.

Regression takes a group of random variables, thought to be predicting Y, and tries to find a mathematical relationship between them. This relationship is typically in the form of a straight line (linear regression) that best approximates all the individual data points.
![image](https://user-images.githubusercontent.com/45789407/197382712-ab5f5b89-6115-4aeb-a5ec-38d6e517ef8d.png)

The general form of each type of regression is:
Simple linear regression:
Y = a + bX + u
Multiple linear regression:
Y = a + b1X1 + b2X2 + b3X3 + ... + btXt + u

Machine learning, which is a subfield of AI, is widely adopted in many fields, for example, speech recognition, image recognition, traffic prediction, and email spam and malware filtering. Also, we can adopt the ML with linear regression applications to produce the best line of regression.


## Our Problem:
Traditionally, a machine learning model is trained on a central set of data, which may be collected by one or more data providers. This method works well when the data is owned by a single data provider or when data owned by several different data providers can be shared and merged together without violating laws and regulations.
In some cases, there are some practical challenges to sharing and circulate data across different organizations. On the one hand, there are risks of data abuse and/or secondary distribution of data once the data is shared with third parties. On the other hand, it is prohibited to trade some types of data according to certain laws and regulations. How to train machine learning models under these constraints raises a major challenge for both the academic and industry communities.


## Our Solution:
Federated Learning is a new distributed learning mechanism which allows model training on a large corpus of decentralized data owned by different data providers, without sharing or leakage of raw data.

In this project, we are working on Federated Learning framework, where each client trains a sub-model at its site using only local data, and then shares its sub-model with the central server to make its contribution in the global model. The global model will be used many times to improve the sub-models.
![image](https://user-images.githubusercontent.com/45789407/197382729-cbd76250-8dd6-4ad1-905a-6517f7b4979e.png)

## Our Objective and Contribution
Through this project, we seek to provide a framework that combines sub-models to form a global model without the need to share data for each party.

In addition, we present a project to combine the federated learning and linear regression, as there are no researches that combine them according to what we found after a long search process.

Finally, we implanted this project as a framework that can be used with any regression dataset (with some constraints).

## OUR METHODOLOGY
Approach taken to accomplish this project:
- Ongoing meetings with the supervisor of the research project.
- Constantly reading research papers related to the research project.
- Attend a short course on research skills.
- Searching for libraries to implement Al and ML models.
- Collecting and testing data from different resources.
- Reviewing (STAT319, ML, AI) courses to understand the ML algorithms.


## Testing the framework
Dataset:
To setup this framework, we have to select any dataset with the following constraints:
- The dataset file extension should be “.csv”.
- The first row in the file represents the labels of the features.
- The remaining rows represent the samples.
- The type of each element in the dataset should be number (integer, float, double) with no empty element.
- From the first column to the column before the last, the data represent the independent variables [Xs], and the last column represent the dependent variable [y].

Federated Clients (parties): this framework can be used by any number of clients (parties), and to setup this experiment, the user should enter the number of clients (parties), where in this experiment, the user enter the dataset as one block, then the framework will distribute the dataset to the clients. In real world implementation of Federated learning, each client has its own dataset in isolation. The shard creation step in the framework only happens in the experiments.

Training and Testing samples: the user has the ability to enter the percentage of the testing samples, then the framework will split the dataset to two sub-datasets, one for the training, and the other for the testing. The training samples will be sharded to sub-datasets, where each sub-dataset will be associated to one client. The testing samples will be used to test the federated model and the centralized model.

Training client datasets: each client trains a sub-model at its site using only local data, and then shares its sub-model with the central server to make its contribution in the global model. The global model will be used many times to improve the sub-models. The sub-model of each client contains the values of the estimated slope coefficients and the y-intercept.

* Each client shares its regression equation and receives the global regression equation.


## The result
To test the accuracy of the federated learning framework, we should compare its percentage of error with the traditional central server with the same dataset for training and testing.

dataset name: wire_pull_strength
number of clients: = 4
testing size = 20%
![image](https://user-images.githubusercontent.com/45789407/197382751-0ef915d3-c1e8-4114-a375-e34a6121babd.png)


## REFERENCES
- Yong Cheng, Yang Liu, Tianjian Chen, and Qiang Yang. 2020. Federated learning for privacy-preserving AI. Commun. ACM 63, 12 (December 2020), 33–36. DOI:https://doi.org/10.1145/3387107
- P. Chhikara, P. Singh, R. Tekchandani, N. Kumar and M. Guizani, "Federated Learning Meets Human Emotions: A Decentralized Framework for Human–Computer Interaction for IoT Applications," in IEEE Internet of Things Journal, vol. 8, no. 8, pp. 6949-6962, 15 April15, 2021, doi: 10.1109/JIOT.2020.3037207.
- F. Sattler, K. -R. Müller and W. Samek, "Clustered Federated Learning: Model-Agnostic Distributed Multitask Optimization Under Privacy Constraints," in IEEE Transactions on Neural Networks and Learning Systems, doi: 10.1109/TNNLS.2020.3015958. URL: https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9174890&isnumber=6104215
- L. Ahmed, K. Ahmad, N. Said, B. Qolomany, J. Qadir and A. Al-Fuqaha, "Active Learning Based Federated Learning for Waste and Natural Disaster Image Classification," in IEEE Access, vol. 8, pp. 208518-208531, 2020, doi: 10.1109/ACCESS.2020.3038676. URL: https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9261337&isnumber=8948470
- G. Hua, L. Zhu, J. Wu, C. Shen, L. Zhou and Q. Lin, "Blockchain-Based Federated Learning for Intelligent Control in Heavy Haul Railway," in IEEE Access, vol. 8, pp. 176830-176839, 2020, doi: 10.1109/ACCESS.2020.3021253 URL: https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9184854&isnumber=8948470
- L. U. Khan, M. Alsenwi, I. Yaqoob, M. Imran, Z. Han and C. S. Hong, "Resource Optimized Federated Learning-Enabled Cognitive Internet of Things for Smart Industries," in IEEE Access, vol. 8, pp. 168854-168864, 2020, doi: 10.1109/ACCESS.2020.3023940. URL: https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9195820&isnumber=8948470
- Keith Bonawitz, Hubert Eichner, Wolfgang Grieskamp, Dzmitry Huba, Alex Ingerman, Vladimir Ivanov, Chloe Kiddon, Jakub Konečný, Stefano Mazzocchi, H. Brendan McMahan, Timon Van Overveldt, David Petrou, Daniel Ramage, Jason Roselander
- Jakub Konečný, H. Brendan McMahan, Felix X. Yu, Peter Richtárik, Ananda Theertha Suresh, Dave Bacon
- Rieke, N., Hancox, J., Li, W. et al. The future of digital health with federated learning. npj Digit. Med. 3, 119 (2020). https://doi.org/10.1038/s41746-020-00323-1
