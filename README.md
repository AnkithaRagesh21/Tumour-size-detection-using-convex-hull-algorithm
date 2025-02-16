# Tumour-size-detection-using-convex-hull-algorithm
The Convex Hull algorithm is a computational geometry algorithm used to find the smallest convex polygon that contains all the given points in a set. In simpler terms, it helps identify the outer boundary of a set of points, forming a convex shape.
let's break down the code function by function:

1. struct Point: Defines a structure to represent a point in 2D space. It contains two integers, x and y, representing the coordinates of the point.

2. struct Patient: Defines a structure to represent a patient. It contains:
   - A character array name to store the patient's name.
   - An integer age to store the patient's age.
   - Two pointers hist and loc to dynamically allocated memory, intended to store the patient's medical history and tumor location respectively.

3. void inputPatientData(struct Patient *patient): This function takes a pointer to a Patient structure as input and prompts the user to input various details about the patient, such as name, age, medical history, and tumor location. It dynamically allocates memory for the medical history and tumor location using malloc().

4. int orientation(struct Point p, struct Point q, struct Point r): This function calculates the orientation of three points p, q, and r using the cross product method. It returns:
   - 0 if the points are collinear.
   - 1 if they are in clockwise order.
   - 2 if they are in counterclockwise order.

5. void convexHull(struct Point points[], int n): This function calculates the convex hull of a set of points using the Graham Scan algorithm. It takes an array of Point structures and the number of points n as input. It finds the points forming the convex hull and prints them along with the area covered by the convex hull.

6. void freePatientData(struct Patient *patient): This function frees the dynamically allocated memory for the medical history and tumor location of a patient using free().

7. int main(): The main function of the program. It:
   - Declares a Patient structure and calls inputPatientData() to input patient details.
   - Asks the user for the number of tumor coordinates and then inputs those coordinates.
   - Calls convexHull() to calculate the convex hull of the tumor coordinates.
   - Frees dynamically allocated memory using freePatientData().
   - Returns 0 to indicate successful execution.

Overall, the program allows the user to input patient details and tumor coordinates, calculates the convex hull of the tumor, and prints the boundary points and the area covered by the convex hull. Finally, it frees dynamically allocated memory to prevent memory leaks.
