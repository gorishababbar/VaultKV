# Distributed Key Value Store using Raft Consensus Algorithm with Leader Lease

This project presents a Distributed Key-Value Store implemented using the Raft Consensus Algorithm with Leader Lease. Leveraging the reliability and fault tolerance offered by Raft, the system ensures consistent data replication and fault recovery across a distributed network of nodes. By integrating leader lease functionality, it enhances the time complexity of various operations.

Built by - Mohammad Aflah Khan, Shivaansh Mital & Nishaant Rastogi

## Getting Started

### Prerequisites

To run this implementation, you need:

- Python 3.x
- ZeroMQ library (`pyzmq`)

### Installation

1. Clone this repository to your local machine.
2. Install dependencies using `pip`:
   ```
   pip install -r requirements.txt
   ```

### Usage

1. Modify the `connections.json` file to specify the network topology and node addresses.
2. Run the Raft nodes:
   ```
   python raft_node.py --nodeId <node_id> [--restarting <True/False>]
   ```
   - `<node_id>`: Unique identifier for the Raft node.
   - `--restarting`: Optional flag to indicate whether the node is restarting after a crash.

Once run correctly the nodes will automatically timeout elect leaders and work. You can then run `client.py` to send requests to the nodes, kill nodes and restart them and do all other fancy things.

## Acknowledgments

- This implementation was developed as a course assignment in Distributed Systems course offered at IIITD.
- Resources consulted - 
    - https://raft.github.io/
    - https://en.wikipedia.org/wiki/Raft_(algorithm)
    - https://thesecretlivesofdata.com/raft/
    - https://www.yugabyte.com/tech/raft-consensus-algorithm/
