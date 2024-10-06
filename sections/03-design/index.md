---
title: Design
has_children: false
nav_order: 4
---

## Design

This chapter explains the strategies used to meet the requirements identified in the analysis

## Architecture

The architecture of the Graph Website is based on a client-server model, where the frontend and backend components are decoupled to allow for scalable and maintainable development. The frontend is built using HTML, CSS, and JavaScript. The backend is developed using Node.js with Express, responsible for processing user requests and serving the necessary static files. This architecture enables seamless communication between the client and server, ensuring quick response times and efficient data handling.



## Modelling

The application employs a modular approach, where each component of the system is designed to perform specific functions. The modeling focuses on the following key areas:

- Graphing Module: Handles the input of mathematical equations and the generation of their graphical representations. It uses a library like Plotly.js to render graphs based on user input.

- User Input Module: Manages user inputs for equations, X and Y ranges, and ensures that the data is validated before being processed. This module ensures a smooth user experience by providing immediate feedback for invalid entries.

- API Module: Exposes RESTful endpoints for the frontend to interact with the backend. This includes endpoints for serving the main page, returning static assets, and handling user-generated data.


## Interaction

User interaction with the Graph Website is designed to be intuitive and straightforward. Upon accessing the application, users are presented with a clean interface where they can input their equations. 

The interactive features include:

- Input fields for entering one or two equations.
- Controls for specifying the X and Y ranges for graph plotting.
- Buttons to submit equations and trigger graph generation.

As users interact with the application, the system provides immediate visual feedback, allowing them to see how changes in equations or ranges affect the graphs in real time. This responsive design enhances the user experience by facilitating an engaging learning process.

## Behaviour

The behavior of the application is governed by well-defined user actions and system responses. Key behaviors include:

- **Graph Generation**: When users submit equations, the application processes the inputs and generates the corresponding graphs. If users modify their equations or ranges, they must re-submit their inputs to refresh the graphs.

- **Error Handling**: The system incorporates validation checks for user inputs, displaying error messages when invalid equations are entered. This prevents users from experiencing crashes or undefined behavior.

- **Dynamic Updates**: The application updates the graphs dynamically without requiring page reloads, creating a seamless experience for users as they manipulate their inputs.

## Data-related aspects

The data handling within the Graph Website is minimal since the primary function is to visualize equations rather than store user data persistently. However, the application does involve the following data-related aspects:

- **User Input**: The application captures user input for equations and ranges, which are processed in real-time to generate graphs.

- **Graph Data**: Data representing the X and Y coordinates for the graphs is generated based on the mathematical equations provided by the users. This data is transient and is only held in memory during the session.

- **Stateless Design**: The application follows a stateless design approach, meaning it does not retain user data between sessions. Each interaction is independent, allowing users to start fresh without previous inputs affecting new graph generations.
