# Degrees of Separation

This Python project is a tool designed to find the shortest path of degrees of separation between two actors in the film industry, using data from the IMDb database. The program determines the minimum number of steps required to link two actors through their co-starring roles in movies.

## Features

- Utilizes IMDb data to find connections between actors.
- Implements Breadth-First Search algorithm for finding the shortest path.
- Handles ambiguities in actor names by allowing the user to select from multiple options.
- Interactive command line interface for querying actor connections.

## How It Works

The program operates by loading data about actors and movies from provided CSV files. It then prompts the user to enter two actor names and computes the shortest path of movie connections between them.

### Data Structure

- `names`: A dictionary mapping actor names to their corresponding IMDb person IDs.
- `people`: A dictionary mapping person IDs to their respective details (name, birth year, movies).
- `movies`: A dictionary mapping movie IDs to their details (title, year, starring actors).

### Classes

- `Node`: Represents a node in the search tree, containing state, parent, and action information.
- `StackFrontier`: Implements a stack-based frontier for search (unused in the final implementation).
- `QueueFrontier`: Implements a queue-based frontier (BFS) for finding the shortest path.

## Usage

1. Clone the repository or download the source code.
2. Ensure that the IMDb data files (`people.csv`, `movies.csv`, `stars.csv`) are placed in a directory.
3. Run the script from the command line: `python degrees.py [data directory]`
4. Follow the on-screen prompts to enter actor names.

## Dependencies

- Python 3
- CSV module (included in standard Python distribution)

## Note

This project is for educational purposes and demonstrates basic principles of graph theory and search algorithms using real-world data.
