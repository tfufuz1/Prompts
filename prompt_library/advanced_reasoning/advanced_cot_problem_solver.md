# Advanced Problem Solver (Chain-of-Thought Reasoning)

**Objective:** To solve a complex problem by explicitly detailing the reasoning process step-by-step.

**User Instructions:**

Please state the complex problem you would like me to solve. The more detail you provide about the problem, the better I can assist you.

**AI Instructions:**

Once the user has stated the problem, your task is to solve it by demonstrating a clear Chain-of-Thought (CoT) reasoning process. Please adhere to the following structure:

1.  **Understand the Problem:**
    *   Briefly restate the problem in your own words to ensure you've understood it correctly.
    *   Identify the core question(s) to be answered or the primary goal to be achieved.

2.  **Identify Assumptions:**
    *   Explicitly list any assumptions you are making to solve the problem. This is important for transparency and for understanding the context of your solution.

3.  **Think Step-by-Step (Chain of Thought):**
    *   Break down the problem into smaller, manageable steps.
    *   For each step, clearly explain your reasoning. Show your work.
    *   Detail the information or logic you are using to move from one step to the next.
    *   If you encounter a point where different approaches could be taken, explain why you chose a particular path.

4.  **Identify Potential Areas of Uncertainty:**
    *   As you reason through the problem, note any areas where information is missing, ambiguous, or where your conclusions depend heavily on your initial assumptions.
    *   Highlight aspects of your reasoning that might change if new information were available.

5.  **Solution/Conclusion:**
    *   Based on your step-by-step reasoning, present the solution or conclusion.
    *   If applicable, briefly summarize the key steps that led to this solution.

6.  **Confidence Level (Optional):**
    *   If appropriate for the problem, indicate your confidence in the solution and briefly explain what factors influence this confidence.

**Example Interaction:**

**User:** "I have a budget of $100. I need to buy apples, bananas, and cherries. Apples cost $2/kg, bananas $1/kg, and cherries $5/kg. I need at least 1kg of each fruit, but I want to maximize the total kilograms of fruit I can buy. How many kgs of each should I get?"

**AI (following the structure above):**

1.  **Understand the Problem:** The user wants to maximize the total kilograms of apples, bananas, and cherries they can buy with $100, given individual fruit prices and the constraint of buying at least 1kg of each.

2.  **Identify Assumptions:**
    *   I assume the user can buy fractional kilograms of fruit (e.g., 1.5 kg).
    *   I assume the prices are fixed.
    *   I assume the $100 is the absolute maximum to be spent.

3.  **Think Step-by-Step:**
    *   **Step 1: Account for minimum purchase.**
        *   The user needs 1kg of apples, 1kg of bananas, and 1kg of cherries.
        *   Cost of 1kg apples = $2.
        *   Cost of 1kg bananas = $1.
        *   Cost of 1kg cherries = $5.
        *   Total cost for minimums = $2 + $1 + $5 = $8.
    *   **Step 2: Calculate remaining budget.**
        *   Remaining budget = Total budget - Cost of minimums = $100 - $8 = $92.
    *   **Step 3: Determine how to spend the remaining budget to maximize kilograms.**
        *   To maximize kilograms with the remaining $92, I should prioritize buying more of the cheapest fruit.
        *   Bananas cost $1/kg (cheapest).
        *   Apples cost $2/kg.
        *   Cherries cost $5/kg (most expensive).
        *   Therefore, I should spend the entire remaining budget on bananas.
    *   **Step 4: Calculate additional kilograms of the cheapest fruit.**
        *   Additional bananas = Remaining budget / Price of bananas = $92 / $1/kg = 92 kg.
    *   **Step 5: Calculate total kilograms of each fruit.**
        *   Apples: 1 kg (minimum)
        *   Bananas: 1 kg (minimum) + 92 kg (additional) = 93 kg
        *   Cherries: 1 kg (minimum)
    *   **Step 6: Calculate total kilograms of fruit and total cost.**
        *   Total fruit = 1kg + 93kg + 1kg = 95 kg.
        *   Total cost = (1kg * $2) + (93kg * $1) + (1kg * $5) = $2 + $93 + $5 = $100.

4.  **Identify Potential Areas of Uncertainty:**
    *   The assumption about buying fractional kilograms is key. If only whole kilograms are allowed, the problem becomes an integer optimization problem, which would require a different approach (e.g., exploring combinations or more complex algorithms).

5.  **Solution/Conclusion:**
    *   To maximize the total kilograms of fruit, the user should buy:
        *   Apples: 1 kg
        *   Bananas: 93 kg
        *   Cherries: 1 kg
    *   This will result in a total of 95 kg of fruit for exactly $100.

---
**User, please state your problem below.** I will "think step-by-step" to help you find a solution.
