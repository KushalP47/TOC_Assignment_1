# NFA to DFA Conversion and Minimization

This project provides a tool to convert a Non-deterministic Finite Automaton (NFA) to a Deterministic Finite Automaton (DFA) and minimize the resulting DFA. It includes scripts to generate graphical representations of the DFA and the minimized DFA.

## Project Structure

- `convert_nfa_to_dfa.py`: Contains the function to convert NFA to DFA.
- `minimize_dfa.py`: Contains the function to minimize the DFA.
- `generate_graph.py`: Generates graphical representations of the DFA and minimized DFA.
- `testcases/`: Contains subfolders with test cases for the conversion and minimization.

## Setup

1. **Clone the Repository**

    ```bash
    git clone <repository-url>
    cd <repository-directory>
    ```

2. **Install Required Packages**

    Ensure you have Python installed, then install the required packages using `pip`:

    ```bash
    pip install graphviz
    ```

3. **Directory Structure**

    The `testcases` directory should contain subfolders named `testcase-1`, `testcase-2`, etc., each containing:
    - `input.txt`: Contains the NFA description.
    - `dfa_image.png`: Output image for the DFA.
    - `minimized_dfa_image.png`: Output image for the minimized DFA.

## Usage

1. **Prepare Your Test Cases**

    Create subfolders inside the `testcases` directory for each test case. Each subfolder should include an `input.txt` file formatted as follows:

    ```
    States: {q0, q1, q2}
    Alphabet: {0, 1}
    Start State: q0
    Accept States: {q2}
    Transitions:
    q0 -> 0 -> q0
    q0 -> 1 -> q0, q1
    q1 -> 1 -> q2
    ```

2. **Run the Script**

    Execute the `AU2140105_Assignment_1.ipynb` script to process all test cases

    This script will:
    - Read `input.txt` from each test case folder.
    - Convert the NFA to DFA.
    - Minimize the DFA.
    - Generate graphical representations of both DFA and minimized DFA.
    - Save the images (`dfa_image.png` and `minimized_dfa_image.png`) in the respective test case folders.

## Example

Here’s an example of how the output will be structured:

**Input (`testcases/testcase-1/input.txt`):**
``` plaintext
States: {q0, q1, q2} 
Alphabet: {0, 1} 
Start State: q0 
Accept States: {q2} 
Transitions: 
q0 -> 0 -> q0 
q0 -> 1 -> q0, q1 
q1 -> 1 -> q2
```


**Generated Output:**

- `testcases/testcase-1/dfa_image.png`: Graphical representation of the DFA.
- `testcases/testcase-1/minimized_dfa_image.png`: Graphical representation of the minimized DFA.

