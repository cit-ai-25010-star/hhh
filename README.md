# AI Model & Training Pipeline Manager (C++17 OOP Project)

A modern Object-Oriented C++17 application designed for second-year Artificial Intelligence students. This project simulates an automated machine learning training pipeline that manages datasets, trains different types of AI architectures (Computer Vision and NLP), evaluates their performance, and handles runtime exceptions safely.

---

## Core OOP Concepts Demonstrated

| OOP Concept | Implementation in Project |
| :--- | :--- |
| **Encapsulation & Constructors** | Protected and private attributes (`modelName`, `learningRate`, `accuracy`) initialized safely via parameterized constructors. |
| **Abstraction** | `AIModel` acts as an abstract base class defining a pure virtual `train()` interface. |
| **Inheritance** | `VisionModel` and `NLPModel` inherit core attributes and evaluation logic from `AIModel`. |
| **Polymorphism** | Runtime polymorphism via `std::shared_ptr<AIModel>` executing specialized `train()` methods for images vs. text. |
| **Composition** | `TrainingPipeline` contains a `Dataset` object as a core member (a pipeline cannot exist without data). |
| **Operator Overloading** | Overloaded the `>` operator in `AIModel` to directly compare models based on their accuracy. |
| **Exception Handling** | `try / catch` blocks with `std::invalid_argument` and `std::out_of_range` to validate learning rates, epochs, and dataset sizes. |
| **STL & Modern C++17** | Uses `std::vector`, `std::shared_ptr`, `std::move`, and `override` for safe memory management without memory leaks. |

---

## How to Compile and Run

Using **G++ (C++17)** inside the course Docker environment or any local terminal:

```bash
# Compile with warnings enabled
g++ -std=c++17 -Wall -Wextra -g main.cpp -o app

# Run the executable
./app