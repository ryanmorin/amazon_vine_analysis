# Amazon Vine Analysis

## Purpose of the Analysis
The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

The analysis uses the luggage dataset and PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin (see links at the bottom of the page for screen shots of the loaded data). Next, the analysis uses PySpark, Pandas, or SQL to determine if there is any bias toward favorable reviews from Vine members in your dataset. The analysis looks only at the number of 5 star ratings in the 'vine' and 'not vine' datasets. The dataset was further thinned down.  We filtered for those ratings where there were at least 20 votes for a product and the ratio of helpful_votes to total_votes was greater than 50%.

## Results

Overall there were 6711 luggage reviews.  Of that, 51.5% of the reviews (3458) were five star reviews.

![all](https://github.com/ryanmorin/amazon_vine_analysis/blob/main/all.png)

Most of the reviews are not associated with the Vine program (6690). The percentage of five star reviews was essentially the same as the overall average.

![not-vine](https://github.com/ryanmorin/amazon_vine_analysis/blob/main/vine.png)

Very few of the reviews were affiliated with the vine program (21).  The percentage of five star reviews was lower than the overall.  47.6% of the vine reviews were scored as five stars.

![vine](https://github.com/ryanmorin/amazon_vine_analysis/blob/main/vine_y.png)

## Summary

There doesn't appear to be any positivity bias regarding the vine reviews.  The products participating in the vine program have fewer 5 star ratings compared to those products not participating in the program. There could still be bias. An additional test could look at the average rating for the various categories.  If there was bias one would expect to see a higher average rating for the vine products.  The average could then be tested to see if the difference is significant to provide a more definative answer.


### pgAdmin loaded data screen shots
![](https://github.com/ryanmorin/amazon_vine_analysis/blob/main/customers_table.png|width=50px)


