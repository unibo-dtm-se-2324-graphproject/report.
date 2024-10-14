```mermaid
graph TD;
    Frontend -->|Submit Equation| Backend;

    subgraph Frontend
        UI[User Interface] --> Input[Input Fields]
        UI --> Graph[Graph Display]
    end

    subgraph Backend
        StaticFiles[Express.js Server <br> Serves Static Files] --> GraphLogic[Graphing Logic]
        GraphLogic --> DataProcessing[Data Processing]
    end

    Backend -->|Serves HTML| Frontend