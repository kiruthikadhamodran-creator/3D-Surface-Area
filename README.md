Problem Description

Given a 2D grid where each cell contains a height representing stacked cubes, calculate the total 3D surface area of the resulting shape.

Each cube has:

Top face
Bottom face
Four side faces

Only faces that are exposed to air contribute to the surface area.

Approach
For every cell with height h > 0:
Add 2 for the top and bottom faces.
Compare the current stack with its four neighbors:
Up
Down
Left
Right

For each direction, add the exposed area:

max(current_height - neighbor_height, 0)
Sum all exposed faces to get the total surface area.
Algorithm
Read the grid dimensions and heights.
Traverse each cell.
Add top and bottom faces.
Calculate exposed side faces using neighboring heights.
Output the total surface area.
Complexity
Time Complexity: O(H × W)
Space Complexity: O(1) (excluding input storage)
Example

Input:

1 1
1

Output:

6
