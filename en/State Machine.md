TOPIC: State Machine
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Heather; hbloomer@mozilla.net; mdn:hbloomer

# State Machine

A state machine is a mathematical abstraction used to design algorithms. A state machine reads a set
of inputs and changes to a different state based on those inputs.

A state is a description of the status of a system waiting to execute a transition. A transition is
a set of actions to execute when a condition is fulfilled or an event received. In a state diagram,
circles represent each possible state and arrows represent transitions between states.

Looking at the final state, you can discern something about the series of inputs leading to that state.

There are two types of basic state machines:

**deterministic finite state machine**:

This kind allows only one possible transition for any allowed input. This is like the "if" statement
in that `if x == true then doThis else doThat` is not possible.
The computer must perform one of the two options.

**non-deterministic finite state machine**:

Given some state, an input can lead to more than one different state.

Figure 1: Deterministic Finite State Machine

In Figure 1, the state begins in State 1; the state changes to State 2 given input 'X',
or to State 3 given input 'Y'.

Figure 2: Non-Deterministic Finite State Machine

In Figure 2, given input 'X', the state can persist or change to State 2.

Note that any regular expression can be represented by a state machine.

## Learn More

### General Knowledge

- [Finite-state machine](https://en.wikipedia.org/wiki/Finite-state%20machine) on Wikipedia
- [UML state machine](https://en.wikipedia.org/wiki/UML%20state%20machine) on Wikipedia
- [Moore machine](https://en.wikipedia.org/wiki/Moore%20machine) on Wikipedia
- [Mealy machine](https://en.wikipedia.org/wiki/Mealy%20machine) on Wikipedia
