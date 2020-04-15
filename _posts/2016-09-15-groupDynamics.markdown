---
title: Group Dynamics
layout: post
categories: General
excerpt: This post uses the framework of graph theory to analyze group outings, especially lunches and dinners.
---


Consider a mathematical representation of a group of people. Each person is represented by a point called a *node* or a *vertex*, and the relationship between any two persons is denoted by an *edge* between them. A fully connected network of people is one where each person is related to the other, and so there is an edge between every pair of individuals in the group.

<figure> 
	<img src="/assets/posts/2016-09-15-groupDynamics/fig1.png" width="65%" height="65%" />
	<figcaption> A group </figcaption>
</figure>


Generally, no two persons share the same type of relationship. This means that we must find a way to represent edges that reflects this observation. We can do that by weighting the edges, thicker edges imply greater affinity between a pair of people, thinner edges correspond to lesser affinity. The same thing can be represented numerically by what is called an *edge weight* between two nodes. The more positive the weight, the greater the familiarity between the individuals. A small positive value indicates reasonable familiarity, and a negative value may mean that the two people have never met before, or have an intense dislike for each other. Now the aim of a group outing should be to maximize the “happiness” of as many individuals as possible. This seems to be a fair objective that the group should adopt. We can model individual happiness as follows : The individual should be a part of conversations that interest him, the more the better. In what follows, I will point out some general features of group outings, and finally draw up a heuristic that maximizes group happiness.  <br><br>


**Large groups suck**  - This is invariably the case, and for obvious reasons. What happens in large groups is that the distribution of the edge weights is highly non-uniform, which means we have people who have never met each other before, or are not very comfortable being together. Some variation in the weights is inevitable, but we must try to stick to the uniform distribution as much as we can.  <br><br>


**As interests diverge, quality of discussions go downhill**  - We are all unique, have different interests, tastes, opinions. Large groups cannot accommodate diverse interests. As a result, groups end up doing one of the following. Either they split into subgroups, each discussing something that interests them, or they all start discussing the most banal things in life - food, cinema, politics. The Indian mentality is yet to rise above these things. The group can’t be blamed for it. When you have ten people sitting across a table and eating sweets, and one of them comments that the sweet tastes sweet, the rest have to put up with it, however meaningless the statement.  <br><br>

**Individuals who should avoid group outings**  - An advice for all those who are planning to attend a group dinner - make sure that you can at least understand the “group-language”, the language spoken by most people in the group. In one of my group outings I happened to sit right in the middle of a long table. There were five people to my left, five to my right. These two sub-groups were busy jabbering in Hindi among themselves. Occasionally one subgroup would unleash a few sentences that would be caught by the other group, passing right through me. I don’t blame them. Language is a great factor that assists in social bonding. There is a feeling of natural warmth when we meet people who speak our language. I just pity those non-Hindi speaking “junta” who sit there, tongues tied, ears out of order, not knowing whether to laugh, or to appear serious, and simply keep staring at other faces, or at empty plates. These people usually return from the outing feeling insulted and sidelined. Again, I don’t blame the Hindi speaking group members. The fault lies with the non-Hindi folks - why do they go in the first place? The other group that should avoid such outings are those people who like conversations, but want them to be meaningful. And individuals who fall in either category return from the meeting feeling absolutely hollow - not only did no interesting conversation happen, they were not even in a position to understand what was being spoken. That is, well, pitiable. These people form the the odd-nodes.  <br><br>

**Dominant egos**  - Returning to our mathematical model, if we are ready to give weights to nodes as well, there would be some dominant nodes that would like to hijack the discussions and take the group along with it. All group activity is ultimately that - a clash of egos, as each person tries to assert himself, take the centre stage, and shine in the limelight. Ultimately the strongest ego wins. <br><br>

**Maximizing group happiness**  - We finally come to the optimization problem. There are no closed form solutions available. Instead, I suggest the following heuristic:  <br><br>

> Keep the number of nodes in the graph small.  
 Make the weight distribution of the edges as uniform as possible.  
 Remove odd-nodes from the graph.