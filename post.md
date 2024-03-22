# Lab X: Doing stuff with hardware!

Please write a blog post describing your lab here.

This is just an example of how you might structure your blog post, feel free to edit as you wish. For example, you might divide the lab into different sections each with their own intro, instructions, results, and takeaways. Please see the rubric for details on how the post will be evaluated.

## Overview and Motivation
This week we'll explore...

## Materials
-IC data sheets

-PB-503 breadboard prototyping station

-Wires and connection tools

-Logic Probes

-Logic Switches

-Push Button

-7404 NOT gate IC

-7408 AND gate IC

-7486 XOR gate IC

-7476 JK Flip Flop IC

-Resistors

## Project Steps
In order to start designing the circuit, we first needed to design a FSM (DFA-Deterministic Finite Automata), using a state transition diagram. We designed it in the way that if the stream x, ends in 00, then the circuit outputs and 1, and if it ends in anything else, in outputs a 0.
<img src="./assets/dfa.png" />

Next we had to contruct a state table. A state table shows us the states and the steps taken inorder to reach those states. If you look at the image below you will see that our starting state is S0. This is because we want our stream to end in 00.

-Below is our state table.
<img src="./assets/statetable.png" />

After we created a state table we need to the FSM to and state table to create a function table. This shows us the before and after values for signals in the circuit. It showa the signals that are sent to the J and K inputs. 

- Below is the state table.
<img src="./assets/fun.png" />

Next, after creating the function table we use the values from the table inorder to contruct k-maps to create our circuit.
<img src="./assets/J1.png" />
<img src="./assets/K1.png" />
<img src="./assets/J0.png" />
<img src="./assets/K0.png" />
<img src="./assets/F.png" />

Finally, we use the k-maps to design and build the circuit.

-Below is the logisim design of our circuit.
<img src="./assets/photo.png" />

-Below is the final circuit we built on the breadboard.
<img src="./assets/circuit.png" />

## Testing
In order to test the circuit we had to have the x input certain streams to see if the output of the circuit was correct. If you remeber, the circuit is supposed to out put a 1 if the stream ends in 00, and it's supposed to output a 0 for anything else. We tested multiple inputs of x to ensure that the output was correct. See the video below for a demostration.



## Conclusion




