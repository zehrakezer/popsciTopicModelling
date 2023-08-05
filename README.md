# Topic Modelling(Unsupervised ML) on Scientific News Articles

In this project, I will describe how I categorize scientific news articles with unsupervised ML.

As we know, the volume of scientific literature published every day is growing exponentially and it can be quite difficult for researchers, journalists and others to keep up with the latest developments and trends in their field.

In this project, I will share with you the results of the subject modeling analysis that I carried out on a data set consisting of scientific news articles.

Popular science is a popular science journal that started to be published in America in 1872. The magazine, which appeals to the general reader, examines the subjects of science and technology.

I pulled the text data that I will analyze from the popular science website. I analyzed them using LDA algorithm with many different libraries in python.

My dataset consists of 9600 scientific articles published online on the popular science site. The data generally includes subheadings of science, technology, health, DIY, gear, and environment. In these articles, I shot the title, abstract, category and the first paragraph of the article.


We can see the keywords for each topic and the weight of each keywords:
* When we look at topic 1, we see that it is mostly in technological devices. We can classify this category as technology. 
* When we look at topic 3, we see that there are more temporal things.
* When we look at Topic 5, there are more energy-related things, 
* Topic 2 for some reason children's things, 
* Topic 4 health and 
* Topic 6 spatial words.
![image](https://github.com/zehrakezer/popsciTopicModelling/blob/main/1.png)

When we look at it in general, although it is similar to the main topics, there is not much clarity.


Let's visualize it a little more, wordcloud shows the Energy, Space, Covid topics very clearly if we look at the very specific ones.
![image](https://github.com/zehrakezer/popsciTopicModelling/blob/main/2.png)
![image](https://github.com/zehrakezer/popsciTopicModelling/blob/main/3.png)
![image](https://github.com/zehrakezer/popsciTopicModelling/blob/main/4.png)


With another visualization method, pyLDAvis, we can see the distance between subjects. To get the best results is to change the parameters so that they do not conflict.
![image](https://github.com/zehrakezer/popsciTopicModelling/blob/main/5.png)
As can be seen in this image, since topic 4 and topic 1 overlap, we can get more logical and consistent results by treating them as a single topic.

Let's look at the single topic in detail
![image](https://github.com/zehrakezer/popsciTopicModelling/blob/main/6.png)
In topic 5, we can see especially energy and its types.


However, when we look at it in general, the distance between the subjects is quite far from each other. Therefore, it seems that the desired result can be obtained when we reduce the number of subjects to 5

As a result, I analyzed the LDA algorithm of the scientific news articles I pulled from the popular science website and by looking at the visualization results, we saw that we could get good results with 5 topics. This shows that some topics are close to each other.






