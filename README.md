# Kempelen Consensus Approach

![](mechanical_turk.jpeg)

## Miami Network Abstract
-----------

>A Summary Overview of Deep Learning and Neural Network Techniques to Influence Blockchain Security, Speed, and Control
-----------

## Overview
-----------
The ***Kempelen Consensus Engine*** (_PoSA-K_) is an upgrade over the existing Parlia consensus engine deployed by the BNB chain. While keeping the lightweight, common-trust based staked authority proof validating consensus, it addresses the issues that may arise from the human decided authority assignment. For example, a shutdown of a chain utilizing Parlia can happen if the authority assigner team, and the existing validator nodes are removed. The Kempelen consensus engine proposes a distributed, intelligent authority assignment process that eliminates most of the human involvement in the upkeep of the chain.


## Goals
-----------
1. Deploying a consensus algorithm that assigns authority to a varying number of validators without any key kept on existing signers.
2. Implementing an automated, intelligent statistical zk key checker that can consistently provide an NP-complete query to prospecting validators in a fully deterministic environment (blockchain).
3. Implementing a routing protocol that fetches the node that suits the user’s transaction patterns, allowing to batch the transaction types on the same node, for optimized processing on the validator machines.

## Features Summary
1. Routing between nodes for optimization
   1. Each node has a running score of transaction processing time by transaction type.
   2. Transactions are batched by type onto each block.
   3. These batches are pushed into the highest scored nodes.
2. Hamiltonian Statistical Zero Knowledge Automated Authority Assignment
   1. Blockchain state is kept as a continuous hamiltonian graph.
   2. Node 1 is an existing validator, Node 2 is a prospector.
   3. A set of transactions in _P_ are assigned (by a learning model) as nodes on a hamiltonian cycle _G_
   4. Node 1 generates a matrix _H_ isomorphic to _G_
   5. Depending on which authority pool the prospector is trying to join two separate queries are formed. Node 2 will either have to prove that it knows the isomorphism between _H_ and _G_ by demonstration, or it will need to provide the number of vertices of _H_.
   6. Node 1 has this hamiltonian cycle (received by the AI key generation node, with varying difficulty depending on the blockchain’s needs).
   7. The computing time for both of these operations through the means of brute force is too high, however, if Node 2 can provide a passing answer to either question, it will be granted signing authority over a fixed amount of blocks, then this process is repeated.
   8. Therefore removing the need for a password to be kept on a centralized database, and suited for a decentralized network.
3. Routing protocol is observed and upgraded by a distributed intelligent agent that can track the transactor’s (sender wallet) tx pattern, and allows a faster indexing to which transaction block the incoming tx belongs.
