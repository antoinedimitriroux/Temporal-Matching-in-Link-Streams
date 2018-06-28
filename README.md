# Temporal-Matching in link-streams

## What is it about?
A link-stream is a sequence of pairs of the form (t,{u,v}), where t ∈ N represents a time instant and u ̸= v.
![alt complex-networks-example](./complex-networks-example.svg)
Given an integer γ and a link-stream L, the γ-link-stream of L is the set of temporally consecutive edges defined as {(t′, {u, v}) | t′ ∈  t, t + γ − 1 }, the sequence of all the edges between vertices u and v, starting at time t.

The maximum temporal matching of a γ-link-stream is a maximum sized subset of its edges, such that there is no pair of edges that "overlap".
Computing a maximum temporal matching is NP-hard, we introduce a way to compute a 2-approximation with a greedy algorithm, and to compute a quadratic kernel in polynomial time.

We developped a javascript application to generate different link-streams based on the [rollernet](http://www-rp.lip6.fr/rollernet/en/experience/experience.html) experiment, and to calculate the 2-approximation and the kernel. It is accessible here: [rollernet-like-tools](https://antoinedimitriroux.github.io/), src files are here https://github.com/antoinedimitriroux/temporal-matching-in-link-streams.io.

### An example of a link-stream
![alt simple-link-stream-example-txt](/simple-link-stream-example.png)
Here is a more fancy representation of these link-streams
![alt simple-link-stream-example-img](/simple-link-stream-horizontal-image.png)

### 2-approximation algorithm
A greedy algorithm can compute a 2-approximation of the maximum temporal matching of a γ-link-stream.

Let L be a link-stream with n edges and an integer γ, the γ-link-stream of L can be computed in O(n^2) in the worst case.
For each edge e in the original link stream, we look after (γ-1) consecutive edges after this one. If we suppose the original link stream edges are cleverly sorted, we can break much earlier in the loop and obtain linear complexity.

Then, given a γ-link-stream γL, the 2-approximation can be computed in O(n^2) in the worst case.
To do so, we iteratively build a subest of the edges in γL by taking e, any γ-edge in γL, adding it to the 2-approximation edges list, and removing every edges of γL that overlap with e. The loop goes on while γL is not empty.

### Kernelisation algorithm
To compute the kernelisation algorithm for the maximum temporal matching of a γ-link-stream γL, we suppose we already computed A, a 2-approximation of γL. Let K be the number of edges in A, and S the result of the kernelisation.

For every edge e in A, we look for at most (2K-1) edges in γL that overlap with e (including e), and add them to S. We obtain a quadratic kernel for the maximal temporal matching of γL.

Of course, we would like this kernel to contain the least edges possible.
We have two ways to do so:
-   since the kernel size depends on K, the 2-approximation size, we can randomly compute different 2-approximations, and chose the one with the least edges,
-   once we have computed/chosen a 2-approximation A, we have to chose (2K-1) edges in γL for the K edges in A. Since some edges in A can "share" some overlapping edges in γL, we can chose cleverly these (2K-1) * K edges such that the union of all these is as small as possible.
