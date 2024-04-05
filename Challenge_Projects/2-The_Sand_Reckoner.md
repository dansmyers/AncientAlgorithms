# Challenge Project: *The Sand Reckoner*

## Due

## Overview

*The Sand Reckoner* is a manuscript by Archimedes, written as a letter to the king of Syracuse. In it, Archimedes lays out an argument that it's possible to count the number of grains of sand that would fill the entire universe. This requires him to do two interesting things:

1. Estimate the size of the universe, which Archimedes does using a model proposed Aristarchus of Samos, an earlier astronomer. The model of Aristarchus is *heliocentric*, making this one of the earliest theories that assumes the Earth and planets move about the sun.

2. Develop a method for representing very large numbers. Greek numbers used a system where different letters stood for different magnitudes. Their largest standard number was the *myriad*, which equaled 10,000. Archimedes designs a place-value number system using the *myriad of myriads* (that is, 10,000 * 10,000 = 100 million) as its base unit.

Archimedes' goal in making this argument is less about producing a real accurate estimate of the grains of sand that could fit in the universe, and more about showing that it's possible to calculate with quantities that would have been, by the standards of the time, unimaginably huge.

## The Assignment

I thought about making you read *The Sand Reckoner* and then answer some questions about it, or something, but that's boring.

Instead: You're going to **design your own assignment** based on *The Sand Reckoner*. This has three parts:

- Read and understand the core concepts of the manuscript. My notes and links below will help you get started.

- Develop an assignment that a hypothetical student could do based on the work. This *could* be a set of questions or a writing prompt, but you can choose another option if you like. Your assignment must give specific learning goals your student will demonstrate by performing it.

- Map the goals of your assignment to the levels of **Bloom's Taxonomy**, a model of the complexity of learning tasks, described below.

Note that you don't have to *do* your own assignment. It's enough to design one, state its learning goals, and map them to Bloom's Taxonomy. You should, however, choose something could feasibly be done by a potential student.


## Notes

### The manuscript

A paraphrased copy of the manuscript is [available here](https://www.ucolick.org/~laugh/reckoner.shtml). This is much easier to read than the regular translated text and lays out the key ideas in more modern notation. Start by reading the beginning, then look at my notes below, then come back and work through the rest of the manuscript.

After the introduction, there are three major sections, each laying out one part of Archimedes' argument:

1. A derivation of the size of the universe, using the heliocentric model of Aristarchus

2. A system for representing big numbers based on units of 100 million

3. A scaling argument that starts with the grains of sand that could fit in a poppy seed and builds up to the estimated number of grains of sand that could fit in the universe


### The size of the universe

Aristarchus's original writing describing his heliocentric model is lost. We do have other writings by him that use a geocentric model and perform gnarly feats of trigonometry to do things like estimate the sizes and distances of the Sun and Moon.

The model is similar to our current conception of the solar system, with the Sun at the center and the earth and other planets moving in circular orbits about it. Much, much, *much* further away is the "sphere of fixed stars", representing the unmoving stars. From a 2D side view, the model looks like this:

<img src="https://lh5.googleusercontent.com/proxy/FvN1nEgkEiIzAsTHWJ_7iRGyr6Qk7n2DWtk4StZdmkLTGvkU7IWz8h5m5BqO-2nQCL1ilc-v8FHNHXdER8E" width="300px" />

*Greg Bothun, U. Oregon*

The stars are the outermost boundary of everything, and Archimedes wants to fill the sphere they surround with sand. Therefore, he needs to know the **diameter** of the sphere of stars so he can calculate its volume.

Archimedes argues (in an ad-hoc way) that the relationship between the stars and the Earth/Sun center of the universe is the same as the relationship between the Earth and Sun:

```
   diameter of the sphere of fixed stars             diameter of the Earth's orbit around the Sun
--------------------------------------------    =    --------------------------------------------
diameter of the Earth's orbit around the Sun                    diameter of the Earth
```

Therefore, if Archimedes knows the diameter of the Earth and the diameter of the orbit around the Sun, he can find the diameter of the entire universe.

He first assumes the circumference of the Earth is no more than 3 million *stadia*. He notes that this is much bigger than other estimates, which were closer to 300,000 stadia. Recall that we discussed Erasothenes, who came up with an estimate of about 250,000 stadia. Dividing by 3 as an approximation of pi, we conclude that the diameter of the Earth can't be bigger than 1 million stadia. This is the first piece.

Citing earlier astronomers, he then states that the diameter of the Sun is no more than 30 times the diameter of the moon. The Earth is bigger than the moon, so the Sun's diameter can't be more than 30 million stadia.

The final part of this argument is the most technical. Archimedes argues that the orbit of the Earth around the Sun is about 1000 times the Sun's diameter. In the original manuscript, this leads to a long discussion where he describes an experiment he carried out to measure the angular size of the Sun in the sky. You can see some details [here](https://web.calstatela.edu/faculty/hmendel/Ancient%20Mathematics/Archimedes/SandReckoner/Ch.1/Ch1.html), but don't stress about it; it's pretty hard to follow.

Putting all this together:

- The Earth's diameter is roughly 1 million stadia

- The Sun's diameter is 30 times this: 30 million stadia

- The orbit of the Earth is 1000 times the Sun's diameter: 30 billion stadia

- Therefore, the diameter of Earth's orbit is about 10 billion stadia, which is 10000 times the diameter of Earth (1 million * 10000 = 10 billion)

- The diameter of the entire universe is therefore 10 billion * 10000 = 100 trillion stadia. This is about [two light years](https://en.wikipedia.org/wiki/The_Sand_Reckoner), which might make Archimedes the first person to think on the scale of real astronomy.

### Big Numbers

The second part of the manuscript discusses Archimedes' system for representing big numbers.

He starts with the standard Greek unit of a *myriad*, which is 10,000, and then proposes to count based upon the *myriad of myriads*, which is 10,000 * 10,000 = 100 million. He calls the numbers from 1 to 100 million the *first order*.

He then defines the *second order* as all the numbers that can be represented from 100,000,000 to 100,000,000<sup>2</sup>. That is, the largest number of the second order is a *myriad of myriads of a myriad of myriads*.

The *third order* are all the numbers from 100,000,000<sup>2</sup> to 100,000,000<sup>3</sup>. He then proposes continuing this process until arriving at the 100,000,000th order, which reaches the number 100,000,000<sup>100,000,000</sup>.

Archimedes' system is very similar to a positional number system of **base-100 million**! Each "order" of his system is like adding one more digit that represents a power of 100,000,000. A number of the third order, for example, could be written in the following form:

```
    a  b  c
    ^  ^  ^  
    |  |  |
    |  |  c * 100,000,000^0
    |  | 
    |  b * 100,000,000^1
    |
    this place stands for a * 100,000,000^2
```

In our modern framework, such a number could represent values from 0 to 100,000,000<sup>3</sup> - 1. The 100,000,000th order corresponds to the base-100 million numbers having 100 million digits.

But Archimedes is an absolute legend for a reason and he ***SIMPLY REFUSES TO QUIT MAKING EVEN HUGER NUMBERS***. 

He calls the number 100,000,000<sup>100,000,000</sup> the *first period* and proposes to now use *that* as the base of his number system. He works his way up to a number that is equivalent 100 million digits in base-100,000,000<sup>100,000,000</sup>. The largest value represented by Archimedes' system is

(100,000,000<sup>100,000,000</sup>)<sup>100,000,000</sup>

This is a 1 followed by 8 billion billion zeros (80 quadrillion zeros).

### Grains of sand

Now the key question: Is such a number big enough to represent the grains of sand that would fill the entire universe?

Throughout the last part, Archimedes uses the fact that the volume of a sphere scales with the cube of its diameter:

- If you double the diameter of sphere, the volume increases by a factor of 8
- If you make the diameter ten times larger, the volume increases by a factor of 1000
- If you 100x the diameter, the volume increases by a factor of 1 million

This is a (mostly) straightforward scaling argument. Archimedes asserts, without proof, that at most 10,000 grains of sand would fit into the volume of a poppy seed. He then states that a finger width (*dactyl*) is 40 poppy seeds long, so the grains of sand that would fit into a sphere with a diameter of one dactyl is at most

40<sup>3</sup> * 10,000 = 64,000 * 10,000 = 640 million

Archimedes then says that this is less than 1 billion, which can be written using numbers of his previously-defined second order.

Making the sphere bigger, Archimedes says that one *stade* is less than 10,000 finger lengths, so the number of grains that could fill a sphere of one *stade* diameter is no more than

10,000<sup>3</sup> * 1 billion = 1 trillion * 1 billion = 10<sup>12</sup> * 10<sup>9</sup> = 10<sup>21</sup>

which is 1 sextillion grains of sand in modern notation.

The estimated size of the universe is 100 trillion stadia (10<sup>14</sup>), so the estimated number of grains in the entire universe is

(10<sup>14</sup>)<sup>3</sup> * 10<sup>21</sup> = 10<sup>42</sup> * 10<sup>21</sup> = 10<sup>63</sup>




