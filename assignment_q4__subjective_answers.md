
Q4.A]

In A part, We have image of size 300*300. We have to increase its resolution by a factor of 2. So we used linear regression based interpolation approach. 

Here are our observations

   1) We have observed results by using different basis funciton of linear regression. At the end, we divided the entire image into 2*2 sized patches. Now we trained sklearn's 
      linear regression on 4 corner datapoints of patch and predict for intermediate points of patch. 

   2) We got good image after upscaling but overall image is pixeleted. 


Q4.B]


In B part, we down scaled input image of size 400*400 to 200*200. using this down scaled image, we trained linear model using 10000 features and 1000 epochs. 

Here are our observations


1) Due to computational limitation, we only trained for 10000 rff features and 1000 epochs. Due to that image is not having good resolution. But the constructed image is comparable to the original image. 


Q4.C]


In C part, We had image of size 300*300 and we masked 10,20,30,40,50,60,70,80,90 percentage pixel of original image. 

Here are our observations

1) As we increase the masking percentage, the actual data(pixels in RGB) used for training would decrease. Due to that the model contains high bias and low variace towards training points. 
Hence image are not properly constructed for high masking percentage.



