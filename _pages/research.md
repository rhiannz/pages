---
layout: archive
title: "Research in Persistent Homology"
permalink: /research/
author_profile: true
---

{% include base_path %}

![](/images/ph_cover.png)

This research project utilizes persistent homology to examine student typing data collected from online proctoring sites and identify trends indicating academic misconduct. Topological data analysis is applied to evaluate the algebraic facets of the persistence of holes in a given space and display high dimensional data trends. 

The following report will explain the general background information behind Persistent Homology, the code used to study different typing patterns, and the results we found. 

All code for this project can be found on the GitHub repository: 
<a href="https://github.com/rhiannz/Persistence/tree/master/Project" style="color: blue; text-decoration: none;">https://github.com/rhiannz/Persistence/tree/master/Project</a>.

## What is Persistent Homology?

Generally, Persistent Homology can be defined as an algebraic method for discerning topological features of a space created from a data set. 
Some examples of topological features are connected components, loops, voids, and simplicial structures, which will be explained in more detail further down. 

Let us first consider this point cloud that consists of 19 points in a plane:  

<center><img src="/images/ph_cloud.png" width="700"/></center>

We can see that this data seems to have a general “loop” shape. But how can we quantify the fact that this has a “loop shape”? This is where Persistent Homology comes in. 
 
One idea to quantify the “loop” shape is to connect nearby points. 
With 0th Persistent Homology, we have balls or spheres simultaneously growing around each point. 
And as the balls are intersecting, they are forming and merging **connected components**. 
This process can be seen more clearly with this diagram, where different colors are assigned to different connected components. 

<center><img src="/images/ph_connected.png" width="400"/></center>

When a ball in one connected component first touches a ball from a different one, the connected components merge and become one bigger connected component. 
**0th Persistent Homology** is the tracking of these connected components. 
 
So, with the previous point cloud, we can see how the balls grow to a diameter of $d$, which is the point when the balls all intersect and merge into one connected component. 

<center><img src="/images/ph_0th.png" width="700"/></center>
 
As we move forward, it is important to note that *the nth homology is quantifying or keeping track of n+1 dimensional holes*. 

Hence, with **1st Persistent Homology**, we still have balls growing simultaneously around the points, but now we are paying attention to the loops that form and disappear as the balls grow. 
A *loop* is formed or *born* when the white space is enclosed around a ring of balls, as seen in the first figure below. 
As the balls continue to grow, the white space decreases and eventually disappears, being completely filled in by the balls, which we call its *death* (seen in second figure). 
However, as the balls grow, a larger loop is also born (seen in third figure) which  eventually dies as well. 

<center><img src="/images/ph_holes.png" width="700"/></center>
<center><img src="/images/ph_1st.png" width="700"/></center>

With **2nd Persistent Homology**, we are keeping track of *voids* or *cavities* which also are born and die as the spheres around each point grow. 

You can sort of see the voids in this diagram: 

<center><img src="/images/ph_2nd.png" width="550"/></center>

In simpler terms, we can think of homology as counting these connected components, holes, and voids. 
But with the figures shown so far, we still are not able to properly compute or quantify anything. 
So, we introduce **simplices**. 

<center><img src="/images/ph_simplexes.png" width="700"/></center>

Starting with a *zero-dimensional simplex*, we have a point. 
Next, an edge between two points is a *one-dimensional simplex*.
A triangular face is a *two-dimensional simplex*.
A solid tetrahedron is a *three-dimensional simples*. 
And this pattern continues as we go higher in dimensions. 

Moreover, if we put together simplices together in a way that the intersection between any two simplices is also a simplex, we obtain a **simplicial complex**, which you can see an example of below. Hence, simplicial complexes are built from points, lines, 
and triangular faces. 

<center><img src="/images/ph_simpcomp.png" width="450"/></center>


Now, returning to our original point cloud and applying the simplices, we have this diagram which shows the simplicial complex changing as the balls grow. 
The simplicial complex allows us to identify and quantify where the holes are computationally. 





Of course, as our dimensions grow, it becomes increasingly difficult to create clear visualizations of our data. 
However, we can still do the computations, because we have Persistent Homology keeping track of the loops and voids within our simplicial complexes and data. 








{% for post in site.research %}
  {% include archive-single.html %}
{% endfor %}
