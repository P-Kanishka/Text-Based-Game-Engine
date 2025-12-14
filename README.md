# 🎮 C# Text-Based Game Engine

**📅 Project Date:** 2021
**🛠️ Tech Stack:** C#, Unity 3D, .NET, OOP
**📂 Status:** Archived 

### 📖 Overview
This project is a modular **Text-Based RPG Engine** built to explore advanced **Object-Oriented Programming (OOP)** patterns in game development. Unlike standard Unity games that rely on physics, this engine relies on string parsing, state management, and data structures.

It was designed to decouple the *Game Logic* from the *Content*, allowing designers to create new rooms and items using `ScriptableObjects` without writing code.

### 🏗️ Software Architecture
The system uses a strict **MVC (Model-View-Controller)** inspired pattern to handle text input and state changes:

* **[GameController.cs](./GameController.cs):** The central manager that orchestrates the `ActionLog`, parses input, and updates the UI.
* **[Room.cs](./Room.cs):** A data structure defining nodes in the game graph, containing descriptions and connections.
* **[RoomNavigation.cs](./RoomNavigation.cs):** Handles the graph traversal logic when moving between rooms.
* **[TextInput.cs](./TextInput.cs):** Tokenizes user commands (e.g., "Go North") and maps them to executable actions.

### 🧩 Key Systems Implemented
* **Dictionary-Based Parsing:** Implemented O(1) lookup efficiency for commands by mapping verbs ("Take", "Use") to `InputActions` using `Dictionary<string, Action>`.
* **ScriptableObject Architecture:** Used for `Rooms`, `Items`, and `Actions` to ensure a data-driven design where game data is separate from logic.
* **State Management:** Tracks inventory (`nounsInInventory`) and room states persistently.

### 📸 Architecture Diagrams
*(See the `/diagrams` folder for full UML)*
![Class Diagram](./diagrams/Class%20Diagram2.jpg)

### 📄 Documentation
The full engineering report, including detailed UML Class Diagrams and State Machines, is available here:
[View Design Document PDF](./Text-Based-Game-Engine.pdf)
