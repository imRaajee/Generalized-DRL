# GDRL: Geometry and Flow Optimization with DRL

This repository contains **the source code for our DRL-based framework designed to optimize heat sink geometry, flow parameters (Reynolds number), and material selection under varying thermal loads**.

## 🧠 Methods
We provide two versions of the reinforcement learning agent:

- `/Simple-Policy/`: A baseline policy-gradient agent for initial performance benchmarking.
-`/Upgraded/`: An improved PPO-based agent with curriculum learning, q-bathces, surrogate models, and generalization across fluids and heat fluxes.

## ⚙️ Problem Description
The agent interacts with a simulated environment to maximize the ratio of heat transfer to pressure drop (Nu / ΔP). Actions include:
4 B-spline control points (geometry)
1 Reynolds number
3 logits (for selecting one among water, ethylene glycol, or air)
The heat source varies across episodes, making the agent generalize across q* ∈ [0, 1].

## 📜 Citation
If you find this useful, please cite the related paper.

## 📎 License
MIT License.
