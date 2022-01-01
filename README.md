# Cryptocurrencies
## Overview of the analysis: 


After our work with Martha and our research into unsupervised machine learning we are now ready to tackle a new project. We are now confident in our skills in processing data. In our research we have learned how to cluster, how to reduce dimensions, and how to reduce the principal components using PCA. We are now working to develop an analysis for clients who are looking to invest in the cryptocurrency market. We are developing our analysis for Accountability Accounting, a prominent investment bank. They are one of Martha’s top clients and we will assist them so they can create a new cryptocurrency investment portfolio for their customers. The data we are working with is difficult to work with so we will need to prepare it to be processed to fit the machine learning models. Since there is no known output for what the data provided, we can leverage unsupervised learning for our process. Martha has decided on a clustering algorithm, and we will use data visualizations to share our findings with the board.

### Deliverable 1: Preprocessing the Data for PCA
__________________________________________________________

#### Initial phase of this process we loaded in the data and start our Transform process.

* Here we are keeping all the cryptocurrencies that are being traded.

![image](https://user-images.githubusercontent.com/88467263/147857896-88ede215-9cd6-47f0-8272-a86e9c039e5f.png)

* After filtering the crypto_df DataFrame so it only has rows where coins have been mined we remove the CoinName column from the crypto_df DataFrame since it's not going to be used on the clustering algorithm.

<img width="750" alt="Dop_Coinname" src="https://user-images.githubusercontent.com/88467263/147857947-8b6bc123-405e-4de9-a560-3fa7edddf5d8.PNG">


### Deliverable 2: Reducing Data Dimensions Using PCA
### Deliverable 3: Clustering Cryptocurrencies Using K-means
### Deliverable 4: Visualizing Cryptocurrencies Results
