# Ex.No: 2  Implementation of Depth First Search
### DATE: 19/03/2024                                                                        
### REGISTER NUMBER : 212221060209 
### AIM: 
To write a python program to implement Depth first Search. 
### Algorithm:
1. Start the program
2. Create the graph by using adjacency list representation
3. Define a function dfs and take the set “visited” is empty 
4. Search start with initial node. Check the node is not visited then print the node.
5. For each neighbor node, recursively invoke the dfs search.
6. Call the dfs function by passing arguments visited, graph and starting node.
7. Stop the program.
### Program:
```
def dfs(graph, start, visited=None):
    if visited is None:
        visited = set()
    visited.add(start)
    print(start, end=' ')

    for neighbor in graph[start]:
        if neighbor not in visited:
            dfs(graph, neighbor, visited)

# Example usage:
graph = {
    'A': ['B', 'C'],
    'B': ['D', 'E'],
    'C': ['F'],
    'D': [],
    'E': ['F'],
    'F': []
}

print("DFS traversal:")
dfs(graph, 'A')
```
### Output:
![image](https://github.com/Prathipa2003/AI_Lab_2023-24/assets/162797752/702ff343-746b-4bf4-905f-d1b4e729247e)
### Result:
Thus the depth first search order was found sucessfully.
