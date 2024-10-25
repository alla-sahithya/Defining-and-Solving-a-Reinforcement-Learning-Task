# Defining-and-Solving-a-Reinforcement-Learning-Task  

# RL Environment:
**Theme:** Lawnmower Grid World  
**States:** There are 16 states (4*4 grid) -  
{S1 = (0,0), S2 = (0,1), S3 = (0,2), S4 = (0,3), S5 = (1,0), S6 = (1,1), S7 = (1,2), S8 = (1,3), S9 = (2,0), S10 = (2,1), S11 = (2,2), S12 = (2,3), S13 = (3,0), S14 = (3,1), S15 = (3,2), S16 = (3,3)}  
**Actions:** Four actions – {Up, Down, Right, Left}  
**Rewards:** Goal state = 10, two positive rewards = 5 each, two negative rewards = -6 each {5, 5, -6, -6, 10}  
**Objective:** The main objective is for the agent to move in the grid world reaching the goal state to receive a maximum positive reward by avoiding the negative rewards.  
• Also, the termination conditions are as follows -  
  o If the goal state is reached  
  o If the max steps given is exceeded  
• The rewards will not be null once after collected. They will remain the same.  

In the below visualized environment, the goal state is marked as green, positive rewards with teal, negative rewards with blue, and the agent’s current position is denoted by yellow.  

![image](https://github.com/user-attachments/assets/3985a158-4072-47d1-aabb-ccd3b23b36bc)  

![image](https://github.com/user-attachments/assets/a34600ae-a354-4a15-b20f-dbf5c8a81807)  
![image](https://github.com/user-attachments/assets/b1c3fe3f-eca4-4b7f-9a45-d2fbbebb0f8b)


