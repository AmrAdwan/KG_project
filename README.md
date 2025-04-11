# Knowledge Graphs and Semantic Technologies – Hybrid Intelligence Ontology Project

This repository contains all project materials for our **Knowledge Graphs and Semantic Technologies** course. It revolves around the Hybrid Intelligence (HI) ontology, which we extended, merged, and linked with external knowledge bases. The repository is organized into four main folders:

## Folder Structure

### `OriginalOntology`
This folder contains the **original Hybrid Intelligence (HI) ontology** provided to us at the start of the project. It serves as the baseline model before any modifications or enhancements were applied.

### `ExpandedOntology`
This folder includes the HI ontology **expanded based on 15 academic papers**. We extracted new concepts, classes, properties, individuals, and OWL axioms, integrating them into the ontology to reflect richer semantic structures. The ontology now includes source paper annotations and uses OWL features such as class restrictions and logical expressions.

### `MergedAndLinkedOntology`
This is the **final version** of our ontology. It combines:
- The original HI ontology  
- Our expanded version  
- Ontologies created by other students  
- **Links to external knowledge sources** including **DBpedia**, **Wikidata**, and the **Open Research Knowledge Graph (ORKG)**

This version is ideal for querying, integration, and analysis.

### `SPARQLQueries`
A text file containing **five SPARQL queries** used during our project to analyze and explore the ontology. Full documentation for each query is provided below.

---

## How to Use

You can use these ontology files by:

1. **Cloning or downloading the repository**.
2. Importing the desired `.ttl` (Turtle) file into tools such as:
   - [**Protégé**](https://protege.stanford.edu/)
   - [**GraphDB**](https://www.ontotext.com/products/graphdb/)
   - [**Triply**](https://triply.cc/)
   - Other RDF or OWL-compatible triple stores and reasoning engines.

---

## SPARQL Query Documentation

### **Query 1** – *Ontology Schema & Property Usage Summary*
- Retrieves instances, their classes, the properties they use, and corresponding range definitions.
- Filters out blank nodes and internal W3C namespace properties.
- Helps validate the ontology’s structure and expected value types.
- **Use case**: Validation, schema understanding, debugging.

### **Query 2** – *Paper-Based Contribution Analysis*
- Returns all instances, their classes, and the **source paper** they originated from (via `hi:sourcePaper`).
- Also counts how many other instances come from the same paper.
- **Use case**: Understand knowledge contribution density per source.

### **Query 3** – *Instance Distribution by Class*
- Counts the number of **non-blank instances per class**.
- Results are grouped and ordered by descending instance count.
- **Use case**: Analyze class population levels across the ontology.

### **Query 4** – *Richness of Class Attributes*
- Finds the **top 20 classes** with the most **distinct properties**.
- Helps identify semantically rich or central classes.
- **Use case**: Schema evaluation, class importance analysis.

### **Query 5** – *Most Frequently Used Properties*
- Returns the **top 50 properties** ordered by usage count.
- Optional labels improve readability.
- Filters out standard RDF/OWL properties.
- **Use case**: Data quality auditing, indexing, performance tuning.

---

## Import Instructions (GraphDB)

1. **Open GraphDB Workbench**.
2. Create or select a repository.
3. Navigate to **Import → RDF → Upload RDF files**.
4. Upload the desired `.ttl` file (e.g., `MergedAndLinked.ttl`).
5. Once imported, go to the **SPARQL tab**, paste any query from the `SPARQLQueries` folder, and click **Run**.

