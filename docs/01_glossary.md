# Glossary

[A](#a) | [B](#b) | [C](#c) | [D](#d) | E | F | [G](#g) | [H](#h) | [I](#i) | J | K | L | [M](#m) | [N](#n) | O | [P](#p) | [Q](#q) | [R](#r) | [S](#s) | T | U | [V](#v) | W | [X](#x)  | Y  | Z

## A
###  ABFT
Asynchronous Byzantine Fault Tolerance
###  Accumulating Node
The node that collates the message and signatures before sending when the sending authority is multiple
###  Accumulation at Source
When proofs are accumulated at the source of a message rather than the destination
###  Ack
Acknowledgement, confirmation that a message has been received successfully
###  Appendable data
Ability to append information to an existing piece of data, you cannot change what already exists.
###  Authority
A label that is applied to any message that determines its ultimate destination
###  Autonomous
The ability for the network to manage data without human intervention
## B
###  Bootstrapping
A process to join the network.  Anything that joins the network has to go through the Bootstrapping process
###  Buffer
Nodes additional to the minimum group size that are required before a split can occur to reduce merges.
## C
###  Chain
Links that couple together identifiers (descriptors)
### Client
Individual computers
###  CRUST
**C**ommunications in **Rust**: It’s a generic networking library that essentially connects two nodes/peers/computers directly without an intermediate server
## D
###  Disjoint Section
A group of Vaults defined by their XOR address prefix
## G
###  Gossip Event
A Gossip Event is any piece of information that is sent across the Network using the Gossip protocol.
###  Group
8 Nodes with a close XOR address
## H
###  Hop
Hop is when you have to  travel through neighbouring Sections in the network to reach your destination.
## I
###  Invariant
A set of rules which enable the Network to maintain a stable state
###  Immutable data
A data type that cannot be changed, and whose location is determined by the hash of the data itself.
## M
###  Merge
Merges happen when there are too few nodes (below minimum group size) in a Section so the nodes ‘merge’ with another Section.  You can only merge with a sibling.   
###  Message
in this context it’s any network operation (gossiping messages, relay messages, new node joining, consensus)
## N
###  Neighbour
relations to sections determined by the Network Invariant . Neighbours are those sections which prefix differ by one bit, i.e the neighbour of ‘01’ is ‘11’ and ‘00’, ‘10’ is not a neighbour as you have to change both the ‘0’ and the ‘1’ (bits).  
###  Network Event
Nodes attempt to communicate ‘truths’ to each other on the network
###  Node
individual device on the network
###  Node age
an autonomous and decentralised node reputation system that ranks nodes based on their age.
## P
###  PARSEC
Protocol for Asynchronous, Reliable, Secure and Efficient Consensus
an algorithm that orders section votes.
###  Prefix
first numbers (bits) at the beginning of the XOR address
###  Proxy
Acts as an intermediary between the client and the network / single authority
## Q
###  Quorum
quorum is the minimum number needed to cast a vote before an action can take place
## R
###  Resource proof
CPU, reliability & bandwidth, features a new node needs to prove on a continuous basis
## S
###  Secure Message Relay
a way of validating the senders of messages (not the messages) across Disjoint Sections of the Network.
###  Section
is a subset of all the addresses on the network.
###  Section info
an object that has info on the section including prefix, version, members - public identity (public key and encryption key), previous hash, hash
###  Sharding
The process by which sections change size, the location of responsibility and often their Neighbours due to splits and merges.
###  Sibling
are a special case of neighbours, siblings prefixes differ by only 1 bit at the very last bit. In the example above 01 would be the sibling to 00. Siblings are of particular importance in the case of mergers
###  Split
split occurs in a section when the section gets too big and unbalanced.  
###  Swarm
the process by which one node in a Section shares a received message with every other node in that Section
## V
###  Vault

###  Vector
list
###  Version
the members of a section at a given point in time.
## X
###  XOR
Every node or piece of data in the Network has a XOR address, which is a 256-bit long identifier
