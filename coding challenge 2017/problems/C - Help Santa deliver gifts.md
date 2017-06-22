# Help Santa deliver gifts
 
* **Simple Input (5p)** — small data set; [get input](https://github.com/Mixbook/coding-challenge-event/blob/master/coding%20challenge%202017/inputs/C-small-input.in)
* **Complex Input (5p)** — large data set; [get input](https://github.com/Mixbook/coding-challenge-event/blob/master/coding%20challenge%202017/inputs/C-large-input.in)
 
On the New Year’s Eve Santa Claus has hopped on his sleigh and looks at his map to deliver greeting cards and presents for the kids. His reindeer are tired, and are only able to fly in straight lines. Santa wants to plan his flight with as little turns as possible.
 
Santa has marked all the places he has to fly by on the map with dots. It turned out that the distance between dots on X axis is precisely **5 points**. Build a polygonal chain that connects all the dots. Every segment of the chain must start, where the previous segment ended and consist of at least **2 dots**. The chain must include all the dots. 
 
Santa can fly near a dot to deliver the presents, but it should be within **K** points from his route.

### Input
The first line of the input gives the number of test cases **T** and the maximum distance from the segment line — **K** separated by space. T test cases follow.
Each test case consists of a list of points' **Y** coordinate separated by space, that starts with **N** number of points. 
 
### Output
For each test case, output one polygonal chain with segments separated by commas. 

The segments should contain successive dots separated by space. 
 
### Limits
* 1 ≤ **T** ≤ 100.
* 3 ≤ **N** ≤ 20 (small data set)
* 3 ≤ **N** ≤ 200 (large data set)
 
### Sample

```bash
Input
2 5
10| 60 38 58 51 43 26 12 3 16 18
12| 26 6 17 6 14 2 17 8 12 17 21 1
 
Output
1 2, 2 3, 3 4 5 6 7 8, 8 9 10
1 2, 2 3, 3 4, 4 5, 5 6, 6 7, 7 8, 8 9 10 11, 11 12
```

![Sample output](/coding%20challenge%202017/problems/images/C-example.png?raw=true "Sample output")
 
Check sample output image for reference. The purple line represents the maximum distance **K** from a dot to the line. In the example image, the 0, 0 coordinate is in top left corner of the map, but you can do it also from bottom left.
 
In **sample case #1** it’s possible to skip dots 4,5,6 and 7 making a straight line from 3 to 8. And skip dot 9 by making a line from 8 to 10. This results in 4 sections: 1-2, 2-3, 3-8 and 8-10.
 
In **sample case #2** there’s no way to skip dots until dot 9 and 10, by making a straight line from 8 to 11. This results in 9 sections: 1-2, 2-3, 4-5, 6-7, 7-8, 8-11 and 11-12.
