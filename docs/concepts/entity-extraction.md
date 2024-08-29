# Entity Extraction

[Entity Extraction](../glossary.md#entity-extraction) is the process of identifying and categorizing key pieces of information (entities) from text, such as names of people, organizations, locations, dates, and other specific concepts. These entities are often represented by proper nouns or specific phrases that are crucial to understanding the text's meaning.

Entity extraction in the GraphRAG process plays a critical role in identifying and linking entities mentioned in the input query to corresponding entities in a knowledge graph. This step is essential for effectively retrieving relevant information and establishing connections between the textual data and the structured graph data.

Entity extraction is often considered a pre-processing step in GraphRAG. It involves identifying key entities within the user's query and linking them to their corresponding nodes in the graph database. This ensures that the retrieval process can focus on the correct parts of the graph, thereby enhancing the relevance and accuracy of the retrieved information.

It is particularly crucial in the **Graph-Guided Retrieval** phase, where entities identified in the text are mapped to their graph representations. This mapping allows the retrieval algorithms to more accurately extract the relevant subgraphs, nodes, or paths that correspond to the query.

Entity Extraction** typically occurs at the beginning of the **Graph-Guided Retrieval** phase. After the graph-based indexing phase, where the graph is prepared and indexed for efficient querying, entity extraction takes place to identify which parts of the graph are relevant to the query. This step directly influences the subsequent retrieval processes, ensuring that the retrieval is focused and efficient.

Entity extraction is thus a foundational step in aligning the unstructured text query with the structured graph data, enabling the GraphRAG system to retrieve and generate more contextually relevant responses​(GraphRAG-Survey)​(GraphRAG-Survey).

## Why Entity Extraction is Important in the GraphRAG Algorithm:

### Building Knowledge Graphs

Entity extraction is essential for constructing knowledge graphs, which are structured representations of information. By identifying entities, the GraphRAG algorithm can map these entities as nodes in the graph, forming the foundation for connecting and linking various pieces of information.

### Enhancing Information Retrieval

In the context of the GraphRAG (Graph Retrieval-Augmented Generation) algorithm, entity extraction allows for precise retrieval of relevant information from a knowledge graph. When a user query is mapped to specific entities, the algorithm can more effectively navigate the graph to find accurate and contextually relevant information.

#### Enabling Contextual Understanding:**

By extracting entities, the algorithm can understand the context of a query or document. This contextual understanding is critical in generating accurate and relevant responses, as the algorithm can link the query to the right nodes and paths in the graph.

### Improving Query Mapping and Response Generation:**

Entity extraction helps in accurately mapping user queries to the graph's structure. This mapping is crucial for the GraphRAG algorithm to generate responses that are informed by the specific entities and their relationships within the knowledge graph.

### Supporting Complex Relationships and Reasoning:**

GraphRAG leverages the connections between entities in the knowledge graph to perform reasoning tasks, such as inferring new information or understanding complex relationships. Accurate entity extraction ensures that the graph is populated with the right entities, allowing for more sophisticated reasoning and inference capabilities.

## Picking the Right Granularity of Entities

Every business application might have different requirements
for locating entities in a document.  A legal system might
only care about finding the names of parties in a contract
and the effective dates of the contract.  For these
applications only simple entity extraction rules that
find People, Organizations, Locations and Events (POLE) entities
might be needed.  This makes the entity extraction pipeline
fast and low cost.

Other applications want to understand more nuanced concepts in
a document such as overall tone, development of ideas, analysis
of assignments or commitments.  These tools need better granularity
of extracting both abstract concepts and the relationship between
these concepts.

In summary, **Entity Extraction** is a foundational step in the GraphRAG algorithm, enabling the creation of a rich, structured knowledge graph and facilitating accurate, context-aware retrieval and generation of information.