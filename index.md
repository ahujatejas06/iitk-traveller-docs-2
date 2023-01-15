---
title: Home
layout: home
nav_order: 0
---

# About the Language
IITK - Traveller is an esoteric language designed by Programming Club,IIT Kanpur. Started as a fun winter project, the construct of the language is partially inspired by esolangs 3var and Taxi, and its major goal is to introduce IITK peeps to esolangs and provide them with a relatable, challenging and creative construct, in case they have been bored using the similar language constructs like C/C++,Java,Python etc.

# Overview
The language consists of a memory tape which is an integer array(namely mem[]), of length 2048. There are 4 variables in this language
- **mem_1** - memory pointer in the tape
- mem_2 - memory pointer in the tape
- mem_3 - memory pointer in the tape
- cond - represents the condition variable

The last of the variables represents a condition variable, which can intake any integer value. The IITK landmarks will represent the supported commands. As per the language construct, the execution will travel from one landmark to the other depending on the current value of condition variable.

# Syntax

Each command consists of 3 comma-separated tokens ended with a newline.

- Starting Landmark
- Condition Value
- Finishing Landmark

## Example

# Theme
A traveller, with the help of 4 boxes + book in his/her bag, wishes to travel IITK in order to reach to their final destination. They also wish that their journey is meaningful, so they want to leave their token of visit as an output after they have finished travelling. You, being familiar with IITK have to help them by planning their journey through landmarks of IITK while making use of the boxes and the book to help them accomplish their task.

# Execution Flow
The execution flow can be visualized as traversing a graph following its edges. The execution will start at the **start** node and will end as soon as the traveller reaches the **finish** node. Therefore each command represents a directed edge in the graph from the starting landmark to the finishing landmark. The condition value specifies which edge to be traversed from a particular node. Only the commands with condition value equal to the value of cond will be available to follow.

If there is no valid path available, an error will be returned. The start and finish node must be present in the code otherwise an error will be generated.

# Meaning of different landmarks
## Commands and Expressions


| IITK LANDMARK           |          COMMAND |
| start                   |          start |
| finish                  |          finish |
| iit_gate_in_1           |          input to mem[mem_1] |
| iit_gate_in_2           |          input to mem[mem_2] |
| hall_2                  |          mem[mem_3] = mem[mem_1] + mem[mem_2] |
| hall_3                  |          mem[mem_3] = mem[mem_1] * mem[mem_2] |
| hall_5                  |          mem[mem_3] = mem[mem_1] - mem[mem_2] |
| hall_12                 |          mem[mem_3] = mem[mem_1] / mem[mem_2] |
| mt_1_3                  |          mem[mem_1] = mem[mem_3] |
| mt_3_1                  |          mem[mem_3] = mem[mem_1] |
| mt_2_3                  |          mem[mem_2] = mem[mem_3] |
| mt_3_2                  |          mem[mem_3] = mem[mem_2] |
| iit_gate_out_1          |          output mem[mem_1] |
| iit_gate_out_2          |          output mem[mem_2] |
| lecture_hall_gt         |          mem[mem_1] > mem[mem_2] |
| lecture_hall_gt_t       |          path followed if lecture_hall_gt is true |
| lecture_hall_gt_f       |          path followed if lecture_hall_gt is false |
| lecture_hall_lt         |          mem[mem_1] < mem[mem_2] |
| lecture_hall_lt_t       |          path followed if lecture_hall_lt is true |
| lecture_hall_lt_f       |          path followed if lecture_hall_lt is false |
| lecture_hall_eq         |          mem[mem_1] == mem[mem_2] |
| lecture_hall_eq_t       |          path followed if lecture_hall_eq is true |
| lecture_hall_eq_f       |          path followed if lecture_hall_eq is false |
| oat_stairs_1            |          mem[mem_1]++ |
| oat_stairs_2            |          mem[mem_2]++ |
| oat_stairs_c            |          cond++ |
| southern_labs_1         |          mem[mem_1]-- |
| southern_labs_2         |          mem[mem_2]-- |
| southern_labs_c         |          cond-- |
| hall_13_1               |          mem[mem_1] = 0 |
| hall_13_2               |          mem[mem_2] = 0 |
| hall_13_3               |          mem[mem_3] = 0 |
| hall_13_c               |          cond = 0
| rm_1                    |          mem_1++
| rm_2                    |          mem_2++
| rm_3                    |          mem_3++
| kd_1                    |          mem_1--
| kd_2                    |          mem_2--
| kd_3                    |          mem_3--
