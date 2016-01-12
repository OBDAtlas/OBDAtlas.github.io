---
title: Trouble Codes
layout: page
parent: 03
permalink: resources/pids/03/trouble-codes.html
description: Mode 03 is used to request trouble codes from the ECU. You cannot provide any pid together with this mode. 3 codes per message frame.
---

### First character
A7-A6 | First DTC Character
------|--------------------
  00  | P - Powertrain
  01  | C - Chassis
  10  | B - Body
  11  | U - Network


### Second character
A5-A4 | Second DTC Character
------|---------------------
  00  | 0
  01  | 1
  10  | 2
  11  | 3


### Third character
A3-A0, B7-B4, B3-B0 | Third, Fourth and Fifth DTC Character
--------------------|--------------------------------------
        0000        |   0
        0001        |   1
        0010        |   2
        0011        |   3
        0100        |   4
        0101        |   5
        0110        |   6
        0111        |   7
        1000        |   8
        1001        |   9
        1010        |   A
        1011        |   B
        1100        |   C
        1101        |   D
        1110        |   E
        1111        |   F


*Example output: P0420 - Catalyst System Efficiency Below Threshold Bank 1*
