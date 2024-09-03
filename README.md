# MDP REPRESENTATION

## AIM:
To create a MDP (Markov Decision Process) for the undertaken problem statement

## PROBLEM STATEMENT:
Finding class room in university building ground floor.

### Problem Description
Find a specific classroom on the ground floor. 7 states and 4 actions.


### State Space
Specific locations on the ground floor such as hallways and intersections.

Specific classrooms on the ground floor.

### Sample State
S1 : At the entrance of the ground floor.

S2 : In hallway 1.

S3: In hallway 2.

𝑆4: At the intersection of two hallways.

𝑆5: In front of classroom 101.

𝑆6: In front of classroom 102.

s7: In front of classroom 103.

### Action Space
There are four actions 

A1: Move forward.

𝐴2: Turn left.

𝐴3: Turn right.

𝐴4: Enter a classroom.

### Sample Action
Initial State: The student starts at the entrance 

S1 on the ground floor.Goal State: The student needs to find classroom 101, which is on the ground floor.

Policy Example:

𝜋(𝑆1)=𝐴1π(S1)=A 1(Move forward to hallway 1).

𝜋(𝑆2)=𝐴3π(S 2)=A3(Turn right to reach classroom 101).

𝜋(𝑆5)=𝐴4π(S5)=A 4(Enter classroom 101).

### Reward Function
R(S5)=+10 (Reward for finding the correct classroom, e.g., 101).

R(S6)=−1 (Penalty for finding the wrong classroom, e.g., 102).

𝑅(𝑆2)=0R(S 2)=0 (Neutral reward for just being in the hallway).

### Graphical Representation

![WhatsApp Image 2024-08-27 at 8 23 26 AM](https://github.com/user-attachments/assets/c93331f6-e0ef-4215-836e-242f1f50e078)


## PYTHON REPRESENTATION:
```
solver_mdp = {
    # State S1: Entrance
    1: {
        1: [(1.0, 2, -1, False)],  # Move forward to Hallway 1 (S2)
    },
    # State S2: Hallway 1
    2: {
        1: [(1.0, 5, 10, True)],   # Turn right to Classroom 101 (S5), goal state with reward 10
        2: [(1.0, 4, -1, False)],  # Move forward to Intersection (S4)
    },
    # State S3: Hallway 2
    3: {
        1: [(1.0, 6, -1, False)],  # Move forward to Classroom 102 (S6), wrong classroom with penalty -1
        3: [(1.0, 4, -1, False)],  # Move backward to Intersection (S4)
    },
    # State S4: Intersection
    4: {
        1: [(1.0, 2, -1, False)],  # Turn left to Hallway 1 (S2)
        2: [(1.0, 3, -1, False)],  # Move forward to Hallway 2 (S3)
    },
    # State S5: Classroom 101 - Goal State
    5: {
        # No actions needed since this is the terminal state
    },
    # State S6: Classroom 102
    6: {
        # No further actions; penalty for entering the wrong classroom
    }
}

```

## OUTPUT:
![image](https://github.com/user-attachments/assets/5e99a80c-a122-4ef0-b2a5-9cac6d8883a5)


## RESULT:
Thus, the MDP for a stochastic model using python is implemented successfully
