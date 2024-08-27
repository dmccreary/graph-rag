# LLM Prompts used in GraphRAG

## Entity Extraction Prompts

```
Please analyze the following text and extract the entities related to people,
organizations, locations, and events. For each entity, return the output in a
JSON format where each entity is represented as a node, and relationships
between entities are represented as edges. 
Ensure that the output follows this structure:

{
    "nodes": [
        {"id": "1", "label": "Person", "name": "John Doe"},
        {"id": "2", "label": "Organization", "name": "ACME Corp"},
        {"id": "3", "label": "Location", "name": "New York"},
        {"id": "4", "label": "Event", "name": "Annual Conference 2024"}
    ],
    "edges": [
        {"source": "1", "target": "2", "relationship": "works_at"},
        {"source": "1", "target": "3", "relationship": "lives_in"},
        {"source": "2", "target": "4", "relationship": "organizes"},
        {"source": "3", "target": "4", "relationship": "location_of"}
    ]
}

Please make sure to include appropriate relationships between the entities wherever applicable.  Avoid duplication of edges.


