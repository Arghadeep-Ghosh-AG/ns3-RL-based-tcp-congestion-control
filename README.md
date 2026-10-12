# ns3-RL-based-tcp-congestion-control
RL-based TCP congestion control using ns-3.43, PPO, BBR, and Reno.


cat > README.md <<'EOF'
# RL-Based TCP Congestion Control

An experimental reinforcement-learning project using ns-3.43,
Python, Gymnasium, Stable-Baselines3, and PPO.

## Objectives

- Establish TCP BBR and Reno baseline measurements.
- Evaluate throughput and packet loss.
- Develop a PPO-based sending-rate optimization prototype.
- Compare the proposed approach against baseline TCP algorithms.

## Technologies

- C++
- Python
- ns-3.43
- Gymnasium
- Stable-Baselines3
- Proximal Policy Optimization (PPO)

## Project Status

Work in progress. The initial prototype uses episode-based simulation.
The current application-rate controller does not directly replace
the internal TCP congestion-control algorithm.

## Setup

Install ns-3.43 and configure a Python virtual environment.
Install the Python dependencies:

    pip install gymnasium stable-baselines3 numpy

Build ns-3 from its root directory:

    ./ns3 build

Run the baseline from the ns-3 root directory:

    ./ns3 run "scratch/rl-tcp-project/tcp-baseline --tcpType=TcpBbr"

    ./ns3 run "scratch/rl-tcp-project/tcp-baseline --tcpType=TcpLinuxReno"

Run PPO training from the project directory after the Python
environment and integration files are configured:

    python train_ppo.py
EOF
