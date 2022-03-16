# universal-build-tree
An open graph database describing the minimum resources and processes needed to build anything. 

## Purpose
To provide a quick human and machine readable overview of resources and actions needed to build anything. The overview can be used for project planning, game design, or quick resource need estimates. 

## Planned Features
- Directed Acyclic Graph Data in GEXF format
- Python notebook for editing, viewing, and exporting by coders
- Web GUI for editing, viewing, and exporting the data by regular people

## Ontology format
- Nodes have two types
  - Type: Resources Nodes
    - A string name
    - A unique ID
    - A list of resources needed to fabricate a product
    - A list of the ratios of each resource needed
  - Type: Process Nodes
    - A string name
    - A unique ID
    - A list of inputs
    - A list of ouputs
    - An ordered list of conversion steps to transform the inputs into the outputs
    - An integer count of seconds estimated for the task to complete
- Relationships have one type
  - Type: Dependency relationship
    - Directed edge connecting resource nodes to process nodes

## Roadmap 
1. Description [X]
2. Python Notebook
3. Empty DAG GEXF file
4. Add and delete functions
5. View functions
6. Data Validation functions
7. Import 100+ nodes from wiki data
8. Create web application placeholder
9. Create notebook notebook demo example
10. Launch and recruit volunteers
