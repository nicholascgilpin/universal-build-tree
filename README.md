# universal-build-tree
An open graph database describing the minimum resources and processes needed to build anything. 

## Goal
To provide a quick human and machine readable overview of resources and actions needed to build anything. The resulting action graph output can be used for supply chain analysis, project planning, game design, or quick resource need estimates. 

### What's not a goal?
The project is only interested in the relationships between nodes. Collecting information about resources and processes is not a goal. Users are expected to use the application as a list of pointers to additional data. The only reason for the included descriptions are for identifying what other data needs to be gathered. 

## Planned Features
- Directed Acyclic Graph Data in GEXF format
- Python notebook for editing, viewing, and exporting by coders
- Web GUI for editing, viewing, and exporting the data by regular people

## Example Output
### Human Readable Mode

How to make: Sugar

Time: Unknown (-1)

Ingredients:
  - 6 Carbon Dioxide Molecules
  - 6 Water Molecules
  - Light

Instructions:
  1. Do photosythesis on: Carbon Dioxide Molecules, Water Molecules, Light

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

## Ontology format
- Nodes have two types
  - Type: Resources Nodes
    - A string name
    - A list of aliases
    - A unique ID
    - A list of resources needed to fabricate a product
    - A list of the ratios of each resource needed
  - Type: Process Nodes
    - A string name
    - A list of aliases
    - A unique ID
    - A list of inputs
    - A list of ouputs
    - An ordered list of conversion steps to transform the inputs into the outputs
    - An integer count of seconds estimated for the task to complete
- Relationships have one type
  - Type: Dependency relationship
    - Directed edge connecting resource nodes to process nodes

