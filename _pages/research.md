---
layout: archive
title: "Research in Persistent Homology"
permalink: /research/
author_profile: true
---

{% include base_path %}

![](/images/ph_cover.png)

All code for this project can be found on the GitHub repository: 
<a href="https://github.com/edgarlepe/Persistence/tree/master/Project" style="color: blue; text-decoration: none;">GitHub</a>.

## What is Persistent Homology?

Hello, today our research group, Christopher, Edgar, Joshua, and myself - led by Michael and Jade, will talking about Persistent Homology and how we used it to study different typing patterns. 

<center><img src="/images/ph_0th-2.gif" alt="drawing" width="700"/></center>

We will be covering the background information behind Persistent Homology, the research itself and the code we used to study different typing patterns, and the results we found. 

<center><img src="/images/ph_0th-2.gif" width="700"/></center>

So, generally, Persistent Homology can be defined as an algebraic method for discerning topological features of a space created from a data set
Examples of topological features are Connected components, Loops, Voids, and Simplicial Structures,
Which will be furthered explained in this presentation 

First, let’s consider this point cloud, which consists of 19 points in a plane. 

The data seems to generally have a “loop” shape to it. 
But how can we quantify the fact that this has a “loop shape”? 
This is where Persistent Homology comes in 

### Connected Components 
One idea to quantify the “loop” shape is to connect nearby points. 
With 0th Persistent Homology, we have balls or spheres simultaneously growing around each point 
And as the balls are intersecting, they are forming and merging connected components. 
This process can be seen more clearly with this diagram, where different colors are assigned to different connected components. 
When a ball in one connected component first touches a ball from a different one, the connected components merge and become one bigger connected component. 
0th Persistent Homology is tracks the connected components. 
0th Persistent Homology 
So, with the previous point cloud, we can see how the balls grow to a diameter of d, which is the point when the balls all intersect and merge into one connected component. 
Nth homology Quantifying n-dimensional holes 
As we move forward, it is important to note that the nth homology is keeping track of n+1 dimensional holes 
1st Persistent Homology (2 small holes) 
So, with 1st Persistent Homology, we still have balls growing simultaneously around the points, but now we are paying attention to the loops that form and disappear as the balls grow. 
A loop is formed or born when the white space is enclosed around a ring of balls.  
1st Persistent Homology (2 small holes closed) 
As the balls continue to grow, the white space decreases and eventually disappears, being completely filled in by the balls, which we call its death. 
1st Persistent Homology (1 big holes) 
But there is also a larger loop that is born as the balls grow. 
1st Persistent Homology (1 big hole dies) 
Which eventually dies as well. 
2nd Persistent Homology 
With 2nd Persistent Homology, we are keeping track of voids or cavities which also born and die as the spheres around each point grow. 
You can sort of see the voids in this diagram. 
Homology
In simpler terms, we can think of homology as counting these connected components, holes, and voids
But with the figures I have shown so far, we still can’t really compute or quantify anything. 
Simplexes
So, we introduce simplexes.
Starting with a zero-dimensional simplex, we have a point. 
Next, an edge between two points is a one-dimensional simplex
A triangular face is a two-dimensional simplex
A solid tetrahedron is a three-dimensional simples 
And this pattern continues as we go higher in dimensions. 
Simplicial Complex
If we put together simplices together in a way that the intersection between any two simplices is also a simplex, we obtain a simplicial complex, which you can see an example of here. 
Big gif 
Now, returning to our original point cloud and applying the simplexes, we have this diagram which shows the simplicial complex changing as the balls grow. 
The simplicial complex allows us to identify and quantify where the holes are computationally. 
Homology 
So, with higher dimensional data, even though we can’t visualize the data, we can still do the computation, because we have Persistent Homology, keeping track of the loops and voids within our simplicial complexes and data. 








{% for post in site.research %}
  {% include archive-single.html %}
{% endfor %}
