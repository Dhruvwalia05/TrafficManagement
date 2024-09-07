<h1 align="center">🚦 Traffic Light Control System Using Reinforcement Learning</h1>

<div align="center">

[![Python version](https://img.shields.io/badge/python-3.1+-blue.svg)](https://www.python.org/downloads/)

</div>

-------------------------------------

<h3>Description</h3>
This project implements a simulation of an intersection with four traffic lanes (north, east, south, and west) using Reinforcement Learning (RL) to optimize traffic light management. The goal is to minimize vehicle wait times and improve traffic flow efficiency by dynamically adjusting the green light durations based on real-time traffic conditions.

-------------------------------------

<h3>Key Features</h3>
<b>Reinforcement Learning-Based Control:</b> The system uses an RL agent to decide which lane should get the green light based on the current traffic conditions.<br>
<b>Dynamic Traffic Simulation:</b> Random vehicle generation simulates real-world traffic flow, with distinct vehicle densities for peak and off-peak hours.<br>
<b>Customizable Environment:</b> The intersection can handle different traffic loads with parameters such as green light duration, vehicle cross time, and max allowed waiting time for vehicles.<br>
<b>Four-Lane Intersection:</b> Traffic is managed for four lanes—north, east, south, and west—each of which can have its own independent vehicle count and traffic light state.<br>
<b>Flexible Reward System:</b> The reward mechanism incentivizes efficient traffic flow by providing positive rewards for clearing traffic within the allowed time and penalizing delays.<br>

-------------------------------------

<h3>Environment Details</h3>
<b>Action Space: </b>Discrete action space representing the 4 lanes, with the agent choosing which lane gets the green light.<br>
<b>Observation Space: </b>The current state is represented by the number of vehicles waiting in each lane.<br>
<b>Vehicle Cross Time: </b>The time it takes for each vehicle to pass through the intersection (configurable, default is 3 seconds per vehicle).<br>
<b>Green Light Duration: </b>The default green light duration is 10 seconds, but it adapts dynamically based on the traffic load.<br>
<b>Peak/Off-Peak Simulation: </b>Randomized vehicle generation simulates varying traffic density based on time of day, accounting for morning and evening rush hours.<br>
<b>Max Steps Per Episode:</b> Each episode has a limit of 100 steps, with penalties applied if this limit is reached without efficient traffic management.<br>

-------------------------------------

<h3>Simulation Workflow</h3>
<b>Vehicle Generation:</b> Random vehicles are generated for each lane based on the time of day (peak or off-peak hours).<br>
<b>Traffic Light Management:</b> The RL agent observes the traffic situation and chooses which lane receives the green light to optimize vehicle flow.<br>
<b>Reward Calculation:</b> Positive rewards are given for clearing vehicles efficiently, while negative rewards are applied for traffic delays or inefficiencies.<br>
<b>Step and Episode Tracking:</b> Each episode progresses until the maximum number of steps is reached or all lanes are cleared of vehicles.<br>
