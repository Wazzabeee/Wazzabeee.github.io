---
name: PySpark Distributed Classification vs Scikit-Learn
tools: [Pyspark, Scikit-Learn, MR-ID3, MapReduce, Decision Tree, Scaling]
image: ../assets/img/portfolio/pyspark_distributed_classification/comparison.png
description: Demonstration of the interest of the use of PySpark when dataset scaling factor gets too large. 
---

# PySpark Distributed Classification vs Scikit-Learn

This paper presents a reproduction of the results introduced by Vasile PURDILĂ and Stefan-Gheorghe PENTIUC [1] proposing an algorithm
parallel decision tree learning algorithm with
very good scalability according to the size of the dataset.
size of the dataset. In our work, we will reproduce these results in a local Spark environment.

## Overload scenarios

#### Data Analysis

For the training of the model, I used a machine
with 20 cores, 16GB of RAM and 3.6GHz.

For the data, I used the same as in the <a href="https://archive.ics.uci.edu/ml/datasets/adult" target="_blank" rel="noopener noreferrer">
the article </a>, i.e. a dataset with the objective of predicting the income class of a person from several characteristics such as their age, their country of origin, their work
country of origin, their job, the number of hours worked per week
hours worked per week, etc.
These data were not cleaned. 

Indeed,
a certain number of missing values designated by the
character '?' were still present. Also, a particularity of the dataset was that all fields of
type String had a space at the head of each field.
This information, which may have seemed like a small detail, caused me some trouble at the beginning of the analysis, because
I could not replace the missing values. In
Indeed, I had to replace '␣?' and not '?'.

The data analysis phase showed me that a number of values were missing in the characteristics: workclass, occupation and native-country

{% include elements/figure.html image="../assets/img/portfolio/pyspark_distributed_classification/msno_matrix.png" caption="MSNO Matrix" %}

Above, we find the complete matrix of the dataset
data set with highlighted the places containing
zero values in each characteristic mentioned above.
above. This visualization of the missing values is very often
very often useful, because it allows me to see the dispersion of
and to quickly identify if a complete part of the dataset is unusable or if it is only a question of isolated values distributed in all the entries.
In our case, I decided to delete the rows containing null values for
two reasons. On the one hand, because in this part, it is mainly a question of checking the scaling of the learning and not the accuracy of the model. On the other hand, because
secondly, because since these are categorical data specific to each individual, it would be necessary to systematically find a similar individual to fill in the missing values and this is not possible to do.

#### Results verification

To verify the empirical results shared in the article, I divided the dataset into training and test sets containing respectively, 31,553 and 13 669 entries, respectively. To evaluate the overload scenarios, I defined, as in the article, a scaling factor set to 1 for 5,997,434 bytes (including the training and test datasets). I then duplicated the dataset several times until I reached a scaling factor of
of 112 corresponding to 671,712,608 bytes. From the same way as in the article, I defined a second scaling factor for the execution time where a scale factor of 1 corresponds to 3.55 seconds.
I then measured 5 times the training time of the distributed classification algorithm based on decision trees for each scenario in order to avoid having outliers and obtain the associated standard deviation. 

Here are the experimental results :

{% include elements/figure.html image="../assets/img/portfolio/pyspark_distributed_classification/table.png" caption="Experimental results" %}

Here is the graphical equivalent of the table above : 

{% include elements/figure.html image="../assets/img/portfolio/pyspark_distributed_classification/comparison.png" caption="Scaled Classification" %}

From our results, we can say that the trends presented in the article are respected.
Indeed, the graphical results speak for themselves,
we find respectively the same curves in the article and in the reproduction of the results.
We can however note the slight bending of the curve of the execution time from the scale factor '84'. 

We notice a similar increase of the standard deviation from this same threshold. I think that this is due to the limitations of the Spark environment in local mode.
To validate this hypothesis, we would have to carry out the same tests on a cluster to verify if a similar threshold value is detected or not.


## Demonstration of the need for distribution of learning

In order to demonstrate the necessity of the training distribution, I measured, for the same volume of data and for different
and for different configurations, the training time and the accuracy of a decision tree.
These tests were also carried out with scenarios with 1, 2, 4, 8, 12, 16 and 20 cores.
The tests were performed on the same dataset as before with a scale factor of 64, i.e. 383 835,776 bytes.

Here are the experimental results :

{% include elements/figure.html image="../assets/img/portfolio/pyspark_distributed_classification/multicore.png" caption="Multicore scenarios" %}

In the paragraph above, the scenario remained the same, so there was no increase in model performance due to the number of cores allocated to the Spark environment. Moreover, in section "Results Verification", the accuracy of the model for each scenario is not given, because I only duplicated the same data. Thus, even if there had been an increase in accuracy, it would only have been due to the overtraining of the model on the data because it was repeated several times.

In the general case of Big Data, we are faced with the problem of sampling. Indeed, to facilitate the learning of models and despite the parallelization we are often obliged to use a representative sample of data for training. However, such a sample does not ensure 100% accuracy. 

Generally speaking, the more data we have, the closer we get to reality and therefore the better the performance and accuracy of the model. Frequently, in the context of offline machine learning, when the data set does not fit in the memory, the use of online learning is a good compromise for the performance of the model.

## Used Software and Libraries
- Programming languages: Python
- Libraries: PySpark, scikit-learn
- Source control: GitHub
- Other tools: Jupyter Notebook

## References
[1] Vasile Purdil et Stefan-Gheorghe Pentiuc. “MRTree-A Scalable MapReduce Algorithm for Building Decision Trees”. In : 2014.
