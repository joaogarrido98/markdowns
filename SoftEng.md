# Software enginneering

> A quick guide through software engineering

## Use Cases

**Show the external vew of the system**.
Are scenario based technique in the UML which identify the actors in an interaction.
A task which the actor needs to perform.

- **Use** -> How you use the system
- **Case** -> An example
- **Actor** -> is a user if the system (Can be human or non-human)

The details of each use case should also be documented by use case description

##### Template

- ID
  - Short ID
- Name
  - Full Name
- Description
  - Full Description
- Pre-condition
  - What must be true before the use case can proceed
- Event flow
  - Flow of behavior that makes up this use case
- Post condition
  - What should be true if the use case successfully completes
- Includes
  - What other use cases are used
- Extensions
  - Optional behavior
- Triggers
  - What Makes this use case happen

**Example**

![Use Case](./softEng/usecase.JPG)

#### Actors

- Can be human
  - Customer
  - Player
  - Driver
- Can be non-human
  - Sensor
  - Payment Service
  - Geo location
  - Robotic arm

---

## Software Processes

---

#### What is a Process?

> Series of activities when providing a service.

**All process have the following characteristics:**

- It prescribes all of the **major activities**
- It uses resources and produces **intermediate and final products**
- It may include sub-processes and **has entry and exit criteria**
- The activities are **organized in a sequence**
- Constraints or controls may apply to activities (budget constraints, availability of resources)

**Software Processes**

> When the process involves the building of some product we refer to the process as a **life cycle**

Coherent sets of activities for software systems

- **Specifying**
- **Designing**
- **Implementing**
- **Testing**
- **Evolution**

#### Software Process Models

##### The Waterfall Model

Separate and distinct phases of specification and development.

![Waterfall Model](./softEng/waterfall.JPG)

**Problems**:

- Inflexible partitioning of the project into distinct stages making it difficult to respond to changing customer requirements.
- Describes a process of stepwise refinement based on hardware engineering models, widely used in military and aerospace industries.

##### Evolutionary Development

Specification and development are interleaved

![Evolutionary Model](./softEng/evolutionary.JPG)

Based upon the idea of developing an initial implementation, exposing it to the user and refining it based upon their feedback.

**Problems**:

- Lack of process visibility
- System are sometimes poorly structured

##### Agile and Scrum

Use widely in industry today.
Lightweight approach to software development

![Agile Model](./softEng/agile.JPG)

**Focused**:

- Code development as code activity
- Test driven development
- Often use pair programming
- Iterative development
- Self organised teams

**Scrum**

- Rather than deliver the system as a single delivery, **the development and delivery is broken down in to increments** (**Scrum Sprints**) with each increment delivering part of the required functionality.
- **User requirements are prioritised** and the highest priority requirements are included in early increments.
- **Once the development of an increment is started the requirements are frozen** though requirements for later increments can continue to evolve.

**Advantages**

- **Customer Value** can be delivered with each increment so system functionality is available earlier.
- **Early increments** act as a prototype to help elicit requirements for later increments.
- **Lower risk of overall project failure**.
- **The highest priority system services** tend to receive the most testing.

---

## Requirements

---

- **Functional** - What the system does.
- **Non-Functional** - Constrains on how the functions are provided

### Objectives

- To introduce the concepts of **user and system requirements**
- To describe **functional / non-functional requirements**
- To explain **two techniques** for describing system requirements

### Requirements engineering

Is the process of establishing :

- The **services** that the customer requires from a system
- The **constraints** under which it operates and is developed

**Why do we need requirements?**

To ensure software solution correctly solves a particular problem we must:

- Fully **understand** the problem that needs to be solved
- Discover **why** the problem needs to be solved
- Determine **who**

**What is a requirement?**

It may range from a **high-level abstract statement of a service** or of a **system constraint to be detailed mathematical** functional specification

### Types

- **User requirements**
- **System requirements**
- **Software specification**

#### Functional Requirements

> Statements of services the system should provide, how the system should react to particular inputs and how the system should behave in particular situations

**Example**

- All users will access the system using a user id and a password

#### Non-functional Requirements

> Constraints on the services or functions offered by the system such as timing constraints, constraints on the development process, standards.

Define system properties and constraints:

- Reliability
- Response time
- Storage requirements.

Process requirements may also be specified, mandating a particular CASE system, programming language or development method.

**Classifications**

- Product requirements
  - Requirements which specify that the delivered product must behave in a particular way.
- Organisational requirements
  - Requirements which are ......
- External requirements
  - Requirements which arise from factors which are external to the system and its development process e.g. interoperability requirements, legislative requirements

Example:

- All encryption should use the advanced encryption standard
- The system development process and deliverable documents shall conform to the process
- The system shall not disclose any personal information about customers apart from their name.
- The system shall not disclose any personal information about customers apart from their name and reference number to the operators of the system
- The system should respond to a user???s request for information in less than 0.1 seconds during ???peak-time??? and 0.01 seconds during ???normal time???.

##### Domain Requirements

> Requirements that come from the application domain of the system and that reflect characteristics of the domain.

**Requirements Imprecision**

Problems arise when requirements are not precisely stated.

**Requirements Completeness and Consistency**

They should include description of all facilities required and there should be no contradictions in the description.

#### Requirements Measures

![Requirements](./softEng/requirements.JPG)
