# cube2-limited

# Author: Olzhas Yergali, 2023
Schweinfurt, Germany


---

### This notebook is dedicated to implement design described by the following paper, implementing learning process of a DNN based on the two Assumptions from the same paper:


> Takano. "Self-Supervision is All You Need for Solving Rubik’s Cube", 2022 [https://arxiv.org/abs/2106.03157]



---


### Asumption from the paper: <br>
When random paths connect two nodes,
more optimal moves are more often the first move. Randomly scrambled, in absence of redundant moves that cancel each other, the scramble is biased toward the optimal solution.

Most of the following code is written by Takano, but the model was trained and built in PyTorch, whereas I decided to stick with Tensorflow.

The following code could be divided on these sections:


1. Imports.
2. Graphing Functions.
3. 2x2x2 Cube Environment .
4. Model creation and compilation.
5. Using TF Data Sequence for creating data stream of states and moves of the cube.
6. Training the model on 10<sup>5</sup> different scrambles, resulting the model to see 11*10<sup>5</sup> states, which are not necessarily unique.
7. Implementation of a Beam Search, which is used to look through a lot of candidates along the way of solving a cube. The beam widths used were 2<sup>8</sup> and 2<sup>12</sup>.
8. Using the Beam Search and the model for trying to solve a 100 scrambled cubes.
9. Plotting the results.



## For more details and insights, please, check out the Notebook I was working in. 

The environment I worked in is whatever Google Colab provides for free at the beginning of April 2023

Kind Regards<br>
Olzhas Yergali
