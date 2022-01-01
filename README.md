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

* se the get_dummies() method to create variables for the two text features, Algorithm and ProofType, and store the resulting data in a new DataFrame named X.

![image](https://user-images.githubusercontent.com/88467263/147858023-2113dadb-e126-4e10-a45e-49527590ee63.png)

* Use the StandardScaler fit_transform() function to standardize the features from the X DataFrame.
<img width="750" alt="X_Scaled" src="https://user-images.githubusercontent.com/88467263/147858068-bd39f89d-78b1-4625-8285-5fadb5761afb.PNG">


### Deliverable 2: Reducing Data Dimensions Using PCA

* Create a new DataFrame named pcs_df that includes the following columns, PC 1, PC 2, and PC 3, and uses the index of the crypto_df DataFrame as the index.

<img width="750" alt="transform_PCA" src="https://user-images.githubusercontent.com/88467263/147858099-72fed8d8-c90b-46c7-b2e2-220df6528984.PNG">


### Deliverable 3: Clustering Cryptocurrencies Using K-means

* Create an elbow curve using hvPlot to find the best value for K from the pcs_df DataFrame created and run the K-means algorithm to predict the K clusters for the cryptocurrencies’ data.

![image](https://user-images.githubusercontent.com/88467263/147858125-32328092-cfbf-41cf-b69b-d62ae4dd19b1.png)
![image](https://user-images.githubusercontent.com/88467263/147858134-e3b04208-9e41-4ccf-b040-19557cfc1b6d.png)




* Create a new DataFrame named clustered_df by concatenating the crypto_df and pcs_df DataFrames on the same columns. The index should be the same as the crypto_df DataFrame.
* Add the CoinName column that holds the names of the cryptocurrencies.
* Add another new column to the clustered_df named Class that holds the predictions.

![image](https://user-images.githubusercontent.com/88467263/147858214-5f9df836-c00c-4e50-b824-e420614ce99c.png)

### Deliverable 4: Visualizing Cryptocurrencies Results
<img width="374" alt="scatter_3d" src="https://user-images.githubusercontent.com/88467263/147858244-1842e741-5c72-4e93-b1d4-70bd55dd463a.PNG">

