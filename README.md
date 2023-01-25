# Amazon_Vine_Analysis
 
## Overview

This analysis seeks to compare the frequency of five-star Amazon product reviews according to whether the reviewer was a member of Amazon's Vine paid reviewer service. This specific analysis is performed on a table of wristwatch reviews, chosen from several datasets available [here](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt). The data was ETL'd with PySpark, and the analysis was performed in a Jupyter notebook with Pandas.

## Results

### The following analysis was performed only for reviews which met two conditions: >= 20 votes and >= 50% "helpful" votes

Totals of Vine and non-Vine reviews:

![vine and non-vine totals](/images/totals.png)

Totals split up by star rating:

![totals split up by star-rating](/images/groupby_aggs.png)

Rating distribution by Vine/non-Vine - non-Vine on top and Vine on bottom:

![star frequency by review type](/images/hist.png)

Key takeaways:

- Of the 8,409 total reviews 8,362 were not through Vine, while 47 were through Vine.
- 4,332 non-Vine reviews were 5-stars, while 15 Vine reviews were 5-stars.
- 52% of non-Vine reviews were 5-stars, and 32% of Vine reviews were 5-stars.

The number of Vine reviews was significantly smaller than the number of non-Vines, which makes it difficult to draw conclusions from this analysis.

## Summary

Without more data I would be hesitant to say that Vine reviews exhibit a negative bias, despite the clear difference in 5-star frequency. This is because the number of Vine reviews in our dataset is so small, which makes me worry that it may not represent the larger review population. This project only required analysis of one dataset, but I would like to perform this analysis on each dataset in the collection. It would be interesting to see if there are any differences between product types, and having more data to analyze would help me come to a more clear conclusion.