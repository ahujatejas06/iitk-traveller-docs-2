---
title: Home
layout: home
nav_order: 0
---
# Introduction
You are a traveller who has just entered the magical land of IIT Kanpur. Like any tourist, you have no idea of the locals or the surroundings, but luckily you came prepared. H.R Kadim has bestowed upon you some magical items - three books, a dictionary, a compass, and a mysterious box. Using these you must navigate IIT Kanpur, to make your travels memorable, and leave a token of your journey at the end of your journey, the output of your travels. The items also come with a set of instructions on how to use them, given below.

- **Books** - *During a journey each traveller comes upon with much to learn and to share with others upon their return. Take with you these magical books, that can store any and all information you wish to choose in your travels, but beware, as the books are magic, only the correct place will grant the book the power to perform the particular action you wish it to do*
- **Compass** - *Each and every being in this world requires a compass to guide them in their lives. This requirement of guidance is even more so apparent for a traveller of the realms like you. Take care of this box, and review it's contents whenever you wish, and it will guide you towards the next step in your journey* 
- **Dictionary** - *You are entering a strange and unfamiliar place, and require a method to make sense of your surroundings. This dictionary will translate the names of each place in the land of IIT Kanpur and tell you about the power that is contained in that place. Use it whenever you wish to accomplish a specific task, and it will never fail you*
- **Mysterious box** -  *Wise men suggest to always plan your travels before you set out, as an unplanned traveller is likely to get lost, not a situation one wants to entertain in a place where leopards and snakes roam about. Therefore you develop a plan for your travels using the rest of your tools, and once you do, share your plans with this box, and it will tell you the outcome of your journey, and generate the token you wish to leave behind*

Armed with your items, you take out your bicycle and decide to start planning your travel. 

# Overview
## Syntax
Each command consists of 3 comma-separated tokens ended with a newline.

- Starting Landmark
- Condition Value
- Finishing Landmark

## Execution Flow
The execution flow can be visualized as traversing a graph following its edges. Your journey will start at the `start` node and will end as soon as the you reaches the `finish` node. Therefore each command represents a directed edge in the graph from the starting landmark to the finishing landmark. The condition value specifies which edge to be traversed from a particular node. 

Only the commands with condition value equal to the value of `cond` will be available to follow.

If there is no valid path available, an error will be returned. The `start` and `finish` node must be present in the code otherwise an error will be generated.

## Books
Each magical book will be open at a particular page at any moment of time, and you can write one number at each page in the book. Since the books are magical, they have a pecuiliar property that writing any number on any page of one book automatically reflects in the other books as well. So, if you write, for example, the number 5 on page 4 of one book, turning to page 5 on any other book will also show the number 5. You can overwrite previously written numbers, the changes which will also be reflected to the other books. However, the page number you can have open in any book is independent of any other, only the contents are synchornized at all times. 

If you are familiar with the terminology, you can visualize the three books are pointers on a memory tape of infinite length.

The page numbers in the books start from 0, and there are infinite pages in each book.

- `mem_1` - The page number currently open in the first magical book
- `mem_2` - The page number currently open in the second magical book
- `mem_3` - The page number currently open in the third magical book

`mem[mem_1]` will denote the number written on page `mem_1` in any book.


## Compass

The compass will guide your travels by telling you where to go next from any landmark. At any instant of time, the compass will display a number, which you can change on your own, or in the course of your travels. At any step in your journey, you can only travel next to a code line which has the condition value equal to the current value of the compass (also referred to as `cond`).

## Mysterious box

The mysterious box refers to an interpreter, which will go through your travel plan step by step, and direct you automatically to the next landmark in your travel by using the compass(`cond`) and the *condition value* of the statements.

## Dictionary
The following table contains the contents of the dictionary that you have been provided.

| **IITK LANDMARK**           |          **COMMAND** |
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
| airstrip_takeoff_1      |          prints one character (conversion of int to ascii) at a time from mem[mem_1] until the flag is encountered|
| airstrip_takeoff_2      |          prints one character (conversion of int to ascii) at a time from mem[mem_2] until the flag is encountered| 
| pronite_1               |          mem_flag[mem_1] = 1;    
| pronite_2               |          mem_flag[mem_2] = 1;                    
| events_1                |          checks if there is a flag at mem1 location (mem_flag[mem_1] == 1). If yes, you are teleported to events_1_t, else to events_1_f. |         
| events_1_t              |          Path followed if events_1 is true |
| events_1_f              |          Path followed if events_1 is false |
| events_2                |          checks if there is a flag at mem2 location (mem_flag[mem_2] == 1). If yes, you are teleported to events_2_t, else to events_2_f. |
| events_2_t              |          Path followed if events_2 is true |
| events_2_f              |          Path followed if events_2 is false |

# About the Language
IITK - Traveller is an esoteric language designed by Programming Club,IIT Kanpur. Started as a fun winter project, the construct of the language is partially inspired by esolangs 3var and Taxi, and its major goal is to introduce IITK peeps to esolangs and provide them with a relatable, challenging and creative construct, in case they have been bored using the similar language constructs like C/C++,Java,Python etc.
