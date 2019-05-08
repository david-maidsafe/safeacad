# Node Ageing

## Summary
An autonomous and decentralised node reputation system that ranks nodes based on their age. Nodes that have been good citizens of the Network (have good bandwidth, storage and are always online) will have a higher age (reputation) than nodes that have not proven to be as useful.
The Network incentivises good behaviour via an incentivisation approach that is rooted in Game Theory.  A nodes ability to earn is directly related to its age e.g. a well aged node will earn more for equivalent work than a node with a younger age.  If you misbehave you lose trust and lose the incentive.  

Node Ageing helps to mitigate against Sybil attacks (the attacker subverts the reputation system of a peer-to-peer network by creating a large number of pseudonymous identities and uses them to gain a disproportionately large influence) by making it more time consuming/expensive to target specific network sections by diluting the influence of byzantine nodes across the Network.

## Status
This feature is currently in planning phase, and will be implemented as part of the Fleming release.

## How it works
A node’s age increases every time it is relocated.  The age at the point of relocation is arbitrarily picked in time.  In the network, trust increases exponentially with age. A node with age 2 ^4 is twice as trustworthy as one with the age 2 ^3.

Only nodes that are considered Elders take part in Parsec voting as they are the oldest and most trusted nodes in the section.  The top X number of nodes within the section gain the status of Elder and as the network will be constantly moving, there is not a specific age or threshold to gain Elder status. - just whichever nodes are the oldest in the Section at that point in time.  However, Nodes may lose Elder status during Churn.  Adults are any nodes that are not Elders. Infants are nodes that have just joined the Network.

The lower a nodes age the more frequently it is relocated .e.g.  A node with age 2 ^4 will get relocated before a node with age 2 ^5 as it has been in the section for less (half) time.  

Older nodes are relocated less frequently than younger nodes as older nodes are less likely to behave badly, and the consequences would be more costly for them. I e “The more I trust someone (exponentially), I can keep them in the section longer”.  

The greater the nodes trust level .i.e. age the longer they can stay within a section.  This gives a node a greater amount of time to validate data and be ready if asked for the data thus increasing their ability to earn safecoin. Relocations are resource intensive as nodes validate new areas of responsibility within the Section and there is a large amount of traffic.

As described, only Elders take part in Parsec voting, and a Section Quorum is reached based on the majority of the Elders age, but the votes must also come from a majority number of Elders. This avoids trusting an individual node, even one with very high age/reputation.

As we have learned elsewhere in this document, It is not possible to pick your own Section, as to do so would potentially enable adversaries to influence consensus thereby controlling the Section and possibly the Network. When a node does bootstrap initially to a Section chosen by the Network, it is quickly relocated to another section. A new node can only join a section when there are no infants (new nodes) in that Section.

Node reset (going offline) leads to nodes halving their node age therefore you are incentivised to stay online. Additionally, by punishing network resets it reduces the risk of malicious targeting. Targeting can lead to gaining control and stall consensus

The Network’s assessment of a node’s usefulness will continue to adapt over time as it matures.

- In the existing Alpha 2 Network, a node is assessed via a process of Resource Proof, which is essentially a spot check that takes place only when that node is joining the network. Resource Proof assesses bandwidth and CPU.  This mechanism is easy to manipulate as after the initial check a node could then behave maliciously.
- Within Fleming, the first milestone in which Node Ageing will be running, will require the implementation to be different to that described above. There will be no data on Fleming and therefore no no meaningful work against which to profile. Age will be emulated in Fleming based on Work Units, essentially, how many times a node has seen section membership change, with the Network continually spot checking every time a node ages. This will be harder to manipulate as the timing of these spot checks cannot be predetermined.

## Features
- Node Relocation
- Resource proof
- Incentivisation tactics

## Benefits
- Help mitigate against Sybil attacks
- When linked with a network currency, an incentive for ‘good behaviour’
