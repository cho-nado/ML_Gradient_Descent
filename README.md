# Lab Work №1
# Gradient Descent and Its Modifications

###  Task Description

* Select two test optimization functions.
* Implement your own version of the classic gradient descent algorithm.
* Program a testing pipeline for the optimization algorithm.
    * Visualize the function and the optimum point.
    * Calculate the error of the found solution compared to the analytical solution for several runs.
    * Visualize the found solution point (animation can be added for extra points).
* Implement the method for computing the gradient.
    * Allow the gradient function to be passed by the user.
    * Perform symbolic gradient computation (e.g., using SymPy) (for extra points).
    * Implement numerical gradient approximation (for extra points).
* Implement and test one momentum-based modification.
* Implement and test one adaptive modification.
* Implement and test a learning rate evolution method and/or a method for selecting the initial approximation.


# Lab Work №2
## Global Optimization and Metaheuristic Algorithms

In Pygmo, program two test functions of your own and find their optimum using three different algorithms available in the library. Generate a comparison table.


# Summary of Lab Works:
## Lab Work №1: Gradient Descent and Its Modifications

### Objective:
To implement and test various gradient descent methods for optimizing test functions.

## Test Functions:

<img width="528" alt="Снимок экрана 2024-10-14 в 1 34 01 AM" src="https://github.com/user-attachments/assets/e1ac5535-fc07-4f2f-ba34-29392e6813c2">

### Implemented Methods:

1. **Classic Gradient Descent (GD):**
   * The method converged to the minimum but didn’t always reach the global minimum precisely, with errors depending on initial conditions.
   
   **Matyas Function:**
   
   <img width="526" alt="Снимок экрана 2024-10-14 в 1 47 57 AM" src="https://github.com/user-attachments/assets/3c0a3d33-82e6-489d-9a7f-623233dd5d66">
   
   **Levi Function No. 13**
   
    <img width="526" alt="Снимок экрана 2024-10-14 в 1 49 47 AM" src="https://github.com/user-attachments/assets/27ce10e6-dd8a-45fe-a05f-e6b7cb2fdb70">

2. **Momentum Gradient Descent (Inertial GD):**
   * Adding a momentum coefficient accelerated convergence, especially in complex regions, though it did not always achieve the exact minimum.
  
   **Matyas Function:**
   
  <img width="526" alt="Снимок экрана 2024-10-14 в 1 50 37 AM" src="https://github.com/user-attachments/assets/0b10be78-9b8f-47d2-83f8-e0d6c1be861b">

  **Levi Function No. 13**
  
  <img width="526" alt="Снимок экрана 2024-10-14 в 1 50 53 AM" src="https://github.com/user-attachments/assets/24840322-37c5-4465-92df-3bb60e94922a">

3. **Adaptive Gradient Descent (AGD or Adam):**
   * The most accurate method, which showed the fastest convergence and precision for both test functions. The error was minimal, often around 10^-8, indicating high efficiency.
   
   **Matyas Function:**

   <img width="526" alt="Снимок экрана 2024-10-14 в 1 54 54 AM" src="https://github.com/user-attachments/assets/a31591d1-7a90-4223-946b-98fb9b464d0c">
   
   **Levi Function No. 13**

  <img width="523" alt="Снимок экрана 2024-10-14 в 2 00 20 AM" src="https://github.com/user-attachments/assets/8c938650-35c4-4a88-9427-1cd32a50bb6c">

   
4. **Exponential Learning Rate Decay:**
   * Dynamically reducing the learning rate improved convergence stability, but the results showed slight errors, indicating possible overfitting.

  **Matyas Function:**
  
   <img width="526" alt="Снимок экрана 2024-10-14 в 1 57 01 AM" src="https://github.com/user-attachments/assets/0fd7835f-edce-4628-b1c4-6a5441280f5f">

## User-Defined Function (example)

<img width="523" alt="Снимок экрана 2024-10-14 в 1 59 07 AM" src="https://github.com/user-attachments/assets/0085765a-a5e9-414e-8711-ccde5ba61650">



## **Conclusions from Lab Work №1:**

Various modifications of gradient descent have their strengths and weaknesses. Adam demonstrated the best convergence and accuracy for both test cases, while classic gradient descent was less precise and highly dependent on initial conditions. The use of momentum and dynamic learning rate improved results, especially on complex functions like Levi No. 13.

## Lab Work №2: Global Optimization and Metaheuristic Algorithms

### Objective:
To find the optima of test functions using different metaheuristic algorithms from the Pygmo library and compare their efficiency.

## Test Functions:

1. Matyas Function (same as in Lab №1).
2. Levi Function No. 13 (also used in Lab №1).

## Applied Algorithms:

1. **Self-Adaptive Differential Evolution (SADE)** — a self-adaptive differential evolution algorithm.
2. **Differential Evolution (DE)** — differential evolution algorithm.
3. **Simple Genetic Algorithm (SGA)** — a simple genetic algorithm.

## Results:

1. **For the Matyas Function:**
   * **SADE** showed the most accurate convergence with a minimal error of 7.22 × 10^-11.
   * **DE** also achieved good convergence but with a slightly larger error of 2.02 × 10^-10.
   * **SGA** showed the highest error of 0.00072, indicating lower accuracy for this task.
2. **For Levi Function No. 13:**
   * **SADE** again performed the best with the lowest error of 1.81 × 10^-11, almost reaching the global minimum.
   * **DE** showed a slightly larger error of 6.56 × 10^-10
   * **SGA** had the most significant error of 0.00198, confirming its lower efficiency on more complex functions.

## **Conclusions from Lab Work №2:**

Self-Adaptive DE achieved the best results for both functions due to its adaptability in evolution parameters. Differential evolution also proved to be effective, though less precise than SADE. The simple genetic algorithm showed the largest errors, making it less suitable for precise global optimization.
