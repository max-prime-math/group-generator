# group-generator
Generate random groups based on fair grades.

Access here: https://max-prime-math.github.io/group-generator/generator.html

A privacy-focused, client-side web application designed for educators to create student groups with equalized grade averages. This tool uses a stratified sampling approach combined with a hill-climbing optimization algorithm to ensure every group is mathematically balanced.

## Features

### 1. Stratified Grouping Logic
The algorithm prevents "clustering" of similar performance levels by dividing the student list into three tiers (High, Middle, and Low). Groups are initially formed by selecting one student from each tier, ensuring a diverse range of abilities in every group.

### 2. Hill-Climbing Optimization
To achieve the narrowest possible margin between group averages, the tool performs 2,000 stochastic swaps post-grouping. 
* It identifies the "Score Spread" (difference between the highest and lowest group average).
* It attempts to swap students between groups.
* It retains the swap only if the global spread is reduced.



### 3. Presentation Mode
Designed for screen-sharing in a classroom environment, the **Presentation Mode** hides:
* The raw data input area.
* Individual student grades.
* Group average labels and values.

### 4. Triple-Layer Anonymization
To protect student self-esteem and prevent "ranking" identification:
* **Bucket Shuffling:** Initial pairings are randomized within their tiers.
* **Internal Shuffling:** The order of names within a group card is randomized.
* **Group Order Shuffling:** The final sequence of groups is randomized so "Group 1" carries no specific mathematical weight.

---

## Technical Specifications

* **Language:** HTML5, CSS3, Vanilla JavaScript (ES6).
* **Dependencies:** None.
* **Privacy:** 100% client-side. No data is sent to a server; all processing happens in the local browser memory.
* **Input Compatibility:** Supports Tab-separated values (direct copy-paste from Excel/Google Sheets) and space-separated values.

---

## How to Use

### Installation
1. Save the provided HTML code as `index.html`.
2. Open the file in any modern web browser.

### Workflow
1. **Input:** Paste your student names and grades into the text area.
2. **Sort:** Click **Sort & Optimize Groups**. 
3. **Verify:** Review the averages in the default view to ensure the balance is satisfactory.
4. **Export:** Click **Export for Classroom** and use the **Copy Text** button to grab a grade-free list for your LMS.
5. **Present:** Click **Enter Presentation Mode** to hide sensitive data before projecting the groups to the class.

---

## Data Format Example
The tool expects one student per line. Names can include spaces.

| Name | Grade |
| :--- | :--- |
| Jane Doe | 98 |
| John Smith | 85 |
| Sam Baker | 72 |
