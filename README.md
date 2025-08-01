GDRL: Geometry and Flow Optimization with DRL
This repository contains the source code for our DRL-based framework designed to optimize heat sink geometry, flow parameters (Reynolds number), and material selection under varying thermal loads.

🧠 Methods
We provide two versions of the reinforcement learning agent:

basic_agent/: A baseline policy-gradient agent for initial performance benchmarking.

ppo_curriculum_agent/: An improved PPO-based agent with curriculum learning, surrogate models, and generalization across fluids and heat fluxes.

⚙️ Problem Description
The agent interacts with a simulated environment to maximize the ratio of heat transfer to pressure drop (Nu / ΔP). Actions include:

4 B-spline control points (geometry)

1 Reynolds number

3 logits (for selecting one among water, ethylene glycol, or air)

The heat source varies across episodes, making the agent generalize across q* ∈ [0, 1].

📁 Structure
Copy
Edit
📦GDRL
 ┣ 📂basic_agent
 ┃ ┗ agent_pg.py
 ┣ 📂ppo_curriculum_agent
 ┃ ┣ agent_ppo.py
 ┃ ┗ surrogate_models/
 ┗ README.md
📈 Results
The upgraded agent significantly outperforms the baseline in thermal performance and adaptability, especially under high heat flux scenarios.

📜 Citation
If you find this useful, please cite the related paper (add citation here once published).

📎 License
MIT License.
