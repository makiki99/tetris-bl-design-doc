# Tetris Black Label design doc

## Basic information  
* Rotation system: ARS (Ti version)
* Framerate: 60FPS
* Piece previews: 3
* Hold: yes

## Level system  
A loop starts at level 1, and ends at level 999.  
The rest is the same as in TGM3 Ti.

## Rank system  
Rank starts at 0 and will increase from 3 separate rank sources.
Whenever one of the rank sources reach 100% or more, the rank increases by one, and that rank source value decreases by 100%.  
The rank caps out at 50 during the first loop, and at 100 during the second loop.

### Rank sources  
#### Line clears  
Line clear type | Rank value increase
---|---
Single | 5%
Double | 12%
Triple | 25%
Tetris | 50%

#### Speed  
Every level gained increases this source by 4%.  
Every frame this source is decreased by 0.04%, even during ARE.  
This rank source can't fall below 0%.

#### Survival  
Every section passed increases value of this rank source by 100%, functioning as an direct rank increase by 1.

## Second loop requirements  
* Rank 50
* (to be added later)

## Speedcurve  
### First loop  
#### pre-20G  
Rank | ARE | Lock delay | Line clear delay | DAS
---|---|---|---|---
0-19 | 30 | 30 | 30 | 14

Rank | Gravity | Rank | Gravity
---|---|---|---
0 | 4/256 G | 10 | 1 G
1 | 8/256 G | 11 | 1.5 G
2 | 16/256 G | 12 | 2 G
3 | 24/256 G | 13 | 2.5 G
4 | 32/256 G | 14 | 3 G
5 | 48/256 G | 15 | 3.5 G
6 | 64/256 G | 16 | 4 G
7 | 96/256 G | 17 | 4.5 G
8 | 128/256 G | 18 | 5 G
9 | 192/256 G | 19 | 10 G

#### 20G  
Rank | ARE | Line clear delay | Lock delay | DAS
---|---|---|---|---
20-24 | 30 | 22 | 30 | 8
25-29 | 25 | 16 | 30 | 8
30-34 | 20 | 8 | 30 | 8
35-39 | 16 | 6 | 30 | 8
40-44 | 12 | 4 | 17 | 6
45-49 | 6 | 3 | 17 | 6
50 | 4 | 2 | 15 | 6

### Second loop  
Rank | ARE | Line clear delay | Lock delay | DAS
---|---|---|---|---
50-69 | 4 | 2 | 15 | 6
70-89 | 4 | 2 | 12 | 6
90-99 | 4 | 1 | 10 | 6
100 | 4 | 0 | 8 | 6

## Grade names  
Pre-S grades|S grades|M grades|X Grades|Master Grades
---|---|---|---|---
9|S1|M1|X1|Master
8|S2|M2|X2|MasterS
7|S3|M3|X3|MasterM
6|S4|M4|X4|MasterX
5|S5|M5|X5|Grand Master
4|S6|M6|X6|
3|S7|M7|X7|
2|S8|M8|X8|
1|S9|M9|X9|
|S10|||
|S11|||

#### Max grade obtainable in first loop:
* S9 without M-roll
* S10 with M-roll achieved
* S11 with M-roll passed

#### Master grades requirements
* Master - 2nd M-roll achieved
* MasterS - 2nd M-roll cleared
* MasterM - 2nd M-roll cleared with good performance (unspecified yet)
* MasterX - True M-roll achieved
* Grand Master - True M-roll cleared
