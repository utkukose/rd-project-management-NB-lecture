<div align="center">

# Week 13: Research Teams, Open Science and FAIR Data

**R&D and Project Management in Computer Science (11117BLG002)**  
Prof. Dr. Utku Kose, Süleyman Demirel University

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/utkukose/rd-project-management-NB-lecture/blob/main/weeks/week-13/NB13_teams_open_science.ipynb) [![Interactive lab](https://img.shields.io/badge/interactive%20lab-open-1D5B78)](https://utkukose.github.io/rd-project-management-NB-lecture/weeks/week-13/lab.html) [![Lecture notes](https://img.shields.io/badge/lecture%20notes-PDF-566A73)](Week13_Lecture_Notes.pdf) [![Course home](https://img.shields.io/badge/course-home-B97813)](../../README.md)

</div>

## Overview

Research is done by teams, and its results are increasingly expected to be open and reusable. This week examines what is known about research teams and their dynamics, the attribution of contributions, and the practices of open science and FAIR data management that funders now expect [1, 2, 3].

**Estimated study time:** 6 to 8 hours.

## Learning outcomes

By the end of the week, students are expected to discuss evidence on team size and team dynamics and to attribute contributions with the CRediT taxonomy. They should also be able to apply open science and FAIR principles to a project and to draft a data management plan.

## Study path

| Step | Activity | Suggested time |
|---|---|---|
| 1 | Read the lecture below or the [PDF version](Week13_Lecture_Notes.pdf) | 90 minutes |
| 2 | Explore the [interactive lab](https://utkukose.github.io/rd-project-management-NB-lecture/weeks/week-13/lab.html) | 45 minutes |
| 3 | Work through the [Colab notebook](https://colab.research.google.com/github/utkukose/rd-project-management-NB-lecture/blob/main/weeks/week-13/NB13_teams_open_science.ipynb) and its exercises | 2 to 3 hours |
| 4 | Take the self-assessment in the interactive lab (tab: Check yourself) | 20 minutes |
| 5 | Answer the reflection prompts in the interactive lab, export the learning log and complete the weekly task | 60 minutes |

## Week at a glance

```mermaid
flowchart LR
  T["Team size: large teams develop, small teams disrupt"] --> D["Dynamics: forming to performing, psychological safety"]
  D --> C["Credit: CRediT roles"]
  O["Open science: TOP standards"] --> G["Good enough computing practices"]
  F["FAIR principles"] --> DMP["Data management plan"]
  G --> DMP
```

## Lecture

### Teams in research

Wuchty, Jones and Uzzi analysed millions of papers and patents [1]. They found that teams increasingly dominate the production of knowledge across fields and that team-authored work tends to receive more citations. Wu, Wang and Evans added an important qualification: Large teams tend to develop existing science and technology, while small teams tend to disrupt it with new ideas and opportunities [4]. The size and composition of a project team therefore affect not only how much it can do but what kind of work it is likely to produce.

<details>
<summary><b>Check your understanding.</b> What did Wuchty and colleagues find about teams in science?</summary>

A. Solo authors produce most highly cited work  
B. Teams increasingly dominate knowledge production and produce more highly cited work  
C. Team size has not changed  
D. Teams publish less  

**Answer: B.** Later work showed that smaller teams tend to disrupt and larger teams tend to develop existing ideas.

</details>

### Team dynamics

Tuckman reviewed studies of small groups and proposed a developmental sequence that later became known as forming, storming, norming and performing [5]. New project teams need time to settle roles and norms before they perform, which is one reason why the first months of a project are often slower than planned. Edmondson showed that psychological safety, a shared belief that the team is safe for interpersonal risk-taking, supports learning behaviour in teams, such as asking questions, seeking feedback and discussing errors [6]. In research, where errors and negative results are part of the work, this matters directly for quality. Clear attribution also prevents conflict. Allen and colleagues proposed a taxonomy of contributor roles [7]. The resulting CRediT taxonomy distinguishes 14 roles, from conceptualisation and methodology to software, supervision and writing.

<details>
<summary><b>Check your understanding.</b> What is psychological safety in a team?</summary>

A. A shared belief that the team is safe for interpersonal risk taking  
B. Insurance against accidents  
C. A security clearance  
D. Strict hierarchy  

**Answer: A.** Teams with psychological safety report errors and learn from them more readily.

</details>

### Open science

Nosek and colleagues proposed the Transparency and Openness Promotion guidelines, eight standards for journals and funders [2]. The standards cover citation of data and code, transparency of data, code, materials and design, preregistration of studies and analysis plans, and replication. Each standard has increasing levels of stringency. Wilson and colleagues described good enough practices in scientific computing for researchers without specialised training [8]. The practices include saving raw data, writing code in small documented functions, using version control and recording how every result was produced. For computing projects, these practices overlap with the reproducibility requirements discussed in Week 2.

<details>
<summary><b>Check your understanding.</b> Which is NOT usually counted among open science practices?</summary>

A. Open access publication  
B. Sharing data  
C. Preregistration  
D. Keeping analysis code private until all papers are published  

**Answer: D.** Open code is part of open science, and delaying it limits verification.

</details>

### FAIR data and data management plans

Wilkinson and colleagues formulated the FAIR guiding principles: Data and metadata should be findable, accessible, interoperable and reusable, by machines as well as by people [3]. Figure 13.1 summarises them. FAIR does not mean open: Personal data may have restricted access and still be FAIR, if their metadata are findable and the conditions of access are clear. Many funders, including the European Commission in Horizon Europe, expect projects that generate or reuse data to maintain a data management plan. The plan describes the data, formats, metadata, repositories, licences, access, preservation and responsibilities. The interactive lab provides a FAIR self-assessment, a template for a data management plan and a builder for CRediT statements.

> **Pause and reflect.** Which dataset produced in your project would be the hardest to make FAIR, and why?

![The FAIR guiding principles for scientific data management and stewardship, in brief.](figures/w13_fig1.png)

*Figure 13.1. The FAIR guiding principles for scientific data management and stewardship, in brief [3].*

<details>
<summary><b>Check your understanding.</b> What does FAIR stand for?</summary>

A. Fast, accurate, inexpensive, reliable  
B. Findable, accessible, interoperable, reusable  
C. Funded, approved, indexed, reviewed  
D. Free, anonymous, instant, recorded  

**Answer: B.** FAIR does not require data to be open, but it requires clear conditions of access.

</details>

## Interactive lab

Part A assesses a dataset against the FAIR principles. Part B drafts a data management plan and downloads it as a Markdown file. Part C builds a contribution statement with the CRediT roles [3, 7].

[Open the interactive lab](https://utkukose.github.io/rd-project-management-NB-lecture/weeks/week-13/lab.html)

![Screenshot of the Week 13 interactive lab](screenshots/lab.png)

## Colab notebook

The Colab notebook validates a metadata record against required fields, verifies file integrity with checksums and records the computing environment, three small practices that make data and results reusable [3, 8].

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/utkukose/rd-project-management-NB-lecture/blob/main/weeks/week-13/NB13_teams_open_science.ipynb)

Screenshots of the executed Colab notebook:

![Output 1 of the Week 13 Colab notebook](screenshots/nb_1.png)

## Self-assessment and reflection

The interactive lab contains a self-assessment of six questions (tab: Check yourself). Students answer each question, state how sure they are and receive instant feedback. A confident but wrong answer marks the first topic to revisit. The reflection prompts below also appear in the interactive lab (tab: Reflect and submit). Answers written there are saved in the browser and can be exported as a learning log.

1. Which stage of team development is your research group in, and what would help it move on?
2. Write the CRediT statement for your most recent paper. Did it reveal any contributions that the author list does not show?
3. Which data of your project must remain restricted, and how can they still be made FAIR?

## Weekly task and submission

**What to do.** Complete the data and team parts of your proposal. First, write the data management plan of your project with the template of the interactive lab. Second, complete a FAIR self-assessment for its main data set. Third, add a team section to your proposal with the roles of the members, a plan for CRediT contribution statements in publications and measures that support psychological safety.

**Where to look.** Lecture: sections "Team dynamics", "Open science" and "FAIR data and data management plans". Interactive lab: Part A for the FAIR self-assessment, Part B for the data management plan and Part C for the CRediT statement. Colab notebook: Section 1 for metadata, Section 2 for checksums and Section 3 for a record of the run.

**Example.** A data set of annotated, anonymised posts could be deposited in Zenodo with a DOI, a licence and a README that describes the annotation guidelines. This makes the data findable and reusable. A measure for psychological safety could be a monthly meeting in which failed experiments are presented without blame.

**What to submit.** The data management plan, the FAIR self-assessment and the team section, and the Colab notebook with Exercises 1 and 2 completed.

The weekly task supports self-learning and builds a personal portfolio. In an active semester, students who follow the course with the instructor can send their work for evaluation to utkukose@sdu.edu.tr or utkukose@gmail.com. The e-mail contains the items that the task lists under What to submit. It also includes the learning log exported from the interactive lab (tab: Reflect and submit).

## Research and report assignment (optional)

**Team science and open practices in computing.** How do team size and open science practices affect computing research?

**What to do.** Review the evidence on team size, team composition and open science practices in computing research [1, 2, 4]. Assess their implications for project design.

**Where to start.** Lecture sections "Teams in research" and "Open science".

**Example focus.** Wu and colleagues found that small teams tend to disrupt science and technology, while large teams tend to develop them [4]. The report could ask what this means for staffing a funded project.

This research assignment is optional and supports self-learning. In an active semester, students who follow these weeks with the instructor can send the report for evaluation to utkukose@sdu.edu.tr or utkukose@gmail.com. The report has 1500 to 2500 words and follows the structure of an academic paper. It cites at least six scholarly or official sources in square brackets and ends with a reference list. The [report template](https://github.com/utkukose/rd-project-management-NB-lecture/blob/main/exams/REPORT_TEMPLATE.md) shows a suitable structure.

## References

[1] Wuchty, S., Jones, B. F., & Uzzi, B. (2007). The increasing dominance of teams in production of knowledge. *Science*, 316(5827), 1036-1039. <https://doi.org/10.1126/science.1136099>

[2] Nosek, B. A., Alter, G., Banks, G. C., et al. (2015). Promoting an open research culture. *Science*, 348(6242), 1422-1425. <https://doi.org/10.1126/science.aab2374>

[3] Wilkinson, M. D., Dumontier, M., Aalbersberg, I. J., et al. (2016). The FAIR Guiding Principles for scientific data management and stewardship. *Scientific Data*, 3, 160018. <https://doi.org/10.1038/sdata.2016.18>

[4] Wu, L., Wang, D., & Evans, J. A. (2019). Large teams develop and small teams disrupt science and technology. *Nature*, 566(7744), 378-382. <https://doi.org/10.1038/s41586-019-0941-9>

[5] Tuckman, B. W. (1965). Developmental sequence in small groups. *Psychological Bulletin*, 63(6), 384-399. <https://doi.org/10.1037/h0022100>

[6] Edmondson, A. (1999). Psychological safety and learning behavior in work teams. *Administrative Science Quarterly*, 44(2), 350-383. <https://doi.org/10.2307/2666999>

[7] Allen, L., Scott, J., Brand, A., Hlava, M., & Altman, M. (2014). Publishing: Credit where credit is due. *Nature*, 508(7496), 312-313. <https://doi.org/10.1038/508312a>

[8] Wilson, G., Bryan, J., Cranston, K., Kitzes, J., Nederbragt, L., & Teal, T. K. (2017). Good enough practices in scientific computing. *PLOS Computational Biology*, 13(6), e1005510. <https://doi.org/10.1371/journal.pcbi.1005510>

---

<sub>R&D and Project Management in Computer Science. Prof. Dr. Utku Kose, Süleyman Demirel University. ORCID [0000-0002-9652-6415](https://orcid.org/0000-0002-9652-6415). Content licensed under CC BY 4.0. This course is updated in line with current developments in the field. First version: September 2026. Last update: October 2026.</sub>
