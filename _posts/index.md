---
layout: post
title: "I believe every human has a finite number of heartbeats. I don't intend to waste any of mine."
date: 2020-01-30 23:45:13 -0400
background: '/img/posts/05.jpg'
---



## NAVIGATING THE MAZE OF THE MIND :

### INTRODUCTION : 
Step right up to the surprisingly insightful world of Wikispeedia, a game where the simple act of hyperlink hopping transforms into a treasure hunt through the vast expanse of Wikipedia. It's a straightforward challenge: dart from one article to another, utilizing solely the intertwined links crafted by a multitude of creators worldwide.

On the surface, it is most straightforward — just find a series of clicks to get from point A to B and voilà, you've won. But don't let the simplicity fool you. Under this simple surface, we find a wealth of information filled with insights about our shared curiosity and the hidden patterns of how we think and explore.

// TODO modify meme if needed : 
![HeatMap_finsihed_up](/graphs/wikispeedia_treasure_meme.png)



Join us as we navigate the intricate web of Wikispeedia. We'll follow the paths through a sea of information and discover unexpected gems of knowledge. You never know what secrets we'll find in the simple twists and turns of this online game. Let's figure out the mysteries of our digital travels and uncover what really makes this internet journey tick.

### EXPLORING THE DATA 

The Wikispeedia game dataset is a collection of 4604 articles spanning 129 semantical categories from geography to . 



Players are tasked to go from one article to the other using the intr :

![incoming links distribution](/graphs/Outgoing_link_distribution.png)

![incoming links distribution](/graphs/Inoming_link_distribution.png)

### SUCCESSFUL VS UNSUCCESSFUL

Players who played the game formed 405,835 paths - 256,585 successul and 149,250 unsuccessful- using the inter article links. What constitutes a wining strategy and is there a true difference between successful players and unsuccessful players, we peel the layers of player patterns one by one to see where the difference lies :
- #### Layer 1 : Strategy #### 
- #### Layer 2 : Player Knowledge #### 
- #### Layer 3 : Source and Target Properties #### 

//TODO : this graph can be removed 
![pyramid graph Page Rank](/graphs/path_length_distribution.png)

#### GAME PLAN - THE HIKE TO SUCCESS 

We first uncover the common strategy of players playing the game. Human intuition when navigating from a point A to point B in an unmapped environment (//TODO look for paper that proves this intuition if possible) dictates finding the known point C most propbable to be linked to both points. 
We therefore need a measure of "popularity" of an article in this environment that has to take into considertion the non-symetric roads (links) nature of our environment : 
We use the Page Rank algorithm for this task and find the follwing patterns 

![pyramid graph Page Rank](/graphs/PR_pyramid_graphs.png)


Our intuition for human navigation is confirmed and we can clearly see the split of paths into 2 parts : 
- UpPath : The left part of the mountain = search for the most useful central node in our search 
- DownPath : The right part of the mountain = The search for the target from the central node

However this strategy is present in both successful and unsuccessful paths, so if there is a difference, it is cause by a deeper. 



#### PLAYER KNOWLEDGE - //TODO : change title 

#### most popular subjects 
 ![most popular subjects ](/graphs/Top_topics_graph.png)

So you're using the same strategy as otehr players but you're not getting as successful, is it a knowledge problem ? 

We will discern knowledge patterns with the proximity between the different categories in both finished and unfinished paths, we measure this proximity by how often two categories appear in succession when users play the game. We also use the previous split we found between Up path and downpath since generalizing more is easy and therefore not as insightful as the downpath when trying to see cognitive patterns in action 
+ Uppath finished
![HeatMap_finsihed_up](/graphs/HeatMap_finished_up.png)

+ Uppath unfinished
![HeatMap_unfinsihed_up](/graphs/HeatMap_unfinished_up.png)

As we predicted the Up path behaviour is nearly identical. So either the cognitive connections are the same or successful and unsuccessful players alike have no difficulty going up, meaning there is still a chance successful players have "better" knowledge. Which one ios it ? Only one way to find out : 

+ Downpath finished
![HeatMap_finsihed_down](/graphs/HeatMap_finished_down.png)

+ Downpath unfinished
![HeatMap_unfinsihed_down](/graphs/HeatMap_unfinsihed_down.png)

Aha ! The patterns are different, but wait, this isn't what we were expecting. The heatmap  shows that the connections between different subjects in unseccussful paths are stronger than their counterparts, this can be explained by the fact that once players encounter a hard task, they explore new connections, even if it eventually doesn't end in reaching their target.

If this is the case and unsuccessful paths explore as much if not more semantical connections, what makes a path unsuccessful ? 

If failure isn't caused the strategy or the knowledge of the player, only one culprit remains : the game task.


#### GAME DIFFICULTY - //TODO : change title 

The game task is defined by the source article and the target article. We saw that in both finished and unfinished paths getting to a high point is not a problem, therefore the source of the path isn't a problem since the player essentially chooses their favorite starting point during the Up Path (the summit). The target isolation is therefore the cause of player failure (no need to be insecure about your general knowledge if you fail anymore) 

![in degrees difference](/graphs/in_degrees_differrence.png)

//TODO : wait isn't this plot showing the opposite ?!

We conclude that the main factor influencing success is therefore how isolated the target link is way more than any single player factor.

- Intra connections :

We now dive deeper into each subject and get to see in detail the specifities of connections inside each semantical field (the idea here is to get the maps for all fields and get a "complete mind map")
![MM_science](/graphs/Mind_Map_Science.png)
=> make a nice visualization of the mind maps where we press a category and get it's map foreach category

- Visualized learning : 
we discern beteweeen two types of dynamics :
+ Movement Towards the Target : Some categories appear to have moved closer to the target category (the yellow star) in the 'After training' plot compared to the 'Before training' plot. This movement suggests that for these categories, players found more efficient paths after training.

+ Movement Away from the Target : Conversely, there are categories that have moved further away from the target in the 'After training' plot.

This indicates that these players are strengthening their semantic links between concepts. Over time and with experience, players are likely to form sharper associations between related topics, which helps in recalling the pathways more efficiently. For example, a category that moves closer to the target might indicate that players have developed a stronger conceptual link between that category and the target, allowing for quicker navigation.
![learning visualization](/graphs/learning_visualization.png)

- Specific case Analysis :  in this part we analyze the behaviour of the player who played the most games giving us the best opportunity to analyze the learning patterns in an individual, by using multiple statistical tests (we also guess the background of the person based on the learning behavior but this isn't a scientific result)

### CONCLUSION : 
// make a conclusion about the findings and the interesting results of the project 