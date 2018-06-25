# Temporal-Matching in link-streams

## What is it about?

A link-stream is a sequence of pairs of the form (t,{u,v}), where t ∈ N represents a time instant and u ̸= v.

![alt complex_network_example_svg](https://www-complexnetworks.lip6.fr/~latapy/test5.svg)

Given an integer γ and a link-stream L, the γ-link-stream of L is the set of temporally consecutive edges defined as {(t′, {u, v}) | t′ ∈  t, t + γ − 1 }, the sequence of all the γ-edges between vertices u and v, starting at time t.

The maximum temporal matching of a γ-link-stream is a maximum sized subset of its γ-edges, such that there is no pair of y-edges that "overlap".
Calculating a maximum temporal matching is NP-hard, we introduce a way to compute a 2-approx with a greedy algorithm, and to compute a quadratic kernel in polynomial time.

### An example of a link-stream
![alt simple-link-stream-example-txt](/simple-link-stream-example.png)
Here is a more fancy representation of these link-streams
![alt simple-link-stream-example-img](/simple-link-stream-horizontal-image.png)

### The 2-approximation algorithm
A simple greedy algorithm can compute a 2-approximation for the maximum temporal matching of a γ-link-stream.

Given a link-stream L with n edges and an integer γ, the γ-link-stream can be computed in O(n^2).
It is equivalent to sort the edges of L, then for each of them, look if there are (γ-1) consecutive edges after this one.

Then, given an γ-link-stream γ-L, the 2-approximation can be computed in O(n^2).
To do so, we build a subset of γ-L by taking e, its first γ-edge, adding it to the 2-approximation edges list, and removing every γ-edges of γ-L that overlaps with e. We loop while γ-L is not empty.

Overall, the worst case complexity of this 2-approximation algorithm is O(n^2), and is obtained when there are no edges overlapping in the original link-stream.

### Section 1-b

Du texte du texte du texte

* [Test_1](http://google.com) - Un moteur de recherche
* [Test_2](https://maven.apache.org/) - Un autre moteur de recherche

* **Antoine Roux** - *Un essai* - [Superzenith](http://superzenith.com)

## Section 2

### Section 2-a

Du texte du texte du texte

### Section 2-b

Du texte du texte du texte

{
    "plugins": ["scripts"],
    "pluginsConfig": {
        "scripts": {
            "files": [
                "./index.js"
            ]
        }
    }
}

### Section 2-c

Du texte du texte du texte

## Section 3

### Section 3-a

Du texte du texte du texte

### Section 3-b

Du texte du texte du texte

### Section 3-c

Du texte du texte du texte

### Installing

