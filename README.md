# SUMO Traffic Simulator Tutorial

A comprehensive tutorial project demonstrating traffic simulation and adaptive traffic signal control using SUMO (Simulation of Urban Mobility) and Python's TraCI interface. This repository explores various approaches from basic vehicle monitoring to advanced reinforcement learning for intelligent traffic management.

 # Project Overview
This tutorial series demonstrates progressively complex traffic simulation scenarios, including:

# Basic vehicle monitoring and control
Traffic light management for emergency vehicles
Reinforcement learning approaches for adaptive traffic signal control
Connected and autonomous vehicle (CAV) simulations
#  Prerequisites
Required Software
SUMO (Simulation of Urban Mobility) - Latest version
Python 3.7+
SUMO_HOME environment variable properly configured
# Python Dependencies
pip install numpy matplotlib tensorflow keras
SUMO Installation
Download and install SUMO from Eclipse SUMO
Set the SUMO_HOME environment variable to your SUMO installation directory
Ensure SUMO tools are accessible in your system PATH
📁 Project Structure
├── Traci1.py          # Basic vehicle speed monitoring
├── Traci2.py          # Vehicle position and movement control
├── Traci3.py          # Network analysis using SUMOLib
├── Traci4.py          # Emergency vehicle traffic light preemption
├── traci5.FT.py       # Fixed-time traffic signal control with RL setup
├── traci6.QL.py       # Q-Learning for adaptive traffic signal control
├── traci7.DQL.py      # Deep Q-Learning for traffic signal optimization
└── traci8.CAVs.py     # Connected and Autonomous Vehicles simulation
🚀 Getting Started
1. Environment Setup
Ensure your SUMO_HOME environment variable is set:

# Windows
set SUMO_HOME=C:\Program Files\Eclipse\Sumo

# Linux/Mac
export SUMO_HOME=/usr/local/sumo
2. Running the Tutorials
Each Python file represents a different tutorial level. Run them in order for a progressive learning experience:

Basic Vehicle Monitoring (Traci1.py)
python Traci1.py
Monitors vehicle speed in real-time
Demonstrates basic TraCI connection setup
Vehicle Movement Control (Traci2.py)
python Traci2.py
Controls vehicle position and movement
Shows how to manipulate vehicle trajectories
Network Analysis (Traci3.py)
python Traci3.py
Analyzes network properties using SUMOLib
Calculates average speeds across network edges
Emergency Vehicle Priority (Traci4.py)
python Traci4.py
Implements traffic light preemption for emergency vehicles
Demonstrates intelligent traffic signal control
Fixed-Time Control with RL Setup (traci5.FT.py)
python traci5.FT.py
Sets up reinforcement learning environment
Implements fixed-time traffic signal control as baseline
Q-Learning Traffic Control (traci6.QL.py)
python traci6.QL.py
Implements Q-Learning algorithm for adaptive signal control
Learns optimal traffic signal timing policies
Deep Q-Learning Optimization (traci7.DQL.py)
python traci7.DQL.py
Uses deep neural networks for traffic signal control
Handles complex state spaces with deep reinforcement learning
Connected Autonomous Vehicles (traci8.CAVs.py)
python traci8.CAVs.py
Simulates connected and autonomous vehicles
Analyzes travel time improvements
🧠 Reinforcement Learning Features
State Space
The RL implementations use:

Queue lengths from traffic detectors
Current traffic signal phase
Vehicle counts and speeds
Action Space
Traffic signal phase selection
Phase duration optimization
Reward Function
Minimizes total waiting time
Reduces queue lengths
Optimizes traffic flow
Algorithms Implemented
Q-Learning: Tabular reinforcement learning approach
Deep Q-Network (DQN): Neural network-based Q-learning
Fixed-Time Control: Baseline comparison method
📊 Configuration Files
The project uses several SUMO configuration files:

Traci.sumocfg - Basic simulation configuration
RL.sumocfg - Reinforcement learning simulation setup
CAVs.sumocfg - Connected autonomous vehicle scenarios
Test1.sumocfg - Emergency vehicle testing
🔧 Customization
Modifying Traffic Scenarios
Edit the .sumocfg files to change simulation parameters
Adjust network files to modify road layouts
Modify vehicle routes and types in route files
Tuning RL Parameters
Key parameters in RL scripts:

TOTAL_STEPS = 10000      # Training duration
EPSILON = 0.9            # Exploration rate
LEARNING_RATE = 0.1      # Learning rate
DISCOUNT_FACTOR = 0.95   # Future reward discount
Adding New Scenarios
Create new .sumocfg configuration file
Develop corresponding network and route files
Implement Python script following the established pattern
📈 Performance Metrics
The simulations track various metrics:

Average waiting time per vehicle
Queue lengths at intersections
Travel times across the network
Throughput (vehicles per hour)
Fuel consumption and emissions
🤝 Contributing
Contributions are welcome! Areas for improvement:

Additional RL algorithms (A3C, PPO)
Multi-agent traffic control
Real-world network integration
Advanced CAV coordination strategies
📚 Learning Objectives
By completing this tutorial series, you will learn:

SUMO simulation environment setup and configuration
TraCI API for traffic simulation control
Basic traffic signal control algorithms
Reinforcement learning applications in transportation
Connected and autonomous vehicle concepts
Performance evaluation of traffic control strategies
🔍 Troubleshooting
Common Issues
SUMO_HOME not set: Ensure environment variable points to SUMO installation
Import errors: Install required Python packages
Configuration file not found: Ensure .sumocfg files are in the correct directory
Simulation won't start: Check SUMO GUI availability and display settings
Debug Mode
Add --verbose flag to SUMO configuration for detailed logging:

Sumo_config = [
    'sumo-gui',
    '-c', 'your_config.sumocfg',
    '--verbose'
]
📄 License
This project is open source and available under the MIT License.

🙏 Acknowledgments
Eclipse SUMO development team
Traffic simulation research community
Reinforcement learning in transportation research
📞 Support
For questions and support:

Check SUMO documentation: SUMO Documentation
Review TraCI API reference: TraCI Commands
Happy Simulating! 🚗💨
