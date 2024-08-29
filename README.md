 # EXPERIMENT 01:MDP REPRESENTATION

## AIM:
To represent any one real world problem in Markov Decision Problem(MDP).

## PROBLEM STATEMENT:

### Problem Description:
Move a coin to reach the goal in a 3*3 grid.

### State Space:
{0,1,2,3,4,5,6,7,8}

### Sample State:
2

### Action Space:
{Up[0],Down[1],Left[2],Right[3]}

### Sample Action:
Down[1]

### Reward Function:
To reach goal ->+1(Reward)
Otherwise ->0

## GRAPHICAL REPRESENTATION:
![WhatsApp Image 2023-09-01 at 8 16 53 PM](https://github.com/Rithigasri/mdp-representation/assets/93427256/f45e222a-0378-4259-9ca6-929561c48018)

## PYTHON REPRESENTATION:
```
# Creating Dictionary
P={
    0:{
        0:[(0.666,0,0.0,False),(0.333,3,0.0,False)],
        1:[(0.333,3,0.0,False),(0.333,0,0.0,False),(0.333,1,0.0,False)],
        2:[(0.666,0,0.0,False),(0.333,3,0.0,False)],
        3:[(0.333,1,0.0,False),(0.333,0,0.0,False),(0.333,3,0.0,False)]
    },
    1:{
        0:[(0.333,1,0.0,False),(0.333,0,0.0,False),(0.333,2,0.0,False)],
        1:[(0.333,4,0.0,False),(0.333,0,0.0,False),(0.333,2,0.0,False)],
        2:[(0.333,0,0.0,False),(0.333,1,0.0,False),(0.333,4,0.0,False)],
        3:[(0.333,2,0.0,False),(0.333,1,0.0,False),(0.333,4,0.0,False)]
    },
    2:{
        0:[(0.666,2,0.0,False),(0.333,1,0.0,False)],
        1:[(0.333,5,0.0,False),(0.333,1,0.0,False),(0.333,2,0.0,False)],
        2:[(0.333,1,0.0,False),(0.333,2,0.0,False),(0.333,5,0.0,False)],
        3:[(0.666,2,0.0,False),(0.333,5,0.0,False)]
    },
    3:{
        0:[(0.333,0,0.0,False),(0.333,3,0.0,False),(0.333,4,0.0,False)],
        1:[(0.333,6,0.0,False),(0.333,3,0.0,False),(0.333,4,0.0,False)],
        2:[(0.333,3,0.0,False),(0.333,0,0.0,False),(0.333,6,0.0,False)],
        3:[(0.333,4,0.0,False),(0.333,0,0.0,False),(0.333,6,0.0,False)]
    },
    4:{
        0:[(0.333,1,0.0,False),(0.333,3,0.0,False),(0.333,5,0.0,False)],
        1:[(0.333,7,0.0,False),(0.333,3,0.0,False),(0.333,5,0.0,False)],
        2:[(0.333,3,0.0,False),(0.333,1,0.0,False),(0.333,7,0.0,False)],
        3:[(0.333,5,0.0,False),(0.333,1,0.0,False),(0.333,7,0.0,False)]
    },
    5:{
        0:[(0.333,2,0.0,False),(0.333,4,0.0,False),(0.333,5,0.0,False)],
        1:[(0.333,8,1.0,True),(0.333,4,0.0,False),(0.333,5,0.0,False)],
        2:[(0.333,4,0.0,False),(0.333,1,0.0,False),(0.333,7,0.0,False)],
        3:[(0.333,5,0.0,False),(0.333,1,0.0,False),(0.333,7,0.0,False)]
    },
    6:{
        0:[(0.333,3,0.0,False),(0.333,6,0.0,False),(0.333,7,0.0,False)],
        1:[(0.666,6,0.0,False),(0.333,7,0.0,False)],
        2:[(0.666,6,0.0,False),(0.333,3,0.0,False)],
        3:[(0.333,7,0.0,False),(0.333,3,0.0,False),(0.333,6,0.0,False)]
    },
    7:{
        0:[(0.333,4,0.0,False),(0.333,6,0.0,False),(0.333,8,1.0,True)],
        1:[(0.333,7,0.0,False),(0.333,6,0.0,False),(0.333,8,1.0,True)],
        2:[(0.333,6,0.0,False),(0.333,4,0.0,False),(0.333,7,0.0,False)],
        3:[(0.333,8,1.0,True),(0.333,4,0.0,False),(0.333,7,0.0,False)]
    },
    8:{
        0:[(0.333,5,0.0,False),(0.333,7,0.0,False),(0.333,8,1.0,True)],
        1:[(0.666,8,1.0,True),(0.333,7,0.0,False)],
        2:[(0.333,7,0.0,False),(0.333,5,0.0,False),(0.333,8,1.0,True)],
        3:[(0.666,8,1.0,True),(0.333,5,0.0,False)]
    }
}
```
## OUTPUT:
![image](https://github.com/Rithigasri/mdp-representation/assets/93427256/c784b237-419b-4e3f-b7b0-3d5affa10f32)

## RESULT:
Thus a real world problem is represented as Markov Decision Problem in the following ways successfully:
1. Graphical Representation
2. Python Representation

