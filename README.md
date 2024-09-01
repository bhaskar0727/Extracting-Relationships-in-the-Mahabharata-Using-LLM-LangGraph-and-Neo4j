# Extracting-Relationships-in-the-Mahabharata-Using-LLM-LangGraph-and-Neo4j



## Project Overview

This project delves into the intricate relationships within the epic Mahabharata using advanced AI technologies, including a Large Language Model (LLM), LangChain, and Neo4j. The objective was to process the
Mahabharata text, extract relationships and entities, and visualize these connections within a Neo4j graph database.

## Steps Involved

### 1. Installation of Dependencies
To set up the project, I installed the following dependencies:

- **LangChain**: Used to manage the LLM and text processing.
- **LLMGraphTransformer** from `langchain_experimental.graph_transformers`: Utilized to transform text into graph structures.
- **PyPDF2**: Employed for reading and processing the Mahabharata PDF file.
- **LangChain Groq**: Used to integrate and interact with the specific LLM model.
- **Py2neo**: Provided the interface for connecting with and managing the Neo4j graph database.

### 2. Creation of LLM Model
I instantiated a custom LLM using the `ChatGroq` class, adjusting various parameters to control the randomness, token limit, and diversity of the generated output. This model was pivotal in understanding and
processing the complex text of the Mahabharata.

### 3. PDF Processing
Given the large size of the Mahabharata PDF, it was necessary to split the document into smaller, more manageable chunks. This step was crucial because the LLM cannot process large files in one go. 
These chunks were then converted into LangChain-compatible `Document` objects.

### 4. Conversion to Graph Documents
The document chunks were processed using the LLMGraphTransformer, which extracted relationships and entities from the text. These extracted relationships were then saved in a dedicated output folder. 
This allows for reusability, so the model doesn't need to reprocess the entire text in future analyses.

### 5. Setting Up Neo4j
I set up a Neo4j database to store and visualize the relationships and entities extracted by the LLMGraphTransformer. This graph database serves as the backbone for exploring the complex web of connections
within the Mahabharata.

### 6. Connecting and Populating Neo4j
Using the `py2neo` library, I connected to the Neo4j database and created nodes and relationships based on the extracted data. The relationships were parsed from the graph documents and added to the database,
effectively building a comprehensive graph structure representing the Mahabharata's intricate relationships.

### 7. Visualization in Neo4j
Finally, the relationships and nodes were visualized using the Neo4j workspace. This step provided an interactive and insightful way to explore the complex network of connections within the Mahabharata.

---

## Future Work

- **Optimization**: Explore more efficient ways to handle large files and optimize the process for even larger datasets.
- **Advanced Visualizations**: Integrate the Neo4j database with other visualization tools to provide richer insights.
- **Model Fine-Tuning**: Further fine-tune the LLM on specific sections or themes within the Mahabharata for even more accurate relationship extraction.

## How to Run

1. Clone the repository.
2. Install the required dependencies.
3. Add your Groq API key.
4. Run the script to process the PDF and extract relationships.
5. Start your Neo4j database and run the Python script to populate it with nodes and relationships.

This README provides a comprehensive overview of the project and the steps involved. Feel free to expand upon it as needed!
