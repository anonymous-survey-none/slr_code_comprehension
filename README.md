# Code Comprehension for Novice Students: Teaching, Assessment, Tools, and Challenges.

Code comprehension is a fundamental research field in software development, especially in the current context where Large Language Models (LLMs) are transforming programming practices by automatically generating code. 

Through a systematic literature review, this work addresses four central questions: (1) What are the most effective strategies for teaching code comprehension? (2) What methods are used to assess this skill? (3) What tools support this process? (4) What challenges do students face? The methodology used integrates an AI-powered tool to analyze more than 18,000 articles, resulting in a selection of 47 relevant studies.

The reviewed studies highlight the importance of adopting teaching strategies that help students build solid mental models before they begin writing code. Tools that incorporate such instructional strategies are essential to personalize learning and overcome the challenges faced by novice programmers. Evaluation methods are also evolving, moving beyond traditional assessments to include interactive and formative approaches.

This review synthesizes the current state of research and offers recommendations for educators, researchers, and developers of educational tools aimed at fostering code comprehension skills.


# Methodology

<img src="https://raw.githubusercontent.com/anonymous-survey-none/slr_code_comprehension/refs/heads/main/methodology.png" height="400">

### 1 Research Questions
* [RQ1] What are the main teaching strategies for code comprehension in novice students?
* [RQ2] What are the most commonly used assessment methods to evaluate code comprehension in novice students?
* [RQ3] What are the most widely used tools to support code comprehension in novice students?
* [RQ4] What are the main challenges faced by novice students in the process of understanding the code?

### 2 Search String

```
(novice OR CS1 OR introduct* OR student*) AND 
(code OR program* OR algorithm*) AND 
(comprehension OR understand*)
```

* Area: Computer Science
* Fields: Title, abstract, keywords
* Language: English
* Period: 2014 - 2024

### 3 Digital Libraries

| Resume | Links |
| ------------- |:-------------:|
| <img src="https://raw.githubusercontent.com/anonymous-survey-none/slr_code_comprehension/refs/heads/main/extraction.png" height="300"> | [ACM Digital Library](https://dl.acm.org) <br><br> [IEEE](https://ieeexplore.ieee.org) <br><br> [Scopus](https://www.scopus.com) <br><br> [Web of Science](https://mjl.clarivate.com/search-results) |

### 4 Prompt Engineering

The final structure of our prompt included the following components:
* <b>Profile</b>: Definition of the research field (“Computer Science”) and the type of study (“Systematic Literature Review”);
* <b>Context</b>: Clear presentation of the review’s objective, namely “to evaluate code comprehension in novice programming students”;
* <b>Task</b>: Description of what the model must do, i.e. “classify scientific articles relevant to the context”, highlighting:
    * Inclusion criteria;
    * Exclusion criteria;
    * Classification guidelines.
* <b>Evaluated Study</b>: Presentation of the title, abstract, and keywords of the study being evaluated;
* <b>Response Format</b>: Specification of the desired output. If the article is positively classified, the model must explain the reason; otherwise, it should respond only with “NO”.

### 4.1 Final prompt

```
You are a researcher **in the field of computer science** and are conducting a **systematic review**.

# 1) Context of the Systematic Review
Analyze the process of understanding codes written in a programming language by beginner students of technology courses. 
The objective is to evaluate the ability of these students to **read a code** written in a programming language and achieve (some or all) of the following skills:
- Understand its structure by identifying and relating elements, such as: variables, commands, control structures, character strings and functions;
- Deduce the purpose of the code;
- Detect syntactic and semantic errors;
- Predict the result of code execution;
- Analyze the clarity, efficiency and readability of the code (considering variable names, organization and comments);
- Demonstrate the ability to use the basic concepts learned to modify or create new codes.

# 2) The Task:
Classify scientific articles (analyzing the title and abstract) according to the inclusion and exclusion criteria defined below.

## 2.1) Inclusion Criteria:
Studies that:
- Have an objective EXPLICITLY related to the research scenario defined in this systematic review;
- Use traditional quantitative (tests, metrics) or qualitative (interviews, questionnaires) methods must be classified **positively**.

## 2.2) Exclusion Criteria:
Studies that address at least one of the following points must be classified **negatively**:
- Have an exclusive focus on advanced students or professionals;
- Explore programming concepts that are not part of an introductory programming course;
- Deal with the Object-Oriented Programming paradigm (focusing on classes, objects, encapsulation, polymorphism, inheritance, etc.);
- Analyze programming for databases (e.g., SQL);
- Using games or animations as a teaching method without emphasizing code comprehension;
- Investigating visual programming tools (such as: Scratch, Blockly);
- Analyzing the use of eye-tracking;
- Evaluating only the usability of IDEs;
- Focusing on understanding the requirements of the problem to be solved;
- Evaluating specific aspects of certain programming languages;
- Analyzing computational thinking in a generic way.

## 2.3) Classification Instructions:
- If the article **meets the inclusion criteria** and does not present any exclusion criteria, it should be classified positively;
- If the article **presents any exclusion criteria** or insufficient information for evaluation, it should be classified negatively.

# 3) Article Information:
## 3.1) Title (in English):
{}

## 3.2) Abstract (in English):
{}

# 4) Your mission:
Analyze the information provided about the article and classify it according to the inclusion and exclusion criteria defined above. 
Explicitly return only the word "NO" if the article is negatively classified. 
For articles classified positively, present a brief summary (1 paragraph) about the objective of this evaluated article.
```

### 5 AI Analysis

Using the specified prompt, a Python script analyzed all papers indexed in the digital libraries.
- [ChatGPT] https://platform.openai.com/docs/api-reference
- [Gemma2 with Ollama] https://www.ollama.com/library/gemma2

ChatGPT performed 6 times better than Gemma2.

### 6 Researcher Analysis

This study makes several key contributions to the understanding of code comprehension among novice programming students:

- <b>Teaching Strategies</b>: It consolidates proven strategies such as code tracing, self-explanation, and reading aloud that help beginners build strong mental models before writing code.
- <b>Supporting Tools</b>: It identifies tools that support these strategies and help manage the challenges of teaching in large and diverse classrooms.
- <b>Assessment Methods</b>: It reviews and compares different methods to evaluate code comprehension objectively, highlighting the benefits of combining multiple approaches for a more comprehensive assessment.
- <b>Subjective Factors</b>: It draws attention to important but often overlooked factors—such as motivation, emotional state, and social influences—that impact students' ability to understand code.
- <b>Future Directions</b>: It suggests the need for future research to bridge the gap between theory and classroom practice by integrating subjective factors with effective methodologies and emerging technologies (IA).


`Further details will be made available in this software repository upon acceptance of the corresponding paper.`
