# CPE2202-Algorithms-Assignment1
Data Structures and algorithms assignment
https://wokwi.com/projects/457464036023669761
📌 ESP32 Data Structures Implementation
📖 Overview

This project demonstrates the implementation and analysis of fundamental data structures on the ESP32 using the Arduino framework in Wokwi.

The goal was to design, test, and compare multiple data structures in an embedded systems context, focusing on memory behavior, efficiency, and correctness.

🧠 Implemented Components
1️⃣ Array vs Linked List (Playlist Manager)

Implemented a static array-based playlist

Implemented a dynamic linked list playlist

Supported operations:

Add song

Remove song

Display playlist

Implemented proper memory cleanup for linked list

Compared static vs dynamic memory behavior

Key Observations

Arrays use fixed memory and provide fast indexing.

Linked lists use dynamic allocation and require careful memory management.

Failing to delete nodes causes memory leaks on embedded systems.

2️⃣ Memory Leak Analysis

Demonstrated proper stack allocation instead of dynamic heap allocation.

Used ESP.getFreeHeap() to monitor memory usage.

Verified that repeated operations did not reduce available heap memory.

Prevented fragmentation and long-term instability.

Key Observations

Heap memory must remain stable across repeated operations.

Avoid unnecessary new in embedded systems.

Stack allocation is safer for repeated short-lived data.

3️⃣ Circular Buffer (Fixed-Size Queue)

Implemented circular buffer using a fixed-size array.

Used modular arithmetic for wrap-around logic.

Automatically overwrites oldest data when full.

No dynamic memory used.

Key Observations

Insertion complexity: O(1)

No shifting required

Efficient for real-time logging systems

Ideal for sensor data buffering

4️⃣ Stack (Undo Functionality)

Implemented array-based stack (LIFO).

Supported:

Push

Pop

Display

Implemented overflow and underflow protection.

Key Observations

Push and Pop are O(1)

Stack correctly removes most recently added item first

Proper boundary checks prevent crashes

⚙️ Technologies Used

ESP32 (Wokwi simulation)

Arduino Framework (C++)

GitHub for version control  
🔍 Key Learning Outcomes

Understanding memory management on embedded systems

Preventing memory leaks

Implementing modular indexing

Comparing static vs dynamic allocation

Applying Big-O analysis in practical embedded scenarios

🚀 Conclusion

This project demonstrates the practical application of fundamental data structures in constrained embedded environments. Emphasis was placed on memory efficiency, safety, and performance trade-offs between static and dynamic allocation.
