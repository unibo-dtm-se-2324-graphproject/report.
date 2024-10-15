---
title: Design
has_children: false
nav_order: 4
---

**Architecture**

The Graph Website follows a Layered Architecture, which provides clear separation between the frontend and backend components, allowing for scalability, maintainability, and flexibility. This architecture is visually represented in the **Component Diagram**, which shows how the various layers interact with each other.

sections/03-design/diagrams/component_diagram.png

**Frontend**

The Frontend layer is responsible for managing user interactions and visualizing the results. Built using HTML, CSS, and JavaScript, the frontend offers users an intuitive interface to input equations and graph ranges. The GraphTool UI, as shown in the Component Diagram, directly interacts with external libraries like Math.js and Plotly.js to process the user inputs and render the graphs dynamically in the browser.

- GraphTool UI: Handles the main interface for users, including equation input and graph plotting.
- Equation Parser: Evaluates the mathematical equations input by the user.
- Graph Plotter: Uses Plotly.js to render graphical representations of the input equations.
  
The interaction between these components is depicted in the **Sequence Diagram**, which shows how user inputs flow through the system, starting from the user interface, to equation evaluation, and ending with graph rendering.

sections/03-design/diagrams/sequence_diagram.png

- Class Design

The **Class Diagram** represents the structure of the main components in the Graph Website. It shows how different classes interact to provide the core functionalities, such as handling user inputs, processing equations, and generating graphs.

- User Class: Represents the user interacting with the system, allowing them to input equations and ranges.
  
- GraphTool Class: This class manages the overall graphing process, including handling user inputs, parsing equations, and plotting the graphs.
  
- Equation Class: Handles the parsing and evaluation of user-inputted equations.
  
- Plotter Class: Responsible for rendering the graph based on the parsed equation and range.
  
- Range Class: Manages the input of the X and Y axis ranges for graph plotting.

sections/03-design/diagrams/class_diagram.png

This Class Diagram visually breaks down the modular structure of the system, making it easier to understand how each part contributes to the overall functionality.

**Backend**

Though currently minimal in the implementation, the Backend layer, as depicted in the Component Diagram, provides support for static file serving and processing potential requests. Built using Node.js and Express, the backend ensures smooth communication between the client and server when necessary. 

- API Module: Responsible for managing any server requests, although for now, the primary function is serving static assets.
  
The Component Diagram shows how the frontend communicates with this API module when required. Even though the backend’s role is minimal in the current version, this architectural layer lays the foundation for future scalability.

**Layered Architecture**

In this layered architecture:

- Presentation Layer (Frontend): Manages everything the user sees and interacts with, from the GraphTool UI to the dynamic graphing capabilities using Plotly.js.
  
- Business Logic Layer: Handles the logic behind processing equations and ranges. In the current implementation, most of this is handled in the frontend via JavaScript and Math.js.
- 
- Data Access Layer (Backend): The backend layer processes incoming requests and serves files but can be extended for more complex tasks.

This separation of concerns ensures that the system is modular and easy to maintain. As shown in the **State Diagram**, the frontend moves through several states—WaitingForInput, ProcessingGraph, and DisplayGraph—to ensure the smooth handling of user actions and graph generation.

sections/03-design/diagrams/state_diagram.png
