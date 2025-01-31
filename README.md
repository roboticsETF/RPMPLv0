# Rapid Prototyping Motion Planning Library v0 (MATLAB)

In this repository, the MATLAB code of two new algorithms are provided:

DRGBT (Dynamic Rapidly-exploring Generalized Bur Tree) algorithm is intended for motion planning in dynamic environments. The main idea behind DRGBT lies in a so-called adaptive horizon, consisting of a set of prospective target nodes that belong to a predefined C-space path, which originates from the current node. Each node is assigned a weight that depends on relative distances and captured changes in the environment. The algorithm continuously uses a suitable horizon assessment to decide when to trigger the replanning procedure.

RGBMT* (Rapidly-exploring Generalized Bur Multi-Tree star) algorithm is intended for asymptotically optimal motion planning for robotic manipulators in static environments. The main idea is the generation of local/extra trees rooted in some random configurations, beside two main trees rooted in initial and goal configurations. Each local tree is expanded towards all other trees generating a bur of free configuration C-space. Each node is assigned a cost-to-come value, which is then used to optimally connect (if possible) all nodes from local trees to a single main tree according to Bellman’s principle of optimality. Configuration space is carefully sampled in order to properly grow main and local trees.
