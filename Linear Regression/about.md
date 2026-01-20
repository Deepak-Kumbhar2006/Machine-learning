# Linear Regression From Scratch 🚀

This repository contains a **from-scratch implementation of Linear Regression using Gradient Descent**, built **without using machine learning libraries** such as scikit-learn.

The objective of this project is **conceptual clarity** — understanding the mathematics and optimization behind linear regression rather than treating it as a black box.

---

## 📌 What is Linear Regression?

Linear Regression is a **supervised learning algorithm** used to model the relationship between:
- Input feature(s) `X`
- A continuous target variable `Y`

It assumes this relationship can be approximated using a straight line.

### Simple Linear Regression Model


y' = w x + b


Where:
- `w` → weight (slope)
- `b` → bias (intercept)
- `ŷ` → predicted value

---

## 🎯 Objective

The goal of linear regression is to find the optimal values of `w` and `b` such that the **prediction error is minimized** across the dataset.

---

## 📉 Error, Loss, and Cost

### Error (per data point)

Error(i) = y(i) - y'(i)


---

### Loss Function (per data point)

We square the error to:
- Eliminate sign ambiguity
- Penalize larger errors more strongly


text{Loss}_i = (y(i) - y'(i))^2


---

### Cost Function (entire dataset)

The cost function is the **average loss** across all samples.


J(w, b) = (1/2n) * sum of i = 0 to n [(y(i) - (w x_i + b))^2 ]

---

## 🧠 Why Mean Squared Error (MSE)?

MSE is preferred because:
- It is **convex** → guarantees a global minimum
- It is **differentiable**
- It aligns with the assumption of Gaussian noise

---

## 🏔️ Geometry of the Cost Function

- With one parameter, the cost function forms a **U-shaped curve**
- With two parameters (`w` and `b`), it forms a **bowl-shaped surface**

Gradient descent moves **down this surface** to reach the minimum.

---

## 🔁 Gradient Descent

Gradient Descent is an **optimization algorithm** used to minimize the cost function.

It works by repeatedly updating parameters in the direction that reduces the cost the fastest.

---

## 🧭 Gradient Intuition

- The gradient points in the direction of **steepest increase**
- To minimize cost, we move in the **opposite direction**

General update rule:


Θ’ := θ - α * J(θ)


Where:
- `α` → learning rate
- `∇J(θ)` → gradient of the cost function

---

## ⚙️ Gradients for Linear Regression

Given:


J(w, b) = (1/2n) sum (y - y')^2


### Gradient with respect to weight `w`


∂J/∂w
= -1/n sum of i = 0 to n (y(i) - y'(i))x_i


---

### Gradient with respect to bias `b`


∂J/∂b
= -1/n sum of i = 0 to n (y(i) - y'(i))


---

## 🚀 Parameter Update Rules


w := w + α * 1/n sum (y - y')x



b := b + α * 1/n sum (y - y')


---

## 🎚️ Learning Rate (α)

The learning rate controls **step size** during optimization.

| Learning Rate | Effect |
|--------------|--------|
| Too small | Very slow convergence |
| Too large | Overshooting / divergence |
| Optimal | Fast and stable convergence |

---

## ⏹️ Stopping Criteria

Training stops when:
- Change in cost is below a threshold (convergence)
- Maximum number of iterations is reached

This prevents unnecessary computation.

---

## 📦 Implementation Highlights

- Parameters initialized randomly in range `[-1, 1]`
- Uses **Batch Gradient Descent**
- Tracks cost history
- Convergence-based stopping condition

---

## 📊 Visualization

The notebook includes:
- Scatter plot of original data
- Regression line
- Cost convergence behavior

---

## 🧪 Why Build From Scratch?

Implementing from scratch helps in:
- Understanding optimization deeply
- Grasping backpropagation later
- Debugging ML models effectively
- Building strong ML fundamentals

---

## 📌 Key Takeaways

- Linear Regression is an optimization problem
- Gradient Descent minimizes cost iteratively
- Cost function is convex
- Parameters may increase or decrease — cost must decrease
- Learning rate controls stability

---

## 🔮 Future Improvements

- Multivariate Linear Regression
- Feature Scaling
- Stochastic / Mini-batch Gradient Descent
- Regularization (Ridge & Lasso)
- Matrix-based implementation

---

## 👤 Author

**Deepak**  
Computer Science Engineering Student  
Focused on building strong machine learning fundamentals from first principles.

---

## ⭐ Support

If this repository helped you understand Linear Regression better, consider starring ⭐ it.
