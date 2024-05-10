I: Matrix Factorization with Missing Rectangular Blocks:

I (A) Loss Evolution:

    The loss values during matrix factorization using ALS decrease over epochs, indicating convergence.
    The initial loss is relatively high, gradually decreasing as the model iteratively updates factorized matrices (W and H).


I (B) Effect of Missing Block Size:

    Larger missing rectangular blocks lead to higher final losses, which is expected since the algorithm needs to infer larger portions of the image.

I (C) Convergence Speed:


    Convergence is relatively slower for larger missing blocks as the model requires more iterations to accurately reconstruct the image.


                -------------------------------x-------------------------------

II: Matrix Factorization with Randomly Missing Pixels:

II (A)     Loss Behavior:

    Loss values during matrix factorization with randomly missing pixels show a similar decreasing trend as in the case of missing rectangular blocks.

II (B)  Random Pixel Masking Impact:

    Loss values are generally higher compared to the missing rectangular block case, indicating that randomly missing pixels pose a more challenging reconstruction problem.

                -------------------------------x-------------------------------

III Linear Model + Random Fourier Features (RFF):

III (A): Loss Evolution:

    The loss values for the linear model with RFF features decrease during training, demonstrating the model's learning process.

III (B): Impact of Random Pixel Masking:

    Loss values for the linear model with RFF are generally higher when dealing with randomly missing pixels, suggesting that this method may be more sensitive to random pixel masking.

                -------------------------------x-------------------------------

                                    Overall Trends:

1. Loss Comparison:

Matrix factorization tends to achieve lower final loss values compared to the linear model with RFF features.

2. Sensitivity to Missing Data Type:

Matrix factorization methods are relatively robust to missing data, while the linear model with RFF may be more sensitive, especially when dealing with random pixel masking.

3. Computational Efficiency:

The computational efficiency of matrix factorization may be affected by image size, whereas the linear model with RFF appears to be less computationally expensive.

4. Potential for Improvement:

Further tuning of hyperparameters and training for additional epochs may lead to improved loss values for both methods.