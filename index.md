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

## Books
Each magical book will be open at a particular page number at any moment of time and all the operations are done with respect to the value written on this page. This page number can be changed by visiting certain locations.Moreover only one number can be present at a page at any time. Initially all pages in all the books have 0 written on them. Since the books are magical, they have a pecuiliar property that writing any number on any page of one book automatically reflects in the other books as well. So, if you write, for example, the number 5 on page 4 of one book, turning to page 5 on any other book will also show the number 5. You can overwrite previously written numbers, the changes which will also be reflected to the other books. However, the page number you can have open in any book is independent of any other, only the contents are synchornized at all times. 

If you are familiar with the terminology, you can visualize the three books are pointers on a memory tape of **infinite** length.

The page numbers in the books start from 0, and there are **infinite** pages in each book.

- `mem_1` - The page number currently open in the first magical book. **(Default/Initial value: 0)**
- `mem_2` - The page number currently open in the second magical book. **(Default/Initial value: 1)**
- `mem_3` - The page number currently open in the third magical book. **(Default/Initial value: 2)**

{: .info}
`mem[mem_1]` will denote the number written on page `mem_1` in any book.

## Compass

The compass will guide your travels by telling you where to go next from any landmark. At any instant of time, the compass will display a number, which you can change be changed in the course of your travels. At every landmark there should be outgoing paths denoted with some number that you would take to travel to the next location. At any step in your journey, you can only take the path which is denoted by the number equal to the current value of the compass (also referred to as `cond`). **The default/initial value of the compass is 0.**

If at a particular location there are multiple outgoing paths which match the current value of the compass, you are confused and get stuck at that location. Thus while setting the map you should make sure that such a situation never arises.

## Mysterious box

The mysterious box refers to an interpreter, which will go through your travel plan step by step, and direct you automatically to the next landmark in your travel by using the compass(`cond`) and the *condition value* of the statements.

## Dictionary
The following table contains the contents of the dictionary that you have been provided.

| **IITK LANDMARK**           |          **COMMAND** |
| start                   |          start |
| finish                  |          finish |
| iit_gate_in_1           |          integer input to mem[mem_1] |
| iit_gate_in_2           |          integer input to mem[mem_2] |
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
| southern_labs_1         |          mem[mem_1]-- |
| southern_labs_2         |          mem[mem_2]-- |
| oat_stage[i]            |          cond += i    |
| hall_13_1               |          mem[mem_1] = 0 |
| hall_13_2               |          mem[mem_2] = 0 |
| hall_13_3               |          mem[mem_3] = 0 |
| hall_13_c               |          cond = 0|
| rm_1                    |          mem_1++ |
| rm_2                    |          mem_2++ |
| rm_3                    |          mem_3++ |
| kd_1                    |          mem_1-- |
| kd_2                    |          mem_2-- |
| kd_3                    |          mem_3-- |
| eshop_1                 |          mem[mem_1] = mem[mem_1] * mem[mem_1] |
| eshop_2                 |          mem[mem_2] = mem[mem_2] * mem[mem_2] |
| nankari_gate_in_1       |          Takes a single charcter as input and stores its ASCII value at mem[mem_1]
| nankari_gate_in_2       |          Takes a single charcter as input and stores its ASCII value at mem[mem_2]
| nankari_gate_out_1      |          Prints the character corresponding to the ASCII value stored at mem[mem_1]
| nankari_gate_out_2      |          Prints the character corresponding to the ASCII value stored at mem[mem_2]
| airstrip_land_1         |          Takes a string as input and stores the ASCII value of the i<sup>th</sup> (0 indexing) character at mem[mem_1 + i] ending with a special EOS character|
| airstrip_land_2         |          Takes a string as input and stores the ASCII value of the i<sup>th</sup> (0 indexing) character at mem[mem_2 + i] ending with a special EOS character |
| airstrip_takeoff_1      |          Prints a string where the i<sup>th</sup> (0 indexing) character corresponds to the ASCII value stored mem[mem_1 + i]. This operation terminates only when an EOS literal is encountered. |
| airstrip_takeoff_2      |          Prints a string where the i<sup>th</sup> (0 indexing) character corresponds to the ASCII value stored mem[mem_2 + i]. This operation terminates only when an EOS literal is encountered. | 
| pronite_1               |          Inserts an EOS literal at mem[mem_1]    
| pronite_2               |          Inserts an EOS literal at mem[mem_2]                 
| events_1                |          Checks whether an EOS literal is present at mem[mem_1]. If yes, you are teleported to events_1_t, else to events_1_f. |         
| events_1_t              |          Path followed if events_1 is true  |
| events_1_f              |          Path followed if events_1 is false |
| events_2                |          Checks whether an EOS literal is present at mem[mem_2]. If yes, you are teleported to events_2_t, else to events_2_f. |
| events_2_t              |          Path followed if events_2 is true  |
| events_2_f              |          Path followed if events_2 is false |

{: .info}
`oat_stage` is a special kind of location to which a parameter i is passed. To get more information regarding this location visit the Landmark Definition Section.

{: .info}
EOS character is a special character that is used to denote the end of a string and does not correspond to any valid signed 32-bit integer value. Hence the EOS value cannot be used in any mathematical operation.

# Programming Specifications
As a programmer, you have to set a map, specifically the outgoing paths from certain landmarks you wish to visit to produce the desired token (output) at the end of your journey. Then with help of the mysterious box you can simulate your journey to get an idea about the output produced as a result of the map.

## Syntax
Each command consists of 3 comma-separated tokens ended with a newline.

- Starting Landmark
- Condition Value
- Finishing Landmark

## Execution Flow
The execution flow can be visualized as traversing a graph following its edges. Your journey will start at the `start` node and will end as soon as the you reaches the `finish` node. Therefore each command represents path, which is a directed edge from the starting landmark to the finishing landmark. The condition value here is the number by which the path is denoted.

When the traveller is present at any node, firstly the operation corresponding to that node is performed then the traveller travels to the next location taking the path corresponding to the current value of `cond`.

If at any node there is no path with value equal to the current value of `cond`, an error will be returned. 

Moreover, as specified earlier, at any node there should not be more than one paths denoted by the same number (condition value).

{: .info}
The traversal should start at the `start` node and end at the `finish` node. The traversal ends as soon as you reach the `finish` node.

{: .info}
The current implementation of this langauge does not support more that 10<sup>6</sup> operations.

# About the Language
IITK - Traveller is an esoteric language designed by Programming Club,IIT Kanpur. Started as a fun winter project, the construct of the language is partially inspired by esolangs 3var and Taxi, and its major goal is to introduce IITK peeps to esolangs and provide them with a relatable, challenging and creative construct, in case they have been bored using the similar language constructs like C/C++,Java,Python etc.
