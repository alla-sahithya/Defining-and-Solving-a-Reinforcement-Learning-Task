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

Random Steps Visualization:  
![image](https://github.com/user-attachments/assets/a34600ae-a354-4a15-b20f-dbf5c8a81807)  
![image](https://github.com/user-attachments/assets/b1c3fe3f-eca4-4b7f-9a45-d2fbbebb0f8b)  

**Safety in AI:**  
• The environment restricts the agent to stay within the defined grid boundaries, preventing it from going out of boundary.  
• The environment also checks the validity of actions before applying them. If it is an invalid action, it will raise a ValueError.  
• The environment also provides a transparent interface for actions through the ‘step’ and ‘reset’ methods. It also checks for terminal conditions to ensure the agent’s safety.  
• The state space is discretized and the ‘state_to_index’ method makes sure that the agent navigates within the defined state space.  
• The environment also enforces a maximum step limit, preventing prolonged interactions and enhancing the safety of our agent by ensuring the controlled exploration.  


# SARSA Agent:  
**Update Function:**   
• This agent chooses actions based on an epsilon-greedy policy.  
• This agent uses the SARSA (State Action Reward State Action) algorithm.  
• The Q-values are updates using the formula –  
![image](https://github.com/user-attachments/assets/028d6050-dcdb-40f8-811e-356c0748d56e)  
 where s is current state, a is current action, s’ is next state, a’ is next action, r is reward, alpha is learning rate and gamma is discount factor.  
**Key Features:**  
• Simple  
• Easy to implement  
• Balances exploration-exploitation using epsilon-greedy strategy   
• Suitable for episodic tasks  
**Advantage:**  
• Converges for certain problems, is model-free, and well-suited for online learning.  
• Guarateed Policy improvement  
• On-policy learning ensures safety in real-world applications  
**Disadvantages:**  
• Slow convergency because of on-policy learning  
• Sensitive to hyperparameter choices  
• Exploration-exploitation trade-off challenges  
