# The V-HACD library decomposes a 3D surface into a set of "near" convex parts.

![Approximate convex decomposition of "Camel"](https://github.com/kmammou/v-hacd/raw/master/doc/acd.png)

# Why do we need approximate convex decomposition?

Collision detection is essential for [realistic physical interactions](https://www.youtube.com/watch?v=oyjE5L4-1lQ) in video games and computer animation. In order to ensure real-time interactivity with the player/user, video game and 3D modeling software developers usually approximate the 3D models composing the scene (e.g. animated characters, static objects...) by a set of simple convex shapes such as ellipsoids, capsules or convex-hulls. In practice, these simple shapes provide poor approximations for concave surfaces and generate false collision detection.

![Convex-hull vs. ACD](https://raw.githubusercontent.com/kmammou/v-hacd/master/doc/chvsacd.png)

A second approach consists in computing an exact convex decomposition of a surface S, which consists in partitioning it into a minimal set of convex sub-surfaces. Exact convex decomposition algorithms are NP-hard and non-practical since they produce a high number of clusters. To overcome these limitations, the exact convexity constraint is relaxed and an approximate convex decomposition of S is instead computed. Here, the goal is to determine a partition of the mesh triangles with a minimal number of clusters, while ensuring that each cluster has a concavity lower than a user defined threshold.

![ACD vs. ECD](https://raw.githubusercontent.com/kmammou/v-hacd/master/doc/ecdvsacd.png)

# Installing the Package

On Windows, go to the ./app directory and run 'cmake CMakeLists.txt' and then load the solution file
On Linux, go to the ./app directory and run 'cmake CmakeLists.txt' and then run 'cmake --build .' to build the test app

![Documentation](https://docs.google.com/presentation/d/1OZ4mtZYrGEC8qffqb8F7Le2xzufiqvaPpRbLHKKgTIM/edit?usp=sharing)