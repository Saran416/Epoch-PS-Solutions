# Task 1

## Data Cleaning:

- Clearly from printing unique values CircleName and StateName is the same for all the values so there is no need of this data.
- I noticed that there are null values in the Latitude and Longitude so fill these values with the mean of the geographical positions belonging to the same Division.
- I realized that there are some outliers from blox plot, so i removed the points using InterQuartileRange.
- I also checked if there were any duplicated rows.

# Task 2

## My approach to the problem:

I observed that the target images were symmetrical and realized that a simple sliding window can easily iterate over each letter. So I iterated over the image array and in each interaction predicted the letter using CNN that I trained beforehand on the alphabets dataset and added it to the output string. To detect the space I say if the sum of all the pixel values is 0.

Now that I extracted the text from the images, I saw that the sentiment analysis dataset was not too big. So I thought that Deep learning may not work well on the data and I decided to go with clustering.

I vectorized the text using count vectorization, since the vocabulary size is also small(because of the small dataset) and using KNN I predicted their sentiments.

I also tried predicting the sentiments using LSTM (just for the sake of experimentation) and as expected the model was unable to predict properly.
