![attack1](@/assets/posts/byzantine-consensus-how-it-works/coordinated-uncoordinated-attack1.png)

The fast development of blockchain technology since 2008 has led to the need for better quality blockchain-based apps. This heavily poses significant difficulties to developing high performance blockchain protocols, because the performance of a blockchain network ultimately relies on the consensus mechanism selected. One of the major difficulties for blockchain technology, for a long time, has been the issue of how to improve throughput or, in other words, how to increase the pace of transactions. The only way to accomplish such improvement is to first identify where the bottlenecks exist.

## Consensus

Consensus is a traditional distributed systems issue, originally addressed in with both theoretical and practical interest.

Decentralized systems in which different actors have different incentives and can act on the information they have is inherently blockchain-based.
New transactions get broadcasted to the network, and nodes then have the option of including or ignoring the transaction based on whether or not they choose to keep their copy of the ledger up to date. When the majority of the actors within the network (actors make up the network) arrive at a single decision, consensus is obtained.
Overall system reliability is hard to achieve in distributed computing and multi-agent systems, even when there are faulty processes. In many cases, processes must first agree on a particular piece of data that is required for computation.
To put it another way, these procedures are known as consensus.

## Byzantine consensus

Byzantine consensus is a basic issue in distributed computing and encryption. It has been used to create failure tolerant systems such as distributed storage systems certificate authorities, fair peer-to-peer sharing , and more recently cryptocurrency. It has also been widely used as building pieces in cryptographic protocols such as safe multi-party computation.

## Evolution of Byzantine consensus (Byzantine Generals’ Problem)

The Byzantine Generals' Problem was designed in 1982 as a mathematical problem to show how a team of Byzantine generals may be unable to decide with their next move because of communication issues.

![attack2](@/assets/posts/byzantine-consensus-how-it-works/coordinated-uncoordinated-attack2.png)

In the study published, Leslie Lamport, Robert Shostak, and Marshall Pease of Microsoft Research there was a city besieged by multiple divisions of the Byzantine army and each division was led by a different commander. Communication between the generals was limited to the use of messengers. Having observed the adversary, they had to come up with a unified strategy. But, there is the possibility that a few of the generals may be in league with the enemies of the army, working to prevent the loyal generals from forming an accord. The generals had to determine when to launch an assault on the city, but a majority of their forces will have to join in simultaneously. In order to prevent the loyal generals from having their strategy jeopardised by a small number of traitors, the generals must implement an algorithm that guarantees that all loyal generals agree on a single plan of action, and that a small number of traitors can't cause the loyal generals to deviate from the agreed-upon strategy. According to the algorithm, the faithful generals will all perform what is expected of them, while the traitors may do anything they want. Loyal generals should agree on a realistic strategy, not simply reaching consensus.

Assume, as is done in this problem, that each general is equipped with his own army and that each of these various places is inhabited by separate groups. The generals must decide whether to launch an assault or withdraw. In other words, it doesn't matter whether they assault or withdraw, as long as all generals are in agreement.

Thus, the following conditions must be met:

- Each general must make a decision: to assault or to withdraw.
- The choice is irreversible once it is made.
- It is vital that all generals agree on the same decision and that they implement it in the same way.
Due to the fact that one general may only interact with another via communications, which are carried by a courier, communication difficulties arise. To solve the Byzantine Generals' Problem, a delay, destruction, or loss of the communications will occur.

A false message may also lead to the complete failure of the campaign.

Conceptually, each general is a blockchain network node, and nodes within the system must arrive at an agreement on the current state of the system. Reduced to another form of expression, in a distributed network, the majority of players must agree and follow the same procedure in order to prevent total failure.

To reach agreement in distributed systems with unreliable or dishonest nodes, at least ⅔ of the nodes in the network must be accurate and honest. the system is more vulnerable to failures and assaults if the majority of the network acts maliciously (such as the 51 percent attack).

## Types of Byzantine Failures

There are two different kinds of failures that are included under this term. Alternatively, arbitrary node failure is sometimes referred to as fail-stop failure. Node failures may be found below:

![agreement problems](@/assets/posts/byzantine-consensus-how-it-works/agreement-problems.png)

- Returning no result
- Respond with an inaccurate result
- Reply with something that is completely deceptive
- Don't just respond the same for every component of the system.

## Algorithms of consensus used in blockchains

A consensus algorithm is the method used to achieve agreement on a blockchain network. Proof of Work (PoW) and Proof of Stake (PoS) are the most often used implementations (PoS). Let's consider the situation of Bitcoin, as an example.The rules that are enforced by the Bitcoin protocol are also established via the Proof of Work consensus method (for instance, during the verification and validation of transactions).

The idea of Proof of Work is centuries old, but Satoshi Nakamoto created a modified version of it, specifically for use in Bitcoin, as a consensus method that also creates a Byzantine consensus system.
PoW has proved to be among the most secure and dependable implementations for blockchain networks owing to the mining process's high cost and cryptographic methods. That interpretation may be called "brilliant," given that the Proof of Work (PoW) consensus method created by Satoshi Nakamoto was specifically intended to deal with the Byzantine Generals' problems.

## Benefits of Byzantine Consensus

Byzantine consensus has these benefits:

- Reduced energy consumption: using Byzantine consensus, consensus may be achieved while avoiding complicated mathematical calculations (like in PoW).
- Transaction finality: The transactions are completed and agreed upon, and do not need further confirmations, as with Proof of Work in Bitcoin, where each individual miner validates all transactions before putting in a fresh block to the network.
- Low variation in reward: Since every node in the network is involved in handling the request from the client, all nodes may be motivated, which results in low reward variance.

## Setbacks of Byzantine Consensus
- With Byzantine consensus, communication overhead rises exponentially with every additional node in the network, thus Byzantine consensus consensus models are efficient only when the number of nodes in the distributed network is limited.

- Sybil attacks involve a single entity controlling many identities. The more nodes there are in the network, the more difficult it becomes to carry out sybil assaults. However, like with Byzantine consensus methods, the Byzantine consensus mechanism has scaling problems as well, which is why Byzantine consensus is used in conjunction with other techniques (s).
- Scaling: Byzantine consensus has a communication cost, thus it doesn't scale well. As the number of nodes in the network grows, so does the time needed to reply to a request.

## Summary

This fascinating Byzantine Generals' Problem ultimately produced Byzantine consensus algorithms, which are now used in many different contexts. Beyond the blockchain sector, Byzantine consensus systems have seen some limited use cases in other areas, including aviation, space, and nuclear power.

To ensure that all nodes get equal data, Byzantine consensus is implemented. The network's protocol is impenetrable even in the event of poor devices or assaults that target the network. Simpler terms to describe consensus consistency: All that is required is that two-thirds of the nodes be secure.

A solid network communication and consensus mechanism are necessary in every blockchain ecosystem. There are still a few remaining challenges in securing these systems, and the current consensus algorithms have yet to overcome some of those obstacles (such as scalability). However, despite this, both proof-of-work (PoW) and proof-of-stake (PoS) are valid as Byzantine consensus schemes, and this leads to wide-ranging innovation.

A blockchain is a decentralised ledger that, by definition, does not have a centralised authority. Bad actors have large economic incentives to attempt to corrupt these ledgers. Nonetheless, a solution to the Byzantine Generals' Problem, and therefore Byzantine consensus, is sorely required for blockchains.
Byzantine consensus doesn't exist, thus a peer may publish and transmit fraudulent transactions to defeat the blockchain's trustworthiness. Sadly, there is no authority to step in and clean up the mess.
The very important step in the development of Bitcoin was the introduction of the Proof-of-Work scheme, as explained in-depth by Satoshi Nakamoto.

If the right nodes in the network are in agreement about their values, Byzantine consensus may be obtained. In the event that no communication is received within a specified time limit, the assumption is that the message originated from a defective node. Furthermore, if the majority of nodes reply with a valid value, we may assign a default response.
