# College of Computing Knowledge Ontology

**Semantic Modeling, Knowledge Graphs, and Logical Inference**

## Project Overview

This project involves designing a semantic ontology for the College of Computing at Umm Al-Qura University. The ontology organizes academic information into a structured knowledge model, defining entities, attributes, and relationships that can be interpreted by semantic web tools.

Using Protégé and OWL, the project explores how academic knowledge can be formally represented, validated through logical reasoning, and queried to retrieve meaningful information about the college's academic environment.

## Project Goals

- Represent the college's academic organization through a formal ontology.
- Establish semantic relationships among academic entities.
- Define class hierarchies, properties, and logical restrictions.
- Use automated reasoning to identify implicit relationships and classify entities.
- Explore structured knowledge retrieval through SPARQL.

## Ontology Structure

### 1. Classes and Subclasses

The ontology contains 10 primary classes representing key elements of an academic institution:

- College
- Department
- Program
- Course
- Person
- Student
- Faculty
- Committee
- Event
- Facility

The class hierarchy organizes related concepts through specialization. For example, Student and Faculty are represented as subclasses of Person, allowing them to inherit characteristics defined at the parent-class level.

### 2. Object Properties

Twelve object properties were defined to connect entities and describe their relationships.

Examples include:

- `hasDepartment` — connects a college with its departments.
- `offersProgram` — links departments to academic programs.
- `offersCourse` — associates programs or departments with courses.
- `enrolledIn` — represents student enrollment.
- `teaches` — connects faculty members with courses.
- `memberOf` — identifies committee membership.
- `participatesIn` — represents participation in events.
- `locatedIn` — describes location relationships.

Inverse and functional properties were also explored to express additional relationship semantics and logical constraints.

### 3. Data Properties

Seven data properties were used to represent descriptive information associated with ontology entities.

These attributes include names, email addresses, student identifiers, course codes, credit hours, website addresses, and event dates. Datatypes help distinguish textual information, numerical values, and other attribute values.

## Ontology Rules and Class Definitions

The ontology uses OWL logical constructs to express rules and restrictions on the modeled domain.

- **Disjoint classes:** Student and Faculty are defined as mutually exclusive classes.
- **Cardinality restrictions:** Constraints describe requirements such as the minimum number of programs offered by a department and the maximum number of courses associated with a student.
- **Equivalent class definitions:** ActiveStudent, PopularCourse, and DepartmentWithPrograms are defined through logical conditions that support automated classification.

These constructs demonstrate how an ontology can capture both the structure of a domain and rules governing its entities.

## Reasoning and Knowledge Inference

The HermiT reasoner was applied to examine the ontology's logical consistency and derive additional knowledge from its assertions and class definitions.

The reasoning tasks included:

- Classifying individuals according to their defined properties.
- Inferring relationships from declared inverse properties.
- Checking whether class definitions and restrictions are logically compatible.
- Identifying inconsistencies arising from conflicting assertions or constraints.

The project documentation reports a successful consistency check, demonstrating the use of automated reasoning to validate the ontology model.

## SPARQL-Based Knowledge Retrieval

Fourteen SPARQL queries were prepared to explore the information represented in the ontology.

The query set covers several academic information needs, including:

- Retrieving student and faculty details.
- Examining committee participation.
- Finding courses that satisfy credit-hour conditions.
- Exploring student participation and extracurricular activities.
- Listing events and their participants.
- Tracing relationships across departments, programs, and courses.
- Aggregating enrollment information and student activity.

The queries use SPARQL features such as `SELECT`, `FILTER`, `OPTIONAL`, `GROUP BY`, `COUNT`, `COUNT DISTINCT`, and `ORDER BY` to retrieve, filter, and summarize information.

## Implementation Summary

| Component | Specification |
|---|---|
| Ontology classes | 10 |
| Object properties | 12 |
| Data properties | 7 |
| Individuals | 25 |
| Defined classes | 3 |
| SPARQL queries | 14 |
| Ontology editor | Protégé |
| Reasoning engine | HermiT |
| Representation language | OWL |

## Technologies Used

- **Protégé:** Ontology modeling and editing.
- **OWL:** Formal representation of concepts and relationships.
- **HermiT:** Logical reasoning and consistency validation.
- **SPARQL:** Querying semantic data.
- **W3C Semantic Web Standards:** Ontology and query-language foundations.

## Potential Extensions

Further development could introduce additional academic concepts, model more complex institutional relationships, connect the ontology to external knowledge sources, and provide a graphical interface for querying academic information.

The ontology could also serve as a foundation for semantic search and knowledge-based applications in university information systems.

## Academic Information

**Course:** DS2203 – Knowledge Representation and Inference

**Department:** Data Science

**Institution:** Umm Al-Qura University

**Project Date:** June 2026
