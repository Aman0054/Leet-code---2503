Approach
1️⃣ Sorting Queries 📌: First, we sort the queries in ascending order while keeping track of their original indices. This allows us to process smaller query values first.

2️⃣ Priority Queue (Min-Heap) ⏳: We use a min-heap to store grid cells in increasing order of value. This helps us efficiently retrieve the smallest unprocessed cell.

3️⃣ Breadth-First Expansion 🌍: Starting from the top-left corner (0,0) ⬆️, we expand to neighboring cells (left ⬅️, right ➡️, up ⬆️, down ⬇️) only if their values are not yet processed and are smaller than the current query threshold.

4️⃣ Processing Queries 📝: For each query, we pop elements from the priority queue while their values are smaller than the query. We count how many cells are processed and store this count as the answer for that query.

5️⃣ Returning Results ✅: Once all queries are processed, we return the result array with answers in the original query order.

⏳ Complexity
Time Complexity:

Sorting the queries takes (O(k \log k)) 📉.
Using a priority queue for processing grid cells results in (O(nm \log (nm))) ⏳ in the worst case.
Overall, the time complexity is (O(nm \log (nm) + k \log k)) ⚡.
Space Complexity:

We use extra space for storing visited cells ((O(nm)) 🏗️).
The priority queue can store up to (O(nm)) elements in the worst case.
The result array takes (O(k)) space.
The total space complexity is (O(nm + k)) 💾.
