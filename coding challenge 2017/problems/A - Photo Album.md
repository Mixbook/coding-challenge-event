# A — Photo Album

* **Simple Input (5p)** — area of interest matches photo size; [get input](https://github.com/Mixbook/coding-challenge-event/blob/master/coding%20challenge%202017/inputs/A-small-input.in)
* **Complex Input  (5p)** — area of interest is inside photo; [get input](https://github.com/Mixbook/coding-challenge-event/blob/master/coding%20challenge%202017/inputs/A-large-input.in)
 
Boris and Anna have just returned from their trip to Paris. They have done **N** photos and want to have them printed in a beautiful photo album. The album already has **N** slots for photos of different sizes and proportions. Boris wants different objects like people, buildings and flowers in the photos to be seen in the photo slots, otherwise the album will be a disaster.

Boris has outlined the the **area of interest** on the photos with a rectangle.
 
Help Boris and Anna pick the right photos to fit in all the slots that meet those criteria:
* The photo should fill the slot completely, meaning there is no empty space in the photo slot;
* The photo should not be extra scaled;
* The center of the area of interest should be inside in the photo slot;
* Pick the best photo slot for each area of interest, to be a good ratio match; 

You can scale images proportionally (the ratio should be the same).
 
Given the list of photo dimensions, areas of interest and photo slots sizes, calculate the perfect match for each photo and output the final dimensions of each photo and the slot it should fit in. The **x** and **y** coordinates start with **0 0** from top left of the screen.

### Input

The first line of the input gives the number of test cases, **T**. **T** test cases follow. Each consists of a list of photos and photo slots, separated by commas and starting with **N** - number of photos. Every photo has 6 parameters: **w h x0 y0 x1 y1**, where: **w** is photo width, **h** - photo height, **x0**, **y0** are the coordinates of the area of interest top left corner and **x1**, **y1** - the coordinates of bottom right corner.

Each photo slot has 2 parameters: slot **width** and slot **height**, and starts with **N** - the number of photo slots. Check sample image for reference.

### Output

For each test case, output one line - a list of photos separated by comma. Every photo must be represented as: **n k x2 y2 x3 y3**, where **n** - photo number(starting from 1), **k** - slot number(starting from 1), **x2** and **y2** - the top left corner coordinates of the scaled photo inside the photo slot, and the **x3 y3** - the bottom right corner coordinates. Check sample image for reference.

![I/O Explanation](/coding%20challenge%202017/problems/images/A-io-example.jpg?raw=true "I/O Explanation")

### Limits

* 1 ≤ **T** ≤ 100
* 3 ≤ **N** ≤ 10
* Every photo size is either **3 x 4** or **4 x 3**.
* **Simple input** — the area of interest is the same size as photo
* **Complex input** — the area of interest is inside the photo

### Sample
 
```bash
Input:
2
3| 4 3 0 0 4 3, 4 3 0 0 4 3, 3 4 0 0 3 4
3| 5 2.5, 1.5 2.5, 3.5 1.5 
2| 3 4 0.2 2.3 2.9 3.5, 4 3 1.1 1.2 2.7 2.7
2| 5 2, 5 4.5
 
Output:
1 1 0 -0.62 5 0.62, 2 3 0 -0.56 3.5 0.56, 3 2 -0.19 0 1.69 2.5
1 2 0 -1.44 5 2.3, 2 1 0 -2.18 5 4.5
```

![Sample output](/coding%20challenge%202017/problems/images/A-example.png?raw=true "Sample output")
 
The sample output displays one set of answers to the sample cases. Other answers are possible. Note that second sample case will not appear in simple input.
 
In **sample case #1** the area of interest is the same size as the photo, so we need to place the photo inside the slot making minimal adjustments. The best matching photo to slot ratios would be 1 photo -1 slot , 2-3, 3-2 or 1-3, 2-1, 3-2 (we've picked the first one). We scale the photo to fit in the corresponding photo slots without leaving empty spaces.
 
The output of "1 1 0 -0.62 5 0.62" means that the 1st photo goes to 1st photo slot, the top left corner is slightly above the photo slot and the lower right corner is slightly below — they are vertically aligned.
The 3rd photo “3 2 -0.19 0 1.69 2.5” is horizontally aligned with the 2nd photo slot, and the top left corner is to the left and the right corner is to the right of the photo slot. Check image for reference.
 
For **sample case #2** the area of interest is inside the photo, so we scale the photos and position them in the slots in a way, that the area of interest is centered in the photo slot and we try to pick the best ratio match. Check images for reference.