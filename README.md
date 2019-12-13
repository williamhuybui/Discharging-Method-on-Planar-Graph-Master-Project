# Discharging Method on Planar Graph
This is the final project for my Master degree in Mathematics with focus on graph theory.

**Projec status**:--Completed

## Introduction

In mathematics, the four color theorem, or the four color map theorem, states that, given any separation of a plane into contiguous regions, producing a figure called a map, no more than four colors are required to color the regions of the map so that no two adjacent regions have the same color.
![Four Colors on Map of United States](https://github.com/williamhuybui/Discharging-Method-on-Planar-Graph-Master-Project/blob/master/Picture/Map_of_United_States_vivid_colors_shown.png)
In 1976, the four color theorem was proved by Appel and Haken using discharging method. The proof is verycomplex, over 400 pages, and it heavily relies on computer.

The process is first using the computer to break down the problem into many smaller cases, then use mathematics to prove these cases. 

In this project, we investigate the technique called **Discharging Method** that was developed to prove the math part of the problem. Later, we use discharging method to solve problems that are outside the scope of Four Color Theorem. One of which is a smaller case of Vizing's conjecture. 

## Result

**Theorem 1**: Every plane graph having no 4-cycle and no j-face with 5≤j≤9 is 3-colorable.
![Discharging rule](https://github.com/williamhuybui/Discharging-Method-on-Planar-Graph-Master-Project/blob/master/Picture/Discharging-tule-theorem1.png)

**Theorem 2**: If G is a plane graph and no two 3-faces sharing an edge, then G is max(∆(G) + 1,8)-edge choosable

The detail of the proof was presented in the attached pdf files. You can also find the LaTex version in the following [link](https://www.overleaf.com/read/brppnmdtttwz) (This require [Overleaf](https://www.overleaf.com/) account)

**References**

Daniel W. Cranston and Douglas B. West, An Introduction to the Discharging Method via Graph Coloring, [arXiv](https://arxiv.org/abs/1306.4434v1). October 11th, 2016. 
