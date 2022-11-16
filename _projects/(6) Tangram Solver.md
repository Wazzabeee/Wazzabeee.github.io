---
name: Tangram Solver
tools: [Python, Backtrack, Algorithm, AI, Puzzle, Tkinter, Gui, Geometric, Figure]
image: ../assets/img/portfolio/tangram_solver/tangram.png
description: Python graphical user interface developed in order to demonstrate the quality of the backtracking algorithm implemented to solve Tangram puzzles.
---

# Tangram Solver

This project was made part of Artificial Intelligence course at <a href="https://www.utbm.fr/" target="_blank" rel="noopener noreferrer">UTBM</a> in collaboration with <a href="https://github.com/axel7083" target="_blank" rel="noopener noreferrer">Axel</a>. It solves Tangram puzzles using backtracking algorithm.

## Problem

A simple observation can be made when observing this problem, it is that the number of pieces is relatively small (7). The idea of simply testing all the possibilities is then very tempting. The first problem that appears is the infinity of the possibilities, indeed since the pieces can be placed anywhere, it is necessary to find a way to reduce this field of possibilities.

The solution we have adopted is based on a logical placement. First of all let's define how the program should work.

The program must take as input 2 arguments, the desired shape, which will be defined as a list of polygons (here the head and the body are two distinct polygons), and the list of basic polygons used to constitute it. The result of the program must be a positioning of the basic shapes forming the complex polygon(s).

{% include elements/figure.html image="../assets/img/portfolio/tangram_solver/solution_example.png" caption="Resolution illustration" %}

Thus, the program has access to all the characteristics of the original shape, i.e. the coordinates of each of its vertices (red dots). A trivial observation is that the vertices of the basic pieces must match the vertices of the complex piece.

The imagined solution is then to navigate on each of the vertices of the complex piece, and to position the pieces one by one for each of them, the area of the difference between the complex shape and the piece is equal to the area of the complex shape minus the area of the basic shape. Thus, we are sure to cover the complex shape with the basic shape.
The program will therefore, for each of the shapes, place the unknown shape in the way that fills the maximum possible, and then place the next one. In the event that it is impossible to place a new piece, the program goes back and changes the position of the last placed piece to a position that also fills the maximum.

{% include elements/figure.html image="../assets/img/portfolio/tangram_solver/simple.png" caption="Correct & incorrect placement" %}

As stated before, the solution we adopted is called backtracking. This solution belongs to a family of algorithms that can solve algorithmic problems. And more precisely, problems of constraint satisfaction (optimization or decision). These algorithms allow to systematically test all the potential assignments of the problem. 
The principle is quite simple: the algorithm selects a variable of the problem, and for each possible assignment of this one, we test recursively if a valid solution can be built from this partial assignment.
Finally, if all the tests are successful with this partial assignment, we abandon it and return to the assignments that were previously made (hence the name "return on trace").

## Results

{% capture carousel_images %}

../assets/img/portfolio/tangram_solver/heart.png
../assets/img/portfolio/tangram_solver/heart_solution.png
../assets/img/portfolio/tangram_solver/square.png
../assets/img/portfolio/tangram_solver/square_solution.png
../assets/img/portfolio/tangram_solver/cat.png
../assets/img/portfolio/tangram_solver/cat_solution.png
../assets/img/portfolio/tangram_solver/duck.png
../assets/img/portfolio/tangram_solver/duck_solution.png

{% endcapture %}
{% include elements/carousel.html %}

## Graphical User Interface

The GUI has been developed using Tkinter's library. The user can vary the number of pieces for the puzzle and place them on the canvas. A sort of magnetization has been implemented so that it is easier to juxtapose puzzle's pieces. When the user is satisfied with the figure, he can click on the solve button and wait for the AI solution to appear.

{% include elements/figure.html image="../assets/img/portfolio/tangram_solver/tangram.png" caption="GUI" %}

## Used Software and Libraries
- Programming languages: Python
- Libraries: Tkinter, MatPlotLib, Shapely
- Source control: GitHub
- Other tools: PyCharm

<p class="text-center">
{% include elements/button.html link="https://github.com/Wazzabeee/tangram-solver" text="Code" %}
</p>