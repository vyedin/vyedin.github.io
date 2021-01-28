---
layout: page
title: Data
tagline: data science, modeling, deep learning
description: 
---

I love working with data, and I am working towards a certificate in data science from Harvard's extension school program. Here are a few examples of data projects I've worked on.

---

### The Modal Voter: GenData 2020 Final Project

For my final project as part of the [Generation Data](https://www.generationdata.org/) Intro to Progressive Data training, I applied statistical methods I learned in one of my favorite Planet Money episodes ("[The Modal American](https://www.npr.org/2019/08/28/755191639/episode-936-the-modal-american)") to our mock campaign data. 

I wrote SQL queries to break voters into demographic "buckets" based on generation, party, sex, and race, and then used Tableau to visualize patterns of voter behavior. 

This presentation was chosen as one of top 6 final projects (out of 20).

<br/><br/>

<p align="center">
<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vRKqgFYAkmTfBKqVjd9hVLthhHHL5RDHiReA8icFVauVOcRKc269TvHOIBdzhyzXw/embed?start=false" frameborder="0" width="640" height="389" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>
</p>

---

### Classifying Building Types: Image Classification for Colloquial Architecture

My final project for the Deep Learning course at Harvard in fall 2020 was an image classifier for common American houses as defined by Virginia Savage McAlester in _A Field Guide to American Houses_. 

I trained a VGG16 image classification model in Keras on a custom dataset. I leveraged transfer learning, image augmentation, dataset balancing, and fine tuning to classify 10 common styles of houses at 86% accuracy.


<p align="center">
<iframe width="560" height="315" src="https://www.youtube.com/embed/4UlEgA22lpE" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</p> 

---

### Flipper: Real Estate Classifier

<p align="center"><img src="../flipper1.png" alt="Flipper" width="600"/></p>

Flipper was a final group project for a course I took with [Zona Kostic](https://www.zonakostic.com/about.html) in summer 2020. My team had access to a subset of Greater Boston MLS (real estate) data from the past 10 years. Our goal was to determine whether a property had flip potential _without_ using listing photos or descriptions, and discern which predictors contributed most to a given listing's flippability. This was a classic data science problem - no deep learning required. 

I owned the data science portion of the project and used a random forest classifier, training the model on past flips we found in the listings augmented with SMOTE to create a more balanced data set. You can browse the full notebook [here](https://github.com/gregfrasco/real-estate-price-predictions/blob/master/notebooks/basic_model.ipynb).

<p align="center"><img src="../flipper2.png" alt="Flipper" width="600"/></p>
<p align="center"><img src="../flipper3.png" alt="Flipper" width="600"/></p>

Getting the model to make accurate predictions using listing metadata was a challenge, but we were able to classify non-flippable properties with ~98% accuracy and classify flippable properties with just under 70% accuracy. Our team was the runner up for best final project with the Flipper model and site.

Collaborators: [@gregfrasco](https://github.com/gregfrasco) and [@goudete](https://github.com/goudete).
