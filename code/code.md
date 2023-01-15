---
title : landmark_definitions
layout : home
# has-children : true
nav_order : 1
---

# Landmark Definitions

## iit_gate_in_1
Takes input from the console to the address in the memory tape pointed to by mem_1. Input is a signed 32-bit integer.

## iit_gate_in_2
Takes input from the console to the address in the memory tape pointed to by mem_2. Input is a signed 32-bit integer.

## hall_2
Standard addition operation. Adds the integers stored at the addresses pointed to by mem_1 and mem_2 and stores them at the address pointed to my mem_3. This operation is not valid for EOS literals.

## hall_3
Standard multiplication operation. Multiplies the integers stored at the addresses pointed to by mem_1 and mem_2 and stores them at the address pointed to my mem_3. This operation is not valid for EOS literals.

## hall_5
Standard subtraction operation. Subtracts the integers stored at the addresses pointed to by mem_1 and mem_2 in order (mem\[mem_1\] - mem\[mem_2\]) and stores them at the address pointed to my mem_3. This operation is not valid for EOS literals.

## hall_12
Standard subtraction operation. Subtracts the integers stored at the addresses pointed to by mem_1 and mem_2 in order (mem\[mem_1\] / mem\[mem_2\]) and stores them at the address pointed to my mem_3. This operation is not valid for EOS literals.

## mt_1_3
Copies the value stored at the address pointed to by mem_1 to the address pointed to by mem_3.

## mt_2_3
Copies the value stored at the address pointed to by mem_2 to the address pointed to by mem_3.

## mt_3_1
Copies the value stored at the address pointed to by mem_3 to the address pointed to by mem_1.

## mt_3_2
Copies the value stored at the address pointed to by mem_3 to the address pointed to by mem_2.

## iit_gate_out_1
Prints the value stored at the address pointed to by mem_1 to the console.

## iit_gate_out_2
Prints the value stored at the address pointed to by mem_2 to the console.

## lecture_hall_gt
Compares the values stored at the addresses pointed to by mem_1 and mem_2. If mem\[mem_1\] > mem\[mem_2\], then the traveller is transported to the location lecture_hall_gt_t. Otherwise the traveller is transported to the location lecture_hall_gt_f. These are actual landmarks and can be used in the program like any other landmark. This operation is not valid for EOS literals.

### lecture_hall_gt_t
The traveller is transported to this location if the value stored at the address pointed to by mem_1 is greater than the value stored at the address pointed to by mem_2.

### lecture_hall_gt_f
The traveller is transported to this location if the value stored at the address pointed to by mem_1 is less than or equal to the value stored at the address pointed to by mem_2.

## lecture_hall_lt
Compares the values stored at the addresses pointed to by mem_1 and mem_2. If mem\[mem_1\] < mem\[mem_2\], then the traveller is transported to the location lecture_hall_lt_t. Otherwise the traveller is transported to the location lecture_hall_lt_f. These are actual landmarks and can be used in the program like any other landmark. This operation is not valid for EOS literals.

### lecture_hall_lt_t
The traveller is transported to this location if the value stored at the address pointed to by mem_1 is lesser than the value stored at the address pointed to by mem_2.

### lecture_hall_lt_f
The traveller is transported to this location if the value stored at the address pointed to by mem_1 is greater than or equal to the value stored at the address pointed to by mem_2.

## lecture_hall_eq
Compares the values stored at the addresses pointed to by mem_1 and mem_2. If mem\[mem_1\] = mem\[mem_2\], then the traveller is transported to the location lecture_hall_eq_t. Otherwise the traveller is transported to the location lecture_hall_eq_f. These are actual landmarks and can be used in the program like any other landmark. This operation is not valid for EOS literals.

### lecture_hall_eq_t
The traveller is transported to this location if the value stored at the address pointed to by mem_1 is equal to the value stored at the address pointed to by mem_2.

### lecture_hall_eq_f
The traveller is transported to this location if the value stored at the address pointed to by mem_1 is not equal to the value stored at the address pointed to by mem_2.

## oat_stairs_1
Increments the value stored at the address pointed to by mem_1 by 1. This operation is not valid for EOS literals.

## oat_stairs_2
Increments the value stored at the address pointed to by mem_2 by 1. This operation is not valid for EOS literals.

## oat_stairs_c
Increments the value of the condition variable by 1.

## southern_labs_1
Decrements the value stored at the address pointed to by mem_1 by 1. This operation is not valid for EOS literals.

## southern_labs_2
Decrements the value stored at the address pointed to by mem_2 by 1. This operation is not valid for EOS literals.

## southern_labs_c
Decrements the value of the condition variable by 1. This operation is not valid for EOS literals.

## hall_13_1
Re-initializes the value stored at the address pointed to by mem_1 to 0.

## hall_13_2
Re-initializes the value stored at the address pointed to by mem_2 to 0.

## hall_13_3
Re-initializes the value stored at the address pointed to by mem_3 to 0.

## hall_13_c
Re-initializes the value of the condition variable to 0.