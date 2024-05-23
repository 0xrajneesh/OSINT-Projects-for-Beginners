# Project 3: Using Maltego for Graphical Link Analysis and Network Mapping

## Introduction

Maltego is a powerful OSINT and forensics tool for graphical link analysis and data mining. It helps visualize relationships between people, groups, websites, domains, networks, and more. This project will guide you through installing and using Maltego to create visualizations and analyze connections within data.

## Pre-requisites

- Basic understanding of OSINT
- Familiarity with graphical user interfaces (GUI)
- A system with Maltego installed (Community Edition or Commercial Edition)

## Lab Set-up and Tools

- **Maltego**: The primary tool for this project
- **Internet connection**: Required for fetching data from online sources

### Installation Steps

1. **Download Maltego**:
    - Go to the [Maltego website](https://www.maltego.com/) and download the appropriate version for your operating system.
    - Follow the installation instructions provided on the website.

2. **Launch Maltego**:
    - Open Maltego and create an account if you don't already have one.
    - Log in with your credentials.

## Exercises

### Exercise 1: Setting Up a New Graph

1. **Create a new graph**:
    - Open Maltego and click on "New" to create a new graph.
    **Expected Output**: A blank canvas ready for adding entities.

2. **Add a domain entity**:
    - Drag and drop the "Domain" entity from the palette onto the canvas.
    - Set the domain name to "example.com".
    **Expected Output**: The domain "example.com" appears on the canvas.

### Exercise 2: Performing Basic Transformations

1. **Run a transformation to discover DNS names**:
    - Right-click on the "example.com" domain entity.
    - Select "Run Transform" and choose "To DNS Name [DNS]".
    **Expected Output**: Additional entities representing DNS names associated with "example.com" are added to the graph.

2. **Run a transformation to find email addresses**:
    - Right-click on the "example.com" domain entity.
    - Select "Run Transform" and choose "To Email Addresses [From WHOIS Info]".
    **Expected Output**: Email address entities associated with the domain appear on the graph.

### Exercise 3: Mapping Relationships

1. **Add a person entity and connect to email addresses**:
    - Drag and drop the "Person" entity from the palette onto the canvas.
    - Name the person entity as "John Doe".
    - Link "John Doe" to one of the email addresses found in the previous step.
    **Expected Output**: The graph shows a connection between "John Doe" and the linked email address.

### Exercise 4: Using External Data Sources

1. **Run a transformation using an external data source**:
    - Right-click on the "example.com" domain entity.
    - Select "Run Transform" and choose "To Social Networks [LinkedIn, Twitter, Facebook]".
    **Expected Output**: Entities representing social network profiles associated with the domain are added to the graph.

### Exercise 5: Analyzing and Exporting the Graph

1. **Analyze the relationships and patterns**:
    - Examine the connections and relationships between entities on the graph.
    **Expected Output**: Insights into how entities are related and any patterns that emerge.

2. **Export the graph for reporting**:
    - Go to "File" and select "Export Graph".
    - Choose the format (e.g., PDF, CSV) and save the graph.
    **Expected Output**: A file containing the exported graph, ready for inclusion in reports or further analysis.

## Conclusion

In this project, you learned how to use Maltego for graphical link analysis and network mapping. You created a new graph, performed basic transformations to discover DNS names and email addresses, mapped relationships, used external data sources, and exported your graph for reporting. Maltego's visual approach to data analysis helps uncover hidden connections and patterns, making it a valuable tool for OSINT investigations.
