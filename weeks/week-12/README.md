<div align="center">

# Week 12: Monitoring and Control: Earned Value Management and Reporting

**R&D and Project Management in Computer Science (11117BLG002)**  
Prof. Dr. Utku Kose, Süleyman Demirel University

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/utkukose/rd-project-management-NB-lecture/blob/main/weeks/week-12/NB12_earned_value.ipynb) [![Interactive lab](https://img.shields.io/badge/interactive%20lab-open-1D5B78)](https://utkukose.github.io/rd-project-management-NB-lecture/weeks/week-12/lab.html) [![Lecture notes](https://img.shields.io/badge/lecture%20notes-PDF-566A73)](Week12_Lecture_Notes.pdf) [![Course home](https://img.shields.io/badge/course-home-B97813)](../../README.md)

</div>

## Overview

Monitoring answers two questions: Is the project where it should be, and where will it end? This week introduces earned value management, which combines scope, schedule and cost in one set of measures, and its use in the reporting of funded projects [1, 2].

**Estimated study time:** 6 to 8 hours.

## Learning outcomes

By the end of the week, students are expected to compute planned value, earned value and actual cost, and to derive schedule and cost variances and performance indices. They should be able to forecast the cost at completion with several methods. Finally, they should be able to choose suitable methods for measuring the progress of research tasks.

## Study path

| Step | Activity | Suggested time |
|---|---|---|
| 1 | Read the lecture below or the [PDF version](Week12_Lecture_Notes.pdf) | 90 minutes |
| 2 | Explore the [interactive lab](https://utkukose.github.io/rd-project-management-NB-lecture/weeks/week-12/lab.html) | 45 minutes |
| 3 | Work through the [Colab notebook](https://colab.research.google.com/github/utkukose/rd-project-management-NB-lecture/blob/main/weeks/week-12/NB12_earned_value.ipynb) and its exercises | 2 to 3 hours |
| 4 | Take the self-assessment in the interactive lab (tab: Check yourself) | 20 minutes |
| 5 | Answer the reflection prompts in the interactive lab, export the learning log and complete the weekly task | 60 minutes |

## Week at a glance

```mermaid
flowchart LR
  B["Baseline: scope, schedule, cost"] --> PV["Planned value"]
  W["Work performed"] --> EV["Earned value"]
  C["Costs incurred"] --> AC["Actual cost"]
  PV --> I["SPI = EV / PV"]
  EV --> I
  EV --> J["CPI = EV / AC"]
  AC --> J
  J --> F["Forecasts: EAC, VAC, TCPI"]
```

## Lecture

### Baselines and variances

Control requires a baseline: the approved plan of scope, schedule and cost against which performance is measured. Reporting that lists costs spent and tasks started says little about performance, because it does not relate the money spent to the work accomplished. Earned value management was developed to make this relation explicit, and it is described in a standard of the Project Management Institute and in the textbook of Fleming and Koppelman [1, 2].

<details>
<summary><b>Check your understanding.</b> What is earned value?</summary>

A. The money received from the funder  
B. The budgeted cost of the work actually performed  
C. The actual cost incurred  
D. The planned cost of all work  

**Answer: B.** Comparing earned value with planned value and actual cost reveals schedule and cost variances.

</details>

### The three measures

Planned value (PV) is the budgeted cost of the work scheduled up to the status date. Earned value (EV) is the budgeted cost of the work actually performed. Actual cost (AC) is the cost actually incurred for that work. From these, the schedule variance is EV minus PV and the cost variance is EV minus AC. The schedule performance index SPI is EV divided by PV, and the cost performance index CPI is EV divided by AC. An index below one signals a problem. In the example of Figure 12.1, a 12-month project has a budget of 240 thousand euro. At month 6, the planned value is 96, the earned value 84 and the actual cost 105, so SPI is 0.875 and CPI is 0.8. The project is behind schedule and over budget.

![Planned value, earned value and actual cost of the example project at month 6.](figures/w12_fig1.png)

*Figure 12.1. Planned value, earned value and actual cost of the example project at month 6 [1].*

<details>
<summary><b>Check your understanding.</b> A project has an earned value of 80 and an actual cost of 100. What does the cost performance index show?</summary>

A. CPI 1.25, under budget  
B. CPI 0.8, over budget  
C. CPI 0.8, ahead of schedule  
D. CPI 20, on budget  

**Answer: B.** CPI = EV / AC = 0.8, so each unit spent produced 0.8 units of planned work.

</details>

### Forecasting the end

The budget at completion (BAC) is the total planned budget. If the current cost efficiency continues, the estimate at completion is EAC = BAC / CPI, 300 thousand euro in the example. If the overrun was a one-off event and future work will proceed as planned, EAC = AC + (BAC - EV), which gives 261. If both cost and schedule performance influence the remaining work, EAC = AC + (BAC - EV) / (CPI x SPI), which gives about 328. The variance at completion is BAC minus EAC. The to-complete performance index, (BAC - EV) / (BAC - AC), states the cost efficiency that the remaining work would need to finish within budget. A to-complete index well above the current CPI indicates an unrealistic plan. The choice among forecasts is a judgement about the causes of the variance, not a matter of arithmetic.

<details>
<summary><b>Check your understanding.</b> With a budget at completion of 500 and a CPI of 0.8, what is the estimate at completion if the current efficiency continues?</summary>

A. 400  
B. 500  
C. 580  
D. 625  

**Answer: D.** EAC = BAC / CPI = 500 / 0.8 = 625.

</details>

### Measuring progress in research

The weak point of earned value in research is the measurement of EV itself, because progress on uncertain tasks is hard to estimate and percent-complete judgements tend to be optimistic. Fixed rules reduce the problem. The 0/100 rule credits a task only when it is finished, and the 50/50 rule credits half at the start and half at completion. Linking earned value to deliverables and milestones makes it verifiable. Funders require periodic technical and financial reports, and earned value measures, even computed informally, help a project team to see problems before the reports do. The interactive lab computes all measures for three scenarios, and the Colab notebook reproduces the calculations.

> **Pause and reflect.** Which measure of progress would be most honest for the tasks of your project: percent complete, 0/100 or milestones?

<details>
<summary><b>Check your understanding.</b> Why is progress hard to measure in research?</summary>

A. Outcomes of tasks are uncertain, so percent complete is subjective  
B. Research has no budget  
C. Researchers do not keep records  
D. Progress is always linear  

**Answer: A.** Milestone-based rules, such as counting value only when a milestone is met, reduce subjectivity.

</details>

## Interactive lab

Choose a scenario and a status month. The calculator plots planned value, earned value and actual cost, computes variances and indices and compares three forecasts of the cost at completion [1, 2].

[Open the interactive lab](https://utkukose.github.io/rd-project-management-NB-lecture/weeks/week-12/lab.html)

![Screenshot of the Week 12 interactive lab](screenshots/lab.png)

## Colab notebook

The Colab notebook computes earned value measures month by month for the example project and compares forecasts of the cost at completion [1].

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/utkukose/rd-project-management-NB-lecture/blob/main/weeks/week-12/NB12_earned_value.ipynb)

Screenshots of the executed Colab notebook:

![Output 1 of the Week 12 Colab notebook](screenshots/nb_1.png)

## Self-assessment and reflection

The interactive lab contains a self-assessment of six questions (tab: Check yourself). Students answer each question, state how sure they are and receive instant feedback. A confident but wrong answer marks the first topic to revisit. The reflection prompts below also appear in the interactive lab (tab: Reflect and submit). Answers written there are saved in the browser and can be exported as a learning log.

1. Which scenario in the interactive lab resembles a project you know, and which forecast would you have trusted?
2. How would you measure earned value for a task whose outcome is a negative result?
3. What should a periodic report to a funder contain beyond the numbers of earned value management?

## Weekly task and submission

**What to do.** Define the performance measurement baseline of your project and use it once. First, give the planned value by month and the rule for measuring earned value in each work package, such as the 0/100 rule or milestones. Second, assume a status in the middle of the project, for example a delay in one work package. Compute the variances, the indices and a forecast of the cost at completion. Third, write a status report of half a page.

**Where to look.** Lecture: sections "Baselines and variances", "The three measures", "Forecasting the end" and "Measuring progress in research". Interactive lab: the earned value calculator with its scenarios (tab: Explore). Colab notebook: Section 1 with both exercises.

**Example.** Suppose that a 10-month project has a budget of 200 thousand euro. At month 4, the planned value is 80, the earned value 70 and the actual cost 75, all in thousand euro. Then SPI = 70 / 80 = 0.875 and CPI = 70 / 75, about 0.93. If this cost efficiency continues, the estimate at completion is 200 / (70 / 75), about 214 thousand euro.

**What to submit.** The baseline, the status report, and the Colab notebook with Exercises 1 and 2 completed.

The weekly task supports self-learning and builds a personal portfolio. In an active semester, students who follow the course with the instructor can send their work for evaluation to utkukose@sdu.edu.tr or utkukose@gmail.com. The e-mail contains the items that the task lists under What to submit. It also includes the learning log exported from the interactive lab (tab: Reflect and submit).

## Research and report assignment (optional)

**Earned value for knowledge work.** Is earned value management useful for software development and research?

**What to do.** Review the evidence on the usefulness and limits of earned value management in software development and research [1, 2]. Include the measurement of progress on uncertain tasks.

**Where to start.** Lecture sections "The three measures" and "Measuring progress in research".

**Example focus.** The 0/100 rule avoids optimistic progress reports, but it shows no progress for a long experiment until the experiment ends. The report could compare such rules with measurement based on milestones.

This research assignment is optional and supports self-learning. In an active semester, students who follow these weeks with the instructor can send the report for evaluation to utkukose@sdu.edu.tr or utkukose@gmail.com. The report has 1500 to 2500 words and follows the structure of an academic paper. It cites at least six scholarly or official sources in square brackets and ends with a reference list. The [report template](https://github.com/utkukose/rd-project-management-NB-lecture/blob/main/exams/REPORT_TEMPLATE.md) shows a suitable structure.

## References

[1] Project Management Institute (2019). *The Standard for Earned Value Management*. Project Management Institute.

[2] Fleming, Q. W., & Koppelman, J. M. (2010). *Earned Value Project Management* (4th ed.). Project Management Institute.

---

<sub>R&D and Project Management in Computer Science. Prof. Dr. Utku Kose, Süleyman Demirel University. ORCID [0000-0002-9652-6415](https://orcid.org/0000-0002-9652-6415). Content licensed under CC BY 4.0. This course is updated in line with current developments in the field. First version: September 2026. Last update: October 2026.</sub>
