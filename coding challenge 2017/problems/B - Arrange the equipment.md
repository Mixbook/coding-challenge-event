# Arrange the equipment
 
* **Simple Input (5p)** — small data set; [get input](https://github.com/Mixbook/coding-challenge-event/blob/master/coding%20challenge%202017/inputs/B-small-input.in)
* **Complex Input (5p)** — large data set; [get input](https://github.com/Mixbook/coding-challenge-event/blob/master/coding%20challenge%202017/inputs/B-large-input.in)
 
A printing studio has decided to buy some modern printing equipment to speed up their work. To lower the total price, they decided to pick parts from different brands. They know that all the parts are compatible with each other, can be arranged in any sequence and will produce a proper result.
 
Robert, the technical manager of the studio, has been assigned with making the printing conveyor from the purchased parts. While reading through manuals, Robert found out that some parts work better together, some worse and neutral with others. He has numbered all parts from **1 to n** and has labeled which parts should be places next to each other, and which should not. 
 
Help Robert find the best match for positioning the equipment in a row in such a way, that each part is next to the ones it works best with. Keep in mind that parts don't always work well both ways: **a** will work well with **b**, but **b** can work badly with **a**.
 
### Input
The first line of the input gives the number of test cases, **T**. T test cases follow. Each test case consists of a list of part pairs separated by comma starting with **N**. Every pair is represented  as **x y k**, where **x** and **y** are parts nad **k** showes if they work good together(+) or bad together(-).

For example: ```3| 1 3 +, 1 2 -, 2 3 +, 2 1 -, 3 1 +, 3 2 -```. **3|** means there are 3 parts. 1 is good with 3, 1 is bad with 2, 2 is good with 3 and so on.
 
### Output
For each test case, output one line that consists of an ordered list of the parts separated by spaces.
 
### Limits
* 1 ≤ **T** ≤ 100.
* 3 ≤ **N** ≤ 15 (small data set)
* 3 ≤ **N** ≤ 100 (large data set)
 
### Sample

```bash
Input
2
3| 1 3 +, 1 2 -, 2 3 +, 2 1 -, 3 1 +, 3 2 -
4| 1 2 +, 1 3 -, 1 4 -, 2 3 +, 2 4 +, 2 1 -, 3 1 +, 3 4 +, 3 2 -, 4 3 +, 4 2 +, 4 1 -
 
Output
1 3 2
1 2 4 3
```
 
The sample output displays one set of answers to the sample cases. Other answers may be possible.
 
In **sample case #1**, the 1st part will work better with 3rd and worse with 2nd, the 2nd part with 3rd and so on. Both first and second part don't work well with each other but work better with 3rd, so the solution would be placing the 3rd part in the middle. The output could also be 2 3 1.
 
In **sample case #2** we have 4 items, but the solution is similar. 1st part should be placed only near 2nd, the 2nd should be placed near 3 or 4, and the 4th part should not be placed near first. In the sample output we are placing 1 and 2 near each other resulting in a neutral effect but helping arrange the rest of the parts in a more favourable order. 
