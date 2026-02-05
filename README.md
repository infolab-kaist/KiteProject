# Kite Project

Welcome to the KAIST Infolab Task-driven Educational Project, a.k.a **Kite Project**. This project is a comprehensive, hands-on educational initiative designed to provide students with practical experience in building advanced data systems. This project targets specific skills in database management, information retrieval, and system architecture.

Our goal is to bridge the gap between theoretical knowledge and real-world implementation. You will not just learn concepts; you will build them.

---

## Project Components

The current curriculum consists of three projects:

1.  **KiteSQL**  
    Focuses on mastering SQL queries, schema design, and database interaction using MySQL. You will act as a DBA managing a complex dataset.
    
2.  **KiteRAG**  
    Dive into the world of AI with Retrieval-Augmented Generation. You will build a system that retrieves relevant information to ground LLM responses, learning about vector databases and semantic search.

3.  **KiteDB**  
    The capstone project where you implement core database internals. This involves understanding storage engines and query processing.

---

## Kite Project Workflow

<p align="center">
  <img src="Figures/workflow.png" alt="Kite Project Workflow" width="70%">
</p>

The overall workflow follows these key steps:
1.  **Invitation**: Accept the assignment invitation via GitHub Classroom to get your private repository.
2.  **Clone and Implement**: Clone your private repository to the Kcloud environment. Implement your code according to the instruction. You can test your code locally using the provided scripts.
3.  **Submit**: Push your code. GitHub Actions will automatically run the grading scripts in the KiteJudge server.
4.  **Grade and Compete**: Check your scores and rankings on KiteBoard and win awards.

---

## Platform & Access

We utilize GitHub Classroom for all assignment distribution and submission. 

- **Invitation Link**: The official invitation link will be posted on KLMS. 

- **Privacy Rules**: 
    - 🚫 **Do NOT share the invitation link.** It is for enrolled students *only*.
    - 🚫 **Do NOT Fork or Publicize.** Your repository must remain private. Publicly forking the repository or sharing your code is a violation of academic integrity.


You must complete the following steps to finish the invitation:
1. Click the invitation link
2. Get access approval via email
3. Enter your personal repository

<p align="center">
  <img src="Figures/platform.png" alt="Platform Example">
</p>

---

## Repository Structure

The project repository is organized to separate documentation, source code, and operational scripts.

### `docs/` — Documentation
*   **`instruction.md`**: The primary guide for each project. **Start here.** It lists every task you need to complete.
*   **Supplementary Materials**: Additional `*.md` files may be provided to explain complex concepts or API usage.

### `src/` — Source Code
*   This is your workspace.
*   You will find placeholders marked with `/* task */`.
*   **Rule**: You can only modify the code file containing that specific task block. Modifications to infrastructure code outside this block will not be reflected in grading.

### `scripts/` — Helper Scripts
We provide a suite of shell scripts to automate common tasks. run these from the project root (e.g., `./scripts/init.sh`).

*   **`init.sh`**: Sets up your local environment. Installs necessary compilers, Python libraries, and other dependencies.
*   **`setdb.sh`**: Initializes the database container. It sets up schemas and populates initial data.
*   **`run.sh`**: Executes the main application. Use this to see your code in action.
*   **`test.sh`**: Runs local test cases. This gives you an estimated correctness score.
*   **`submit.sh`**: Validates and pushes your `master` branch code to the `submit` branch for official grading.

### `.github/workflows/` — CI/CD
*   **`submission.yml`**: Defines the GitHub Actions pipeline.
*   **Automation**: Every hour, this workflow sends the code from your `submit` branch to the **KiteJudge** server for evaluation.

---

## Evaluation: Competition & Awards

We believe in healthy competition to drive optimization and excellence.

### 1. Correctness Score
*   **Definition**: Points awarded for passing functional test cases.
*   **How to check**: Run `scripts/test.sh`. (Note: Local tests are indicative; KiteJudge server tests are final).
*   **Distribution**:
    - KiteSQL: **100 pts**
    - KiteRAG: **50 pts**
    - KiteDB: **50 pts**

### 2. Competition Score
*   **Definition**: Additional points earned based on the **accuracy** and **efficiency** (speed/memory) of your solution compared to your peers.
*   **Distribution**:
    - KiteSQL: **0 pts** (Functional only)
    - KiteRAG: **50 pts** (Performance matters!)
    - KiteDB: **50 pts** (Optimization is key!)

### 3. Final Scoring & Leaderboard
*   **KiteJudge**: The automated grading server evaluates submissions from the `submit` branch.
*   **KiteBoard**: A live leaderboard showing current rankings (Accuracy, Efficiency). Names are anonymized to protect privacy.
*   **Grading Timeline**: Rankings update every hour. Final scores are graded and posted after the deadline.

<p align="center">
  <img src="Figures/leaderboard.png" alt="Leaderboard Example" width="80%">
</p>

### Awards
Outstanding students who are in top 3 of the leaderboards or demonstrate exceptional engineering quality will be awarded **Bonus Points** at the end of the semester.

---

*Good luck, and happy coding!*
