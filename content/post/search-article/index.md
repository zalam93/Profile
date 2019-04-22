+++
title = "Search Engine - Development Phase I"
subtitle ="TF-IDF Implementation"
date = 2019-04-21T10:24:08-05:00
draft = false

# Authors. Comma separated list, e.g. `["Zeeshan Alam"]`.
authors = ["Zeeshan Alam"]

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["Search Engine", "TF-IDF", "JBolt"]
categories = ["Educational","Data Mining"]

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["deep-learning"]` references 
#   `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = ["Search Engine"]`.



projects = ["Search Engine"]




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
<p> The content covers the development phase I for the data mining class at University of Texast at Arlington under Prof Deokgun Park. the first phase of the development covers the search engine where I have implemented
TF-IDF and used cosine similarity to find the similarity between the query and the reviews. </p>

<p> The link for the complete implementation for the search engine can be found below </p>
<h5 align="center"> Link : https://dmsearch.herokuapp.com/ </p>
{{< figure library="1" src="search-page.png" Title="Dataset"  >}}
</div>

<h5> Github Link </h5>
<p> https://github.com/zalam93/search-dm </p>

<h5 align="center"> Dataset </h5>
<p>The dataset has 17 fields and represents reviews from the current and previous employees of that company. the fields that were useful for my search engine is Pros and Company. Pros contains the positive
reviews of the employeers about the current/previous companies. I decided not to include summary field as the text in that field was not clear and I found using "Pros" was giving me better accuracy and it has 
proper review comment. There was another field of interest which is "Cons" which has negative comments by the users for the companies though as I am focusing about finding the right company for the user in terms of the positive attributes
there fore I decided to neglect the "Cons" field and worked only on "Pros" field with the correlation with the "Company" field in this search project.</p>
{{< figure library="1" src="dataset.png" Title="Dataset"  >}}


<h5> What does TF-IDF means? </h5>

<p>
Tf-idf stands for term frequency-inverse document frequency, and the tf-idf weight is a weight often used in information retrieval and text mining.
 The importance increases proportionally to the number of times a word appears in the document but is offset by the frequency of the word in the corpus. 
</p>

<h5> Understanding the Basic Algorithm </h5>
<p> 
The TF*IDF algorithm is used to weigh a keyword in any content and assign the level of importance to that keyword based on the number of times it appears in the document. More importantly, it checks how relevant the keyword is throughout all the document, which is referred to as corpus.
TF*IDF is a weighting factor for features, the more weight of the feature the more that type of term occurs in the specified document which is offset by the number of times the word appears
in the entire document which eventually helps removing common words (stop-words in programming terms) in the language.
For a term t in a document d, the weight Wt,d of term t in document d is given by:
<p>


<p align="center"><b> Wt,d = TFt,d log (N/DFt) </b></p>

<p>
Where:
</p>

- TFt,d is the number of occurrences of t in document d. </br>
- DFt is the number of documents containing the term t. </br>
- N is the total number of documents in the corpus. </br>
</p>

the log above is basically used to dumpen the effects of IDF Function
<p align="center">Smoothing for IDF : log( 1 + N/ |{dED : tED}| ) </p>
The smoothing factor is used for introducing the lower bound of log(2) so that nothing will ever be multiplied by 0 by the IDF.

{{< figure library="1" src="code.png" Title="Dataset"  >}}

Cosine similarity is the cosine of the angle between two n-dimensional vectors in an n-dimensional space. It is the dot product of the two vectors divided by the product of the two vectors' lengths (or magnitudes).
here cosine similiary is used to find the similarity between the query and the documents.

<p>
The link for the web is available on the top of the blog page. I have developed the web app using python django framework and the script which is being called when a user types and clicks the button is 
acting as the intermediate web service. The web application is hosted on free hosting site Heroku</p>

</p>

<h5 align="center"> Challenges </h5>
There were many challegens to complete the search feature. the first and foremost was to learn the TF-IDF algorithm implementation as whole and to implement it properly to get the better accuracy in the result.
Initially my idea was to go for mobile application but Windows 10 Home does not support Hyper-V so I was not able to run emulator to test and build my code and on top of that not having android phone wasn't a big help either so I had to
change my plans from mobile app (android) to web application. I built this using Django framework where I just read the documentation and learning was not a big issue.

The deployment was a big mess as Heroku's documentation is not that accurate. There were many issues while deploying the web application. If i solve the first issue it leads to another issue and so on. Finally
after checking errors through log files and fixing all of them I successfully deployed my web application.

Most of the code was simple as I just used tutorial and built in library but the challegen there was to understand how it works (cosine-similiary, TF-IDF) and how it is interlinked in the code from the library i used.
I tried to optimize the search query response time that was challenging part for me for that I had to read the book provided by Prof in the class syllabus.

<div style="background-color:#f0f0f0">
<h5 align="center"> References </h5>
<p> https://medium.freecodecamp.org/how-to-process-textual-data-using-tf-idf-in-python-cd2bbc0a94a3 </p>
<p> https://towardsdatascience.com/tfidf-for-piece-of-text-in-python-43feccaa74f8 </p>
<p> https://github.com/Heetmadhu/Movie-Recommendation/blob/master/MovieSearch.ipynb </p>
<p> https://scikit-learn.org/stable/modules/generated/sklearn.feature_extraction.text.TfidfVectorizer.html </p>
<p> https://github.com/mohdkashif93/tf-idf-implementation </p>
</div>
