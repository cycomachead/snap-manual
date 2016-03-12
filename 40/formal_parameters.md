## Formal Parameters {#formal-parameters}

The rings around Procedure-type inputs have an arrowhead at the right. Clicking the arrowhead allows you to give the inputs to a block or script explicit names, instead of using empty input slots as we’ve done until now.

![image](SnapManual/Image_143.jpg)

The names #1, #2, etc. are provided by default, but you can change a name by clicking on its orange oval in the input names list. Be careful not to _drag_ the oval when clicking; that’s how you use the input inside the ring. The names of the input variables are called the _formal parameters_ of the encapsulated procedure.

Here’s a simple but contrived example using explicit names to control which input goes where inside the ring:

![image](SnapManual/Image_144.jpg)

Here we just want to put one of the inputs into two different slots. If we left all three slots empty, Snap! would not ﬁll any of them, because the number of inputs provided (2) would not match the number of empty slots (3).

![image](SnapManual/Image_145.jpg)

Here is a more realistic, much more advanced example:

![image](SnapManual/Image_146.png)

![image](SnapManual/Image_147.png)

This is the deﬁnition of a block that takes any number of lists, and reports the list of all possible combinations of one item from each list. The important part for this discussion is that near the bottom there are two _nested_ calls to map, the higher order function that applies an input function to each item of an input list. In the inner block, the function being mapped is in front of, and that block takes two inputs. The second, the empty List-type slot, will get its value in each call from an item of the inner map’s list input. But there is no way for the outer map to communicate values to empty slots of the in front of block. We must give an explicit name, newitem, to the value that the outer map is giving to the inner one, then drag that variable into the in front of block.

By the way, once the called block provides names for its inputs, Snap! will not automatically fill empty slots, on the theory that the user has taken control. In fact, that’s another reason you might want to name the inputs explicitly: to stop Snap! from filling a slot that should really remain empty.