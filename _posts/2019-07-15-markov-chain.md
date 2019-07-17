This is Anagha, and this is my attempt to explain what are Markov Chains. 
This is where I'm going to explain it. 

A Markov Chain is a model that outlines the statistical probability of a random process. They are mathematical systems that use a previous state to determine the probability distribution of the current state. Markov chains are often processes with the Markov property. The Markov property states that the probability distribution of future states depends only on the present state (also refered to as a memoryless random process). However this definition only really covers homogeneous discrete time Markov chains, there are also inhomogeneous Markov chains. 

Markov chains are made of two things: 
* A State Space 
* A Probability Transition Function 

A Markov Chain can either have a discrete state space, which is the set of possible values for random variables, or a discrete index set, time. More often than not, when the term 'Markov Chain' is used it refers to a Discrete Time Markov Chain (DMTC).  

##### Modeling
To model a Markov Chain we use probabilistic automaton which includes the probability of a given transition into the transition function, turning it into a transition matrix. Every state in the state space is included once as a row and again as a column, and each cell in the matrix tells you the probability of transitioning from its row's state to its column's state. If the Markov chain has N possible states, the matrix will be an N x N matrix, such that entry (I, J) is the probability of transitioning from state I to state J. Additionally, the transition matrix must be a stochastic matrix, whose entries in each row must add up to exactly 1, because each row represents its own probability distribution.

A Markov Chain model includes:
* State space
* A transition matrix
* An initial state across the state space

There are also several important properties of Markov Chain 
* Reducibility - A Markov Chain is irreducible if there is a positive probability of transition between any two states. 
* Periodicity - A Markov Chain is periodic if it returns to a state only at multiples of some integer greater than 1.
* Transience + Recurrence - A state is said to be transcient if there is a non-zero probability that we will never return to that state. A state is said to be a positive recurrent if there is a finite amount of steps expected to return to that state or is a null recurrent otherwise. 
* Ergodicity - A state is ergodic if it is aperiodic and postive recurrent. 
* Absorbing state - A state is said to be absorbing when it is impossible to leave this state. 
