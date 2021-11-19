# ICA Data Science Candidate Take Home Task

This is the take home task for the ICA Data Science position.  This task is intended to take no more than a few hours.

In the process of completing this take home assignment, you'll analyze some industry-relevant data.  Use this assignment as a way to show us your thought process as a data scientist.

## Submission Notes

The best way to submit is a Jupyter Notebook since that lets us see your thought process from start to finish.  Alternate submission methods are of course fine, but the submission needs to be **reproducible** by our engineers.  Feel free to clone this repository to your own github repo and use that to submit. Alternately, just zip your work and send us that.

## Task Summary

The data directory contains a selection from the OpenFDA dataset for Medical Device Adverse Events.  This dataset contains 30,000 rows of adverse events data in CSV format.  However, several fields in the dataset contain nested JSON values, which may need to be parsed as part of the task. Additionally, this dataset is not "clean". Some fields are present on certain rows but do not exist on others. 

### Important Fields

Each row in the dataset is an "Event".  Each event pertains to a `patient`, a `device` and the actual "problem' that occured (`mdr_text`), each of which are represented as nested data structures.  Some important values for this assignment are in the nested `device` field.  For instance, `device_report_product_code` inside the `device` field contains the device product code, which we can use as the "device category" for the purposes of this assignment. 

### Instructions

Please complete the following in your submission, and show the code to accomplish each:

1. Exploratory Analysis:
 - Which year had the highest number of recorded adverse events across all devices?
 - Which device category (by product code) had the highest number of adverse events resulting in Injury (not death)?
 - Choose and show a time-series trend of increasing, decreasing or level event frequency by device category. Comment on the confidence of this analysis based on the underlying data.
2. Bonus : The `mdr_text` field often has a detailed text description of the issue that occurred with the device. If there is anything fun or interesting you can think to do with this data, we'd love to see it!