## Summary
The Ethereum blockchain, like other decentralized platforms, has seen a rise in phishing scams where malicious actors attempt to steal funds or sensitive information from users. Traditional phishing detection methods struggle with the diverse and evolving tactics used by attackers. This project explores the potential of graph-based methods to improve the accuracy of phishing detection by analyzing the structure of transaction networks.

## Dataset
The dataset used in this project includes transaction records from the Ethereum blockchain, featuring:

1600+ Verified Phishing Addresses: Collected from Etherscan.
Normal Addresses: Randomly selected to match the number of phishing addresses.
Transaction Records: Data includes transaction amounts, timestamps, and the network of interactions between addresses.
Methodology
We experimented with several graph-based models to classify nodes (addresses) as either phishing or non-phishing:
Node2Vec: Generates node embeddings based on random walks to capture the network structure.
Graph2Vec: Extends node embeddings to entire subgraphs for more context-aware classifications.
Graph Convolutional Networks (GCNs): Utilizes the graph structure directly for node classification by capturing local and global information.
GraphSAGE: An inductive model that generates node embeddings by aggregating features from local neighborhoods.
Trans2Vec: A method that combines biased random walks with transaction-specific features to learn node embeddings.
## Experimental Setup
Classifiers Used: Logistic Regression, SVM, Random Forest, k-Nearest Neighbor (KNN).
Evaluation Metrics: Accuracy, Precision, Recall, F1-Score.
Addressing Class Imbalance: Techniques like SMOTE and upsampling were used to manage the imbalance between phishing and non-phishing nodes.
## Results
GCN Model: Achieved the highest performance in identifying phishing nodes with balanced accuracy, precision, and recall.
Ego Graph Methods: Showed promise by focusing on local neighborhoods around each node.
Full-Graph Methods: Struggled with class imbalance, leading to lower performance in identifying phishing nodes.
## Conclusion
Graph-based methods, especially GCNs and ego-graph approaches, demonstrate significant potential in enhancing phishing detection on the Ethereum blockchain. The ability to capture complex transactional relationships makes these models particularly suited for this task.
