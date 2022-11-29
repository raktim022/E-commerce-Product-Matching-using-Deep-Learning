# E-commerce-Product-Matching-using-Deep-Learning

After downloading the data, basic preprocessing was done which included removing null values and redundant features. Some features were modified in accordance to the task at hand. 
<br>

Two different approaches were taken for this task.
<br>
* #### Using Word Embeddings and Cosine Similarity ####
  * For this task, the dataset was filtered by the product brand and features to obtain a smaller and more accurate pool of data, and hence, reduce time for calculations.
  * Then, the description of each product of Amazon dataset was embedded into vectors using Sentence transformer. 
  * For each Flipkart product, the Cosine Similarity of the description of the product was calculated with every product of the filtered Amazon list, and the product with the highest scored was considered as the match for the Flipkart product.
* #### Using OpenCV and PIL for Image Similarity ####
  * For this approach, after the initial filtering, the url's of the images were converted into OpenCV images using PIL and OpenCV.
  * Then, the image of the Flipkart product was matched with the filtered Amazon products, and Mean Squared Error, i.e., the distance between the images were calculated.
  * The image with the minimum diatance was considered as the match.
<br> <br>
The Word Embedding approach is a lot more accurate and took far less time as compared to the Image Similarity, so that approach should be considered for Product Matching.
