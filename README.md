# 4_Signature_Verification
Pattern Recognition - Task 4

## Getting started
Download the files given for this task and put everything in a folder named "groundtruth"

## Results
### Data preparation and features

### DTW
* For each user, a mean dissimilarity between the 5 genuine signatures is computed. It will be used to decide if a signature is valid or not.
* For each user, every verification signature is compared to the 5 genuine signatures. The mean dissimilarity is stored for each verification signature.

### Evaluation
* In order to know if a verification signature is accepted as genuine or fake, we compare the mean dissimilarity of it with the one obtained between the 5 genuine signatures by a subtraction between the two values. If the result of this subtraction is below or equal to a certain threshold then the signature is valid, otherwise it is a fake. The optimal threshold was chosen by evaluating the accuracy of the predictions with the ground-truth.

![Accuracy](images/accuracy.png)

* The maximal accuracy obtained is 88.59%

* Then the precision and recall curve is the following one with an AP=0.917 :

![Final_curve](images/precision_recall_curve.png)
