# Temporal-Matching on link streams

## What is it about?

A link-stream is a sequence of pairs of the form (t,{u,v}), where t ∈ N represents a time instant and u ̸= v.
Given an integer γ and a link-stream L, the γ-link-stream of L is the set of temporally consecutive edges defined as {(t′, {u, v}) | t′ ∈  t, t + γ − 1 }, the sequence of all the γ-edges between vertices u and v, starting at time t.

The maximum temporal matching of a γ-link-stream is a maximum sized subset of its γ-edges, such that there is no pair of y-edges that "overlap".
Calculating a maximum temporal matching is NP-hard, we introduce a way to compute a 2-approx with a greedy algorithm, and to compute a quadratic kernel in polynomial time.

### An example of a link-stream

A link-stream L can be                The 2-link-stream resulting               A maximum temporal matching
represented as a list                   from L with γ = 2

        0 1 0                                   0 1 0                                   0 1 0
        0 2 0                                   0 2 0                                   
        0 3 0                                   0 3 0                                   
        1 2 0                                   1 2 0                                   
        1 3 0                                   1 3 0                                   
        2 3 0                                   2 3 0                                   2 3 0                              
        0 1 1                                   0 1 1                                   
        0 3 1                                   0 3 1                                   
        1 2 1                                                                          
        1 3 1                                   1 3 1
        2 3 1                                   2 3 1                                   
        0 1 2                                   
        0 2 2                                   
        0 3 2                                   
        1 3 2                                   
        2 3 2                                   


![alt image_chat_local](/chat.jpeg)

### Section 1-b

Du texte du texte du texte

```
Voici un autre exemple
```

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

