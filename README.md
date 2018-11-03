# NeuroFlow-Tasks

## Description of Files

### Part_1.py

This file does some visualization with the four datasets given. I have also chosen to create a new metric, which I have titled "Overall Wellness", which serves to better visualize and quantify the progress a patient is making. I have established this metric by simply combining the values of the four metrics given, and normalizing the results. In my opinion, this metric has the potential to be individualized for each patient by giving more weight to certain metrics in the calculating of the "Overall Wellness" metric.

### Part_1svm.py

I have trained and tested a SVM using the `sklearn` package that can classify if a patient is stressed or not based on the values they have given for "sleep" and "mood". I decided that I would classify a patient as "Stressed" if they gave a value of stress that was greater than or equal to 4; any other value would classify them as "Not Stressed". I trained the classifier by using the data given, and tested the classifier by taking a portion of the data. The results are shown below:
```
              precision    recall  f1-score   support

Not Stressed       0.84      1.00      0.91        16
    Stressed       0.00      0.00      0.00         3

   micro avg       0.84      0.84      0.84        19
   macro avg       0.42      0.50      0.46        19
weighted avg       0.71      0.84      0.77        19

/Users/matthew/Library/Python/3.7/lib/python/site-packages/sklearn/metrics/classification.py:1143: UndefinedMetricWarning: Precision and F-score are ill-defined and being set to 0.0 in labels with no predicted samples.
  'precision', 'predicted', average, warn_for)
[[16  0]
 [ 3  0]]
```
The SVM predicted "Not Stressed" 19 times, and predicted "Stressed" 0 times, while in reality, the patient gave values for "Not Stressed" 16 times, and gave values for "Stressed" 3 times. My rationale for creating this classifier was that when the prediction given by the classifier does not match up with with the state the patient is in, this could raise a red flag to providers. 

### Part_2.py

I used `sqlite3` to ultimately create a function that takes in a month (1 for January, 2 for February, etc.) and returns a statement that states the percentage of users that have completed a exercise in their first month. 

## Running the Code

* Download Python 3.7.1
* Download a Python IDE (preferably PyCharm)
* Install the necessary packages 
     * pandas (0.23.4)
     * numpy (1.15.2)
     * matplotlib (3.0.0)
     * sklearn (0.0)
     * scipy (1.1.0)
* Download python scripts and upload to PyCharm
