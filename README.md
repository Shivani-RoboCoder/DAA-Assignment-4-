# Airline Crew Scheduling – Backtracking + Constraint Satisfaction

## 1. Problem Overview

This project solves a small version of the **Airline Crew Scheduling** problem.

We have:

- A list of **flights** with start and end times  
- A list of **crew members**

The goal is to **assign flights to crew members** so that:

1. No crew member has **overlapping flights**
2. Each crew member has at least a **minimum rest time** (e.g., 1 hour) between two flights
3. (Optional) We can try to **minimize total cost** of assignments using a cost function


## 2. Algorithmic Strategy

- **Main Strategy:** Backtracking (Constraint Satisfaction)
- **Key Ideas:**
  - Try to assign each flight to a crew member.
  - Before assigning, check **constraints** (no overlap, enough rest).
  - If no valid assignment is possible at some step, **backtrack** and try a different choice.
- **Optional Extension:** Cost-aware backtracking to find the **minimum-cost valid schedule**.


## 3. Data Model

### Flights

Each flight is stored as a tuple:

```python
(id, start_time, end_time)
