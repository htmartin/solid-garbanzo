### **Weekly Learning Objectives**

By the end of this week, students will be able to:

1. Navigate the file system using command-line tools, including creating, modifying, and removing files and directories.
2. Explain the layered architecture of a computer and describe the roles of the operating system and applications in managing files and executing programs.
3. Demonstrate proficiency with foundational Bash commands for file and directory manipulation and utilize these in data workflows.
4. Set up and use Git for version control, including creating repositories, committing changes, and collaborating via GitHub.
5. Compare Python’s syntax and constructs with other programming languages, appreciating its readability and versatility for data science applications.

---

#### **1. File System Navigation**
- **Question**: What is the difference between absolute and relative paths? Give an example of each.  
  **Answer**:  
  - **Absolute path**: A path that starts from the root directory and provides the full directory structure to a file or folder (e.g., `/home/user/documents/file.txt`).  
  - **Relative path**: A path relative to the current working directory (e.g., `documents/file.txt` if the current directory is `/home/user`).

#### **2. Computer Architecture**
- **Question**: Describe the role of the operating system in managing files and executing programs.  
  **Answer**:  
  The operating system acts as an intermediary between hardware and software. It manages hardware resources, organizes files into a hierarchical structure, and allocates resources to applications for program execution.

#### **3. Bash Commands**
- **Question**: What does the following sequence of Bash commands do?  
  ```
  mkdir my_project
  cd my_project
  touch data.csv
  ls
  ```  
  **Answer**:  
  - `mkdir my_project`: Creates a directory named `my_project`.  
  - `cd my_project`: Changes the current directory to `my_project`.  
  - `touch data.csv`: Creates an empty file named `data.csv` inside `my_project`.  
  - `ls`: Lists the contents of `my_project`, which now includes `data.csv`.

#### **4. Version Control with Git**
- **Question**: Explain the difference between `git add` and `git commit`.  
  **Answer**:  
  - `git add`: Stages changes to be included in the next commit.  
  - `git commit`: Records the staged changes in the repository's history with a message describing the changes.

#### **5. Python Syntax and Constructs**
- **Question**: Compare Python’s syntax for defining a list with that of a lower-level language like C. Provide an example for both.  
  **Answer**:  
  - **Python**:  
    ```python
    my_list = [1, 2, 3, 4]
    ```  
    Python uses simple square brackets to define a list, and the language handles memory management automatically.  
  - **C**:  
    ```c
    int my_list[] = {1, 2, 3, 4};
    ```  
    In C, lists (arrays) require specifying the data type and initializing elements explicitly.

