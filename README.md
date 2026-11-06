<div align="center">

# Internet Café Management System

**CPE 010 Final Project**

![Language](https://img.shields.io/badge/language-C++17-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![Type](https://img.shields.io/badge/type-console%20app-black?style=flat-square)
![Section](https://img.shields.io/badge/section-CPE--21S3-black?style=flat-square)
![Group](https://img.shields.io/badge/group-2-black?style=flat-square)

</div>

---

## Description

A C++ console program that handles the daily operations of an internet café: station availability, customer sessions, the waiting line, billing, and daily sales. It replaces the paper logbook and sales notebook with data structures and algorithms from the course.

| | |
|---|---|
| **Course Code** | CPE 010 |
| **Course Name** | Data Structures and Algorithms |
| **Section** | CPE-21S3, Group 2 |
| **Instructor** | Engr. Jimlord Quejado |
| **Term** | 1st Semester, SY 2026-2027 |

---

## Features

- Station board with free, in-use, and maintenance status
- Check in a customer, or seat a whole group together
- Preferred PC seating, with the nearest free PC found automatically
- Session tracking with pause and resume
- First-come, first-served waiting line
- Billing at PHP 20/hour (per minute) with a 10% member discount
- Member registration and lookup
- Transaction history with sorting, searching, and receipt printing
- Undo for maintenance status changes
- Daily sales summary
- Performance Lab for theoretical and measured time complexity

---

## Data Structures and Algorithms

| Used for | Structure / Algorithm | File |
|---|---|---|
| Stations | Array | `Stations.h` |
| Active sessions | Singly linked list | `SessionList.h` |
| Waiting line | Queue (linked list) | `WaitQueue.h` |
| Receipts to print | Queue (circular array) | `ReceiptQueue.h` |
| Maintenance undo | Stack (array) | `UndoStack.h` |
| Members | AVL tree | `MemberTree.h` |
| Floor layout, nearest PC, group seating | Graph, **BFS**, **DFS** | `FloorGraph.h` |
| Transaction reports | Insertion sort, bubble sort | `Sorting.h` |
| Transaction lookup | Linear search, binary search | `Searching.h` |

---

## Build and Run

You need a C++17 compiler.

```bash
g++ -std=c++17 -O2 main.cpp -o system
./system
```

---

## Sample Input

Checking in a walk-in customer:

```
Select: 1              (Front Desk)
Select: 1              (Check in a customer)
Customer name: John Pork
Member ID (0 if walk-in): 0
Preferred PC, 0 for any: 0
```

Output:

```
John Pork is seated at PC 01.
```

---

## Main Menu

| Key | Section | What it does |
|---|---|---|
| 1 | Front Desk | Check in a customer or a group, end a session and pay, pause or resume a session, view active sessions and the waiting line. If all PCs are taken, customers join the waiting line. |
| 2 | Computers | View the status board, mark a PC as under maintenance or available, and undo the last maintenance change. |
| 3 | Members | Register a new member, look up a member by ID, and list all members. Members get a 10% discount on billing. |
| 4 | Billing and Reports | View all transactions, sort by highest payment or longest session, search by customer name or receipt number, print the next receipt, and see the daily sales summary. |
| 5 | Performance Lab | Shows the theoretical time complexity of each operation and measured running times. |
| 0 | Exit | Closes the program. |

Pick a number to go in, and `0` to go back.
---

## Team

| Name | Student No. | Role | Main Contributions |
|---|---|---|---|
| Abello, Ralf | 2515011 | Project Leader | |
| Busa, Emmanuel A. | 2516004 | Developer and documentation | `TransactionLog.h`, `FloorGraph.h`, `Cafe.h`, `Benchmark.h` |
| Nacion, Daniela | 2514751 | Developer and documentation | `Types.h`, `Utils.h`, `main.cpp` |
| Paraiso, Wayne | 2512946 | Developer and documentation | `Searching.h`, `Sorting.h`, `MemberTree.h` |
| Serrano, Gabriel | 2515580 | Developer and documentation | Flowchart, `Menu.h`, `Stations.h`, `SessionList.h` |

---

