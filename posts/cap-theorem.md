---
title : "CAP Theorem"
created : "2021-02-28T01:43:00+05:30"
updated : "2021-02-28T01:43:00+05:30"
categories : ["software-engineering"]
tags : ["github"]
summary : "Detail guide on cap theorem"
---

<iframe
  width="560"
  height="315"
  src="https://www.youtube-nocookie.com/embed/taArwdC6b7w"
  frameborder="0"
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
  allowfullscreen></iframe>

Consistency - Availability - Partition Tolerance

## Partition Tolerance
If one node fails, other nodes would continue to operate.

## Availability
Data should be avaiable in different nodes. It means data should be replicated across nodes. If one node goes down then the data of that node should be available in other nodes also.

## Consistency
Data should be upto date in every node.

Let me tell you why it is not possible to Consistency and Availability to coexist. Lets assume we write some data to a node A. When the node A is replicating the data to other nodes for the sake of availability then at the same time user reads the data from a different node in which the data has not been replicated yet. But according to consistency it is wrong.




