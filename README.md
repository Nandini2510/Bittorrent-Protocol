# P2P-file-sharing

## Computer Networks - Project
Group Members: Nandani Yadav, Shaanya Singh, Shashi Shirupa 


## Project details
    * Implementation of a P2P file-sharing software similar to BitTorrent.
    * Establishing connection using TCP, which is a reliable transport protocol.

## Protocol Description
The protocol is structured with an initial handshake, succeeded by an uninterrupted flow of messages that are prefixed with their respective lengths. When two peers establish a connection, they exchange handshake messages before proceeding to send any other types of messages.

## Implementation
    Initializing the peer process: 
        * Create both config files - Common.cfg & PeerInfo.cfg
        * Each peer accesses the config file that includes information about the file to be distributed, its size, intervals for   choking and unchoking, and the count of preferred neighbors.
        * The PeerInfo file indicates a peer's file completion status, marked as either 0 (incomplete) or 1 (complete). When a peer successfully obtains the entire file, the PeerInfo.cfg file is updated with a "1" for that respective peer. The initial peer, being the first to launch, solely listens on the port specified in the PeerInfo file since there are no other peers to connect with at that point.

## Output
![Alt text](/CN-ss.png?raw=true "Optional Title")
