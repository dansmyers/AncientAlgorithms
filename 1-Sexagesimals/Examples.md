# Assignment 1 Examples and Notes

## Standard field problem

Here's an example problem that demonstrates the basic idea of completing the square. As we've discussed, this was a standard technique known to the ancient Mesopotamians and a preferred way of formulating and solving quadratic equations.

*Consider a rectangular field with an area of 1000 square cubits. The length exceeds the width by 20 cubits. Find the length and width.*

First, note that I'm giving you all the numbers for problems like this in base-10 so you don't have to manage non-trivial calculations in base-60. Next, think about the geometric setup. There is a rectangular field of dimensions *w* and *l*. The problem uses units of cubits, but that doesn't affect the solution procedure.

```
    -------------------------
   |                         |
   |                         | 
w  |                         |
   |                         |
   |                         |
    -------------------------
                l
```

The area is known, so we have:

*l* *w* = 1000

The problem relates the length and width to each other:

*l* = *w* + 20

Substituting in place of *l* in the area equation:

*w*(*w* + 20) = 1000

This is a quadratic equation in *w*. Once we solve for *w*, adding 20 to it will give the length.

*w*<sup>2</sup> + 20*w* = 1000

Geometrically, we have the following configuration:

```
    -------------------------
   |                  |      |
   |                  |      | 
w  |                  |      |
   |                  |      |
   |                  |      |
    -------------------------
             w           20
```

Completing the square rearranges this field, which has an area of 1000, into an equivalent field with the same area but a different configuration. Split the strip of width 20 into half, then rotate one half down to the bottom of the figure:

```
             w         10
    ----------------------
   |                  |   |
   |                  |   | 
w  |                  |   |
   |                  |   |
   |                  |   |
    ----------------------
10 |                  |    
    ------------------
```

Allowing for some inexactness in the text picture, this configuration has the same area as the original rectangle. It's *almost* a square of side *w* + 10, but there's a little corner piece missing. Subtracting out the area of the missing corner allows us to "complete the square" and derive an alternate equation with only one *w* term:

(*w* + 10)<sup>2</sup> - (10)<sup>2</sup> = 1000

where the right-hand side is the original area and the subtracted term is the area of the missing corner square. At this point, the solution is a matter of isolating *w* on the left-hand side:

*w* = sqrt(1100) - 10

Solving (with the aid of a calculator, which is fine for these calculations) gives that *w* is about equal to 23.16625 and therefore *l* is about 43.16625. Checking the area will show that the product of those two values is very close to 1000, which is what we want.


## In 3-D

Here is a problem similar to the first example in the Knuth paper that we looked at in class.

A rectangular cistern. A volume 10000 cubic cubits has been excavated. The height is 5 cubits. The length exceeds the width by 50 cubits. Find the length and width.

If it's helpful, start by drawing the rectangular box and labeling the length, width, and height. We're given the volume of 10000 and the known height of 5. Again, the units of cubits are merely flavor text, which I use to create a certain flair in the problem; they don't affect the solution.

The starting equation here is the volume:

*l**w**h* = 10000

The first step is to divide by the height and isolate *l**w*, which is the area of the base:

*l**w* = 2000

This is now the same setup as the previous problem: We have a rectangular region of known area and a relationship between the length and width. Use the same technique as the last example to solve.

