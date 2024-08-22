# Graph RAG Glossary

#### Community Detection

Community detection is the process of identifying groups of nodes within a network that are more densely connected to each other than to the rest of the network. This technique is used to reveal the modular structure of networks, uncovering clusters or communities that share common properties or functions.

For example, in social network analysis, community detection can help identify groups of users who frequently interact with each other, such as friend circles or interest groups.

#### Document Chunking

Document chunking is the process of dividing a large document into smaller, manageable sections or chunks. This technique is commonly used in natural language processing to facilitate tasks such as information retrieval, summarization, or content analysis by processing these smaller chunks individually.

For example, in a question-answering system, document chunking enables the model to focus on specific sections of a document, improving accuracy and efficiency in finding relevant answers.

#### Complex Sequential Question Answering

**Abbreviation**: CSQA
Complex Sequential Question Answering refers to a task in natural language processing that involves answering a series of interrelated questions where the context or the answers to previous questions impact subsequent questions. This task requires handling complex dependencies and reasoning chains, often relying on structured knowledge bases or graphs to provide accurate and context-aware responses. In GraphRAG, CSQA tasks benefit from the ability to retrieve and reason over graph-structured data that captures these intricate relationships​(GraphRAG-Survey).#### Entity Extraction

Entity extraction in the GraphRAG process plays a critical role in identifying and linking entities mentioned in the input query to corresponding entities in a knowledge graph. This step is essential for effectively retrieving relevant information and establishing connections between the textual data and the structured graph data.

Entity extraction is often considered a pre-processing step in GraphRAG. It involves identifying key entities within the user's query and linking them to their corresponding nodes in the graph database. This ensures that the retrieval process can focus on the correct parts of the graph, thereby enhancing the relevance and accuracy of the retrieved information.

It is particularly crucial in the **Graph-Guided Retrieval** phase, where entities identified in the text are mapped to their graph representations. This mapping allows the retrieval algorithms to more accurately extract the relevant subgraphs, nodes, or paths that correspond to the query.

Entity Extraction** typically occurs at the beginning of the **Graph-Guided Retrieval** phase. After the graph-based indexing phase, where the graph is prepared and indexed for efficient querying, entity extraction takes place to identify which parts of the graph are relevant to the query. This step directly influences the subsequent retrieval processes, ensuring that the retrieval is focused and efficient.

Entity extraction is thus a foundational step in aligning the unstructured text query with the structured graph data, enabling the GraphRAG system to retrieve and generate more contextually relevant responses​(GraphRAG-Survey)​(GraphRAG-Survey).

#### GNN-based Retriever

GNN-based retrievers use Graph Neural Networks to understand and process graph structures. They encode graph data, score different retrieval granularities based on similarity to the query, and guide the retrieval process within GraphRAG. These retrievers are particularly adept at handling complex graph data structures​(GraphRAG-Survey).

#### Graph Neural Networks (GNN)

GNNs are a class of deep learning models designed to handle graph-structured data. They operate by aggregating information from a node's neighbors to generate node embeddings, which can then be used for various tasks, such as node classification or graph-based retrieval. In GraphRAG, GNNs are often employed to encode graph data and guide retrieval processes​(GraphRAG-Survey).

#### Graph Retrieval-Augmented Generation (GraphRAG)

A methodology that enhances Retrieval-Augmented Generation (RAG) by leveraging graph data structures. GraphRAG retrieves elements such as nodes, triples, paths, or subgraphs from a pre-constructed graph database, allowing for more precise and context-aware generation by considering the interconnections between texts​(GraphRAG-Survey).

#### Graph-Based Indexing

Graph-Based Indexing is a method for organizing and indexing graph data to optimize retrieval operations. This involves mapping node and edge properties, establishing pointers between connected nodes, and organizing the data to support efficient traversal and retrieval. It plays a crucial role in enhancing query efficiency in GraphRAG​(GraphRAG-Survey).

#### Graph-Enhanced Generation
**Abbreviation**: G-Generation<br/>

The phase in GraphRAG where meaningful outputs or responses are synthesized based on the retrieved graph data. This stage involves taking the query, retrieved graph elements, and an optional prompt as inputs to generate a contextually relevant and accurate response​(GraphRAG-Survey).

#### GraphRAG Step

The key steps in a GraphRAG process, as outlined in the Summary paper, are:

1. Graph-Based Indexing (G-Indexing)

This initial phase involves constructing or identifying a graph database that aligns with the downstream tasks. The indexing process typically includes mapping node and edge properties, establishing pointers between connected nodes, and organizing the data to support fast traversal and retrieval operations. The quality of this step directly impacts the efficiency and effectiveness of the retrieval process.

2. Graph-Guided Retrieval (G-Retrieval)

Following the indexing phase, the retrieval phase focuses on extracting relevant information from the graph database based on the user query. This involves selecting the most pertinent graph elements, such as entities, triplets, paths, or subgraphs, using retrieval algorithms. The goal is to find the graph elements that best match the query and support the next stage of generation.

3. Graph-Enhanced Generation (G-Generation)

In the final phase, the retrieved graph elements are used to generate meaningful responses or outputs. This stage involves taking the query, the retrieved graph elements, and an optional prompt as inputs for a generation model, which produces the final response. The process is enhanced by the structural and relational knowledge embedded in the graph data.

These steps outline the comprehensive workflow of GraphRAG, emphasizing the importance of each phase in achieving accurate, contextually relevant responses based on graph-structured data​(GraphRAG-Survey).

#### Hallucination

Hallucination in natural language processing refers to the generation of content by a model that is factually incorrect, nonsensical, or not supported by the input data. This occurs when the model produces information that appears coherent but is either fabricated or irrelevant to the context.

For example, a language model might hallucinate by generating a detailed but entirely fictitious historical event when asked about a specific time period.

#### Hybrid Granularities

Hybrid Granularities involve retrieving graph data at multiple levels of detail, such as nodes, triplets, paths, and subgraphs, to capture both fine-grained and broad contextual information. This approach enhances the relevance and comprehensiveness of the retrieved data, making it useful for complex queries within GraphRAG ​(GraphRAG-Survey).

#### ISO Definition

A term definition is considered to be consistent with ISO metadata registry guideline 11179 if it meets the following criteria:

1. Precise
2. Concise
3. Distinct
4. Non-circular
5. Unencumbered with business rules

#### Knowledge Base Question Answering
**Abbreviation**: KBQA<br/>

A task in natural language processing focused on answering user queries based on external knowledge bases. KBQA methods are typically categorized into Information Retrieval (IR)-based methods, which retrieve information from knowledge graphs, and Semantic Parsing (SP)-based methods, which generate logical forms to query knowledge bases​(GraphRAG-Survey).

#### Knowledge Merging

A post-retrieval enhancement strategy in GraphRAG that involves combining multiple pieces of retrieved information to provide a comprehensive view. This process assists in consolidating knowledge, improving the relevance and completeness of the final retrieved results​(GraphRAG-Survey).

#### Knowledge Pruning

A technique used after initial retrieval to refine and improve the quality of the retrieved information by removing redundant or less relevant data. It aims to ensure that the final results are highly pertinent to the user's query, enhancing the relevance of the information presented​(GraphRAG-Survey).

#### LM-based Retriever

LM-based retrievers leverage the natural language processing capabilities of language models to retrieve relevant graph data based on text queries. These models are particularly effective for interpreting and processing diverse queries in GraphRAG. They are used to generate reasoning paths and assist in retrieving the most relevant graph elements​(GraphRAG-Survey).

#### Language Models

**Abbreviation**: LMs<br/>
Language models (LMs) are advanced AI models designed to understand and generate human language. They are mainly classified into two types: discriminative models, like BERT and RoBERTa, which focus on tasks such as text classification, and generative models, like GPT-3 and GPT-4, which are used for tasks like machine translation and text generation​(GraphRAG-Survey).

#### Leiden Algorithm

The Leiden Algorithm is an iterative method used for community detection in large networks. It improves upon the Louvain algorithm by guaranteeing well-connected communities, reducing the likelihood of disconnected or fragmented clusters within the detected communities.

For example, the Leiden Algorithm is often applied in graph analysis to identify groups of nodes that are more densely connected internally, such as in social network analysis to find clusters of users with similar interests.

Leiden algorithm, are used to partition the graph into communities of nodes with stronger connections to one another than to other nodes in the graph. This helps in grouping closely related entities together

#### Non-parametric Retriever

Non-parametric retrievers are based on heuristic rules or traditional graph search algorithms. They do not rely on deep-learning models, making them efficient for retrieval tasks that require high speed. These methods typically involve pre-processing steps like entity linking and are used in GraphRAG for tasks like subgraph extraction​(GraphRAG-Survey).

#### Paths

Paths represent sequences of relationships between entities within a graph. In GraphRAG, retrieving paths enhances contextual understanding and reasoning capabilities by capturing complex relationships and dependencies​(GraphRAG-Survey).

#### Query Decomposition

A technique that breaks down the original user query into smaller, more specific sub-queries. Each sub-query focuses on a particular aspect of the original query, making it easier to retrieve pertinent information and reduce the complexity of language queries​(GraphRAG-Survey).

#### Query Expansion

A pre-processing technique used in query enhancement to improve search results by supplementing or refining the original query with additional relevant terms or concepts. It aims to capture lexical variations and expand the information content of the query​(GraphRAG-Survey).

#### Query-Focused Summarization
**Abbreviation**: QFS<br/>

A task in natural language processing where the goal is to generate a summary of a document or set of documents that is focused on a specific query. GraphRAG enhances QFS by retrieving relevant subgraphs that capture the broader context and interconnections within the graph structure​(GraphRAG-Survey).

#### Retrieval-Augmented Generation

**Abbreviation**: RAG
Retrieval-Augmented Generation is a methodology that integrates external knowledge retrieval with the generation process of language models. By dynamically querying a large text corpus, RAG enhances the contextual depth, factual accuracy, and relevance of the content generated by language models. It addresses challenges such as hallucinations, lack of domain-specific knowledge, and outdated information by incorporating relevant factual knowledge into the responses​(GraphRAG-Survey)​(GraphRAG-Survey).

#### Subgraphs

In GraphRAG, subgraphs refer to comprehensive subsets of a graph that encapsulate relational contexts within a larger structure. Retrieving subgraphs allows for capturing complex patterns, sequences, and dependencies, which are crucial for a deeper understanding of semantic connections in graph-based tasks​(GraphRAG-Survey).

#### Text-Attributed Graphs
**Abbreviation**: TAGs<br/>

A universal format for graph data used in GraphRAG, where nodes and edges are associated with textual attributes. TAGs can represent knowledge graphs and other graph structures, enabling the retrieval of complex relational knowledge for use in generation tasks​(GraphRAG-Survey).

#### Triplets

Triplets in graph databases consist of entities and their relationships, represented as subject-predicate-object tuples. This structured representation is used in GraphRAG to retrieve and understand relational data within a graph​(GraphRAG-Survey).


#### Vector Indexing

Vector Indexing involves converting graph data into vector representations to facilitate fast retrieval. This is particularly useful for entity linking and rapid query processing, where vector search algorithms like Locality Sensitive Hashing (LSH) are applied. It enables efficient searches and helps maintain structural information during retrieval​(GraphRAG-Survey).

