# Discharging-Method-on-Planar-Graph-Master-Project

#1 Introduction

* The discharging method is a technique used to prove lemmas in structural graph theory

* Discharging is most well known for its central role in the proof of the Four Color Theorem

* The discharging method is used to prove that every graph in a certain class contains some subgraph from a specified list.

* The presence of the desired subgraph is then often used to prove a coloring result.

## Four color theorem

{Picture/Map_of_United_States_vivid_colors_shown.png}

* In mathematics, the four color theorem, or the four color map theorem, states that, given any separation of a plane into contiguous regions, producing a figure called a map, no more than four colors are required to color the regions of the map so that no two adjacent regions have the same color. Adjacent means that two regions share a common boundary curve segment, not merely a corner where three or more regions meet

* In 1904, Wernicke introduced the discharging method to prove a theorem which was part of an attempt to prove the four color theorem.

* In 1976, the four color theorem was proved by Appel and Haken using discharging method. The proof is very complex, over 400 pages, and it heavily relies on computer.

# Method 
**Euler's formula**: For a connected planar graph: $$V(G)-E(G)+F(G)=2$$

Multiply Euler’s Formula by $-6$ and split the term for edges to obtain:

$$-6V(G)+2E(G)+4E(G)-6F(G)=-12$$

Since $E(G)=\frac{1}{2}\sum_{v\in V(G)}d(v)$ and $E(G) = \frac{1}{2}\sum_{f\in F(G)}l(f)$  substitute to the equation we get

$$\sum_{v\in V(G)}(d(v)-6)+\sum_{f\in F(G)}(2l(f)-6)=-12$$

If we multiply Euler's formula by $-6$ and split E(G) as similar

$$-6V(G)+4E(G)+2E(G)-6F(G)=-12$$

or multiply by $-4$ split the edge as similar

$$-4V(G) + 2E(G) + 2E(G) - 4F(G) = -8$$

and complete the substitution, we obtain the following proposition.

**Proposition:** Let $G$ be a connected plane graph then the following hold for $G$

$$\sum_{v\in V(G)}(d(v)-6)+\sum_{f\in F(G)}(2l(f)-6)=-12 \text{ (vertex charging)}$$

$$\sum_{v\in V(G)}(2d(v)-6)+\sum_{f\in F(G)}(l(f)-6)=-12 \text{ (face charging)}$$

$$\sum_{v\in V(G)}(d(v)-4)+\sum_{f\in F(G)}(l(f)-4)=-8  \text{ (balance charging)}$$

**General structure of the future proof:** 

* Assume by contradiction that G has none of the configuration

* Initialize charge

* Establish discharging rule

* Calculate final charge (which would contradict with the proposition)

# Lemma 1
Every plane graph $G$ with $\delta(G) \geq 3$ has two $3$-faces with a common edge, or a $j$-face with $4 \leq j \leq 9$, or a $10$-face whose vertices all have degree $3$.

Proof:
Suppose the graph has none of these configuration which means: 

**C1**: No $3$-faces with a common edge

**C2**: Every $j$-face satisfies $j=3$ or $j\geq 10$  

**C3**: Every $10$-face have at least one $4^+$-vertex

Use face charging: $2d(v)-6$ for each vertex, $l(f)-6$ for each face. The only thing that need charge are $3$-faces and they begin with charge $-3$.

**R1**: Each triangle takes $1$ charge from each neighboring face.

**R2**: Each face $f$ takes $1$ charge from each incident $4^+$-vertex lying on the triangle sharing an edge with $f$

Every $3$-face is happy because of R1. $3$-vertices also happy. Let $v$ be a $j$-vertex where $j\geq 4$ and we investigate how much charge $v$ can lose. A triangle incident to $v$ can have at most $2$ neighboring-faces that each can take $1$ charge from $v$. This also require at least $2$ extra edges. These extra edges can also be shared by $2$ triangles.

Therefore, the worst case scenario is when we have triangles and edges alternating. Note that if $3|j$ then $v$ would lose at most $\frac{2j}{3}$
