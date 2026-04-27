# OpenStreetsMap GPS For UIC Campus


This GPS application is designed for the UIC campus to provide the fastest route from point A to point B. Users can input a building name or address along with their current location to get the fastest route across campus.

## How It Works
- Map data is pulled from the OpenStreetMap API and parsed into a graph structure  
- Locations (like intersections/buildings) are represented as nodes, and walking paths are treated as edges with weighted distances
- The shortest path is computed using Dijkstra’s Algorithm with a priority queue (min-heap)  
- The algorithm explores nodes based on minimum added distance until the desired point is reached 

## Technical Details
- Implemented graph structures in C++ using adjacency lists
- Used priority queues to find shortest path computation  
- Designed modular components for:
  - Graph construction from map data  
  - Pathfinding logic  
  - Input parsing and validation  

## Frontend & Backend
- Backend server built in C++ to handle the overall routing logic  
- Frontend is built with JavaScript to show the physical route 
- Communication between frontend and backend is through the local server (localhost:3000)  

To run the application, first download the project files. 
Navigate to the project folder directory on the terminal and use:
  ```bash
make run_server
```
Open your browser to http://localhost:3000 and run the application.
