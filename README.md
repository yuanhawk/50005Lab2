# 50005Lab2
Complexity of Banker's Algorithm
O(MN^2)

M ~ Number of Resources
N ~ Number of Processes (Customers)

When designing the safety algorithm, processes are skipped when the need > work as seen in ```tempNeed[i][j] < work[j]```. If need < work, the work adds the allocation as seen in ```work[j] += tempAllocation[i][j];```.

Since the number of processes are iterated and checked multiple times in a while loop, complexity is N^2. And when the need < work, the number of resources is accessed once and used to increment the work array. As such the complexity is M. In total the complexity is O(M) * O(N^2) = O(MN^2).
