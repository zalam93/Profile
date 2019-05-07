+++
title = "Classification : Machine Learning"
subtitle ="Naive Bayes Implementation"
date = 2019-04-21T10:24:08-05:00
draft = false

# Authors. Comma separated list, e.g. `["Zeeshan Alam"]`.
authors = ["Zeeshan Alam"]

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
# tags = ["Search Engine", "TF-IDF", "JBolt"]
# categories = ["Educational","Data Mining"]

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["deep-learning"]` references 
#   `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = ["Search Engine"]`.


Github Link
https://github.com/zalam93/search-dm

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
[image]
  # Caption (Search)
  caption = "JBolt, Application which tells you about your future company!"

  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = "Left"
+++

<div style="background-color:#f0f0f0">

<p> The link for the complete classifer implementation using Multinomial Naive Bayes algorithm for the classification can be found below </p>
<h5 align="center"> Link : https://dmsearch.herokuapp.com/classify </p>


</div>

<h5 align="center"> Dataset </h5>

<p>The dataset has 17 fields and represents reviews from the current and previous employees of that company. the fields that were useful for my classification is:
  * Benefits Rating
  * Growth Rating
  * Workload Rating
  * Senior Management Support Rating
  * Company Ranking
  
  My classification works on the numerial fields which are mentioned above

{{< figure library="1" src="dataset.png" Title="Dataset"  >}}


<h5> What is Classification? </h5>

<p>
Classification separates observations into groups based on their characteristics. For exampls, students applying to engineering schools could be separated into potential acceptance, maybe accepted, and unlikely expected based on grades, GRE scores, industrial experience, and outstanding activities.
</p>

**Algorithm Used**
**Multinomial Naive Bayes Classification:*
Naive Bayes is a machine learning algorithm for classification problems. It is basically based on Bayes probability theorem. this algorithm is one of the simplier algorithm and fast to build models and it makes predictions with Naive Bayes algorithm.


****Bayes’ Theorem is stated as:****

***P(h|d) = (P(d|h) * P(h)) / P(d)***

***f1,f2,f3,....fn = fields in the dataset***
****This application classifies company based on the values from the following field****
- Work-life balance
- Ranking
- Cultural ratings
- Growth Opportunities ratings
- Benefits rating
- Senior Management
{{< figure library="1" src="classify.png" Title="Dataset"  >}}

***Code (Classifier):***
The function below counts the number of times a company occur in the dataset where name is the variable which is the name of the company for example : Google, Facebook, Netflix, Amazon

     def count(name):
        n_count = data['Company'][data['Company'] == name].count()
        return n_count

The function below takes the company name count by calling the count function then divide the count by the total number of rows in the dataset to get the Probability count of the company name
    def P_count(name):
        P_company = count(name) / n_rows
        return P_company

Following are the two main steps in the Naive Bayes Algorithm:

**Calculating mean**:

    mean = data_means[col][data_var.index == name].values[0]

****Calculating variance****:
 
     variance = data_var[col][data_var.index == name].values[0]
****Calculating Likelihood****
 P(X|Y): Probability of X given Y:
 
       p = 1 / (np.sqrt(2 * np.pi * vy)) * np.exp((-(x - my)**2) / (2 * vy))
       
****Formula for the Algorithm****:

where name is the variable which represents the name of the company

        result = P_count(name) * \
            Px_given_Py(c0, calc_mean('Workload', name), calc_var('Rating', name)) * \
            Px_given_Py(c1, calc_mean('Workload', name), calc_var('Workload', name)) * \
            Px_given_Py(c2, calc_mean('Culture', name), calc_var('Culture', name)) * \
            Px_given_Py(c3, calc_mean('Growth', name), calc_var('Growth', name)) * \
            Px_given_Py(c4, calc_mean('Benefits', name), calc_var('Benefits', name)) * \
            Px_given_Py(c5, calc_mean('Management', name), calc_var('Management', name))
            




<p>
The link for the web is available on the top of the blog page. I have developed the web app using python django framework and the script which is being called when a user selects the options and clicks the button is 
acting as the intermediate web service. The web application is hosted on free hosting site Heroku</p>

</p>

<h5 align="center"> Contribution </h5>
**Implementation of the Algorithm from scratch**:
- Reading the file (dataset)
- Only extracting the columns required for the classification out of 17 fields (['Company', 'Rating', 'Workload', 'Culture', 'Growth', 'Benefits', 'Management'])
- Training the data and then testing the data for the classification
- Calculation of mean and variance
- Calculating the Likelihood probability
- Function that labels the data for classification based on naive bayes algorithm


**Accuracy**
- For accuracy the more training data given to the training set the more accurate it would be for the classification

<div style="background-color:#f0f0f0">
<h5 align="center"> References </h5>
<p> https://www.kaggle.com/rakeshrau/social-network-ads </p>
<p> https://chrisalbon.com/machine_learning/naive_bayes/naive_bayes_classifier_from_scratch/</p>
<p> https://medium.com/machine-learning-algorithms-from-scratch/naive-bayes-classification-from-scratch-in-python-e3a48bf5f91a </p>
<p> hhttps://towardsdatascience.com/na%C3%AFve-bayes-from-scratch-using-python-only-no-fancy-frameworks-a1904b37222d </p>
</div>
