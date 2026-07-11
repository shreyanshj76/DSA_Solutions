# Program to perform BFS Traversal of a Graph

Solution :
```c++
#include <iostream>
#include <vector>
#include <queue>
using namespace std;

// Function to perform BFS traversal
void BFS(int start, vector<vector<int>> &adj, int V) {
    vector<bool> visited(V, false); // Keeps track of visited vertices
    queue<int> q;

    // Start from the given vertex
    visited[start] = true;
    q.push(start);

    while (!q.empty()) {
        int current = q.front();
        q.pop();

        cout << current << " ";

        // Visit all adjacent vertices
        for (int neighbor : adj[current]) {
            if (!visited[neighbor]) {
                visited[neighbor] = true;
                q.push(neighbor);
            }
        }
    }
}

int main() {
    int V = 6; // Number of vertices

    // Adjacency List
    vector<vector<int>> adj(V);

    // Adding edges
    adj[0].push_back(1);
    adj[0].push_back(2);
    adj[1].push_back(3);
    adj[1].push_back(4);
    adj[2].push_back(5);

    cout << "BFS Traversal: ";
    BFS(0, adj, V);

    return 0;
}
```