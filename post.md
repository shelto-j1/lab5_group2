# Lab 05: Finite State Machine Design

## Overview and Motivation

This lab delves into the design of a finite state machine (FSM), specifically tasked with reading binary numbers and determining their divisibility by three. This lab not only strengthens the understanding of sequential logic circuits but also serves as a practical application of digital design principles. This task underscores the significance of FSMs in parsing input streams and showcases the dynamic interaction between state transitions and output responses.

<img src="./assets/overview.png" />

## Lab Objectives

- Design a deterministic finite automaton (DFA) to assess the divisibility of binary inputs by three.
- Manage the states of the DFA using JK flip-flops to track and transition between states.
- Construct two combinational logic circuits for determining the next state and output based on the current state and input bit.
- Create a function table to define the logic relations between the state (Q values), input bits, and the desired output.
- Use K-Maps for each output to optimize the circuit design through logical minimization.
- Build the circuit using Logisim software to validate functionality before physical assembly.
- Assemble and test the physical circuit to ensure it meets design specifications and functional requirements.

## Materials
- IC data sheets

- PB-503 breadboard prototyping station

- Wires and connection tools

- Logic Probes

- Logic Switches

- Push Button

- 7404 NOT gate IC

- 7408 AND gate IC

- 7486 XOR gate IC

- 7476 JK Flip Flop IC

- Resistors

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

After assembling the circuit, we moved on to the testing phase, which involved inputting binary numbers through a simple mechanism: toggling the x switch. To add a "1" to the binary number, we flipped the switch to "1"; to add a "0", we flipped it to "0". The circuit updated with each push of the button designated as the clock, adding the new bit to the end of the binary string. We conducted tests using numbers both divisible and not divisible by 3, closely observing the circuit's response, which aligned perfectly with our initial designs and expectations based on the Deterministic Finite Automata.

The testing revealed that the circuit accurately reflected the state of divisibility by 3. When the binary number was not divisible by 3 (not in an accepting state), the probe light remained off. Conversely, when a number divisible by 3 was input (returning to an accepting state), the probe light turned on, indicating the desired outcome. Additionally, we evaluated the circuit's CLEAR function, which allows for resetting the system. By toggling the reset switch off and then on, we successfully cleared the circuit's memory, enabling us to start anew with a different binary number. This level of functionality and control during testing affirmed the circuit's design and operational efficacy.

In order to test the circuit we had to have the x input certain streams to see if the output of the circuit was correct. If you remeber, the circuit is supposed to out put a 1 if the stream ends in 00, and it's supposed to output a 0 for anything else. We tested multiple inputs of x to ensure that the output was correct.  The testing phase included scenarios that were designed to simulate potential edge cases, such as long sequences of zeros, which could potentially trip up the state transition logic if not correctly accounted for in the design

See the video below for a demostration.


## Conclusion

To conclude, with the lab, we began with a clear objective: to design and construct a circuit capable of detecting whether a binary input stream ends with "00". This venture required not only a robust understanding of digital logic but also the practical skills necessary for realization. Initially, we laid the  foundation by designing a Deterministic Finite Automata (DFA), which provided a structured plan detailing state transitions. This was crucial as it translated our concept into a plan complete with expected behaviors for each state transition.

Following the DFA, we created a state table, acting as both a roadmap and a checklist to ensure the circuit behaved as expected, detailing the specific transitions and outputs for each possible input. The transition from this table to the creation of a function table was pivotal, as it outlined the logic levels for the circuit's inputs and outputs, guiding the actual design. This detailed planning phase highlighted the importance of a solid theoretical foundation, transforming understanding into actionable steps.

With the function table in hand, we developed K-maps for simplification. This step was essential for reducing the circuit's complexity, highlighting the importance of efficiency in design. It allowed us to minimize the components needed, paving the way for a more streamlined and error-resistant construction. The process of bringing these designs to life on a breadboard, where theory met reality, was both challenging and enlightening. We navigated the process of assembling the circuit, learning the importance of practical skills in circuit construction and the value of iterative troubleshooting and refinement.

The primary achievement of this lab was the successful translation of theoretical concepts into a functional digital circuit. Our design accurately identified binary sequences ending in "00", validating our approach through rigorous testing. This experience showed the experience of engineering, where design, testing, and refinement are crucial for success. It provided us with valuable stuff in the importance of planning, the efficiency of design through simplification, and the critical nature of practical skills in realizing theoretical concepts. This learning experience has equipped us with insights that will benefit us going forward.



