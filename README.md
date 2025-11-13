# Integrating Machine Learning and Planning as Satisfiability  
**Going beyond Action Model Learning and Heuristics**

This repository contains the slides for the ICAPS tutorial **“Integrating Machine Learning and Planning as Satisfiability: Going beyond Action Model Learning and Heuristics”** by [René Heesch](https://github.com/RHeesch) and [Jonas Ehrhardt](https://github.com/j-ehrhardt).

## Tutorial overview

Planning as satisfiability and SMT (Satisfiability Modulo Theories) provide a powerful framework for encoding and solving planning problems, from classical to numerical domains. However, practical deployment often relies on accurate, manually engineered models of action effects, which limits applicability in complex real-world settings.

Data-driven methods such as action model learning and heuristic learning have been proposed to alleviate this modelling bottleneck, but they are still not widely adopted in deployed planning systems.

This tutorial presents a general paradigm for **embedding trained Machine Learning models into SMT planners**. The approach is based on a *lazy* integration scheme that abstracts neural networks as uninterpreted functions during planning, and only concretizes them via numerical optimization when validating or refining candidate plans.

---

## Content outline

The tutorial is organized into the following sections:

1. **Motivation for ML-Enhanced Planning**
   - Challenges of modelling complex real-world domains
   - Introduction of control parameters for flexible action descriptions

2. **Feature-Vector based State Space Representation**
   - Representing states as feature vectors
   - Using a shared representation for both logical descriptions and neural networks

3. **Learning Preconditions**
   - Exact Preconditions
   - Genralized Preconditions
   - Dependency-Aware Preconditions

4. **Approximating Actions Effects via Neural Networks**
   - Viewing action effects as a functional dependency between (input state, control parameter) and output state
   - Approximating this dependency with neural networks
  
5. **The Eager Planning Approach**
   - Describing neural networks via their inherent mathematical dependencies
   - Integrating these dependencies directly into an SMT planning formulation

6. **The Lazy Planning Approach**
   - Abstract planning with uninterpreted functions
   - Concretization loop and conflict-clause refinement

7. **ML Methods for Concretization**
   - Backpropagation over inputs for control-parameter inference
   - Projected gradient descent and the observer function
---

<img width="1066" height="602" alt="image" src="https://github.com/user-attachments/assets/41d070a0-c230-44fc-8d0a-4608edbeed72" />


