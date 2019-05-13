+++
title = "Recommendation - Development Phase III"
subtitle ="Content Based Filtering"
date = 2019-05-10T10:24:08-05:00
draft = false

# Authors. Comma separated list, e.g. `["Zeeshan Alam"]`.
authors = ["Zeeshan Alam"]

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["Recommendation System", "TF-IDF", "JBolt"]
categories = ["Educational","Data Mining"]

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["deep-learning"]` references 
#   `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = ["Search Engine"]`.




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
<p> The content covers the development phase III for the data mining class at University of Texast at Arlington under Prof Deokgun Park. the third phase of the development covers the recommendation system where I have implemented
TF-IDF and used content based filtering to recommend the companies based on user similar preference </p>

<p> The link for the complete implementation for the recommendation system can be found below </p>
<h5 align="center"> Link : https://dmsearch.herokuapp.com/recommend </p>
</div>

<h5 align="center"> Dataset </h5>
<p> For this component the dataset has been changed as in previous component the dataset i used had companies name redundent as there were many reviews by different 
users for the same company, but for this one i needed a different dataset with unique company names therefore I used Forbes 2000 Kraggle dataset </p>

<p> Link : https://www.kaggle.com/ash316/forbes-top-2000-companies </p>


<h5> Recommendation Systems </h5>
A recommender system or a recommendation system is a subclass of information filtering system that seeks to predict the "rating" or "preference" a user would give to an item. There are two types of recommendation systems 1) Content Based Filtering 
2) Collaborative filtering. In this project I have used Content Based Filtering


Cosine similarity is the cosine of the angle between two n-dimensional vectors in an n-dimensional space. It is the dot product of the two vectors divided by the product of the two vectors' lengths (or magnitudes).

{{< figure library="1" src="recommend.png" Title="Recommendation System"  >}}

<div style="background-color:#f0f0f0">
<h5 align="center"> References </h5>
<p> https://medium.freecodecamp.org/how-to-process-textual-data-using-tf-idf-in-python-cd2bbc0a94a3 </p>
<p> https://www.analyticsvidhya.com/blog/2018/06/comprehensive-guide-recommendation-engine-python/ </p>
<p> https://towardsdatascience.com/how-to-build-a-simple-recommender-system-in-python-375093c3fb7d </p>
<p> https://www.datacamp.com/community/tutorials/recommender-systems-python </p>
</div>
