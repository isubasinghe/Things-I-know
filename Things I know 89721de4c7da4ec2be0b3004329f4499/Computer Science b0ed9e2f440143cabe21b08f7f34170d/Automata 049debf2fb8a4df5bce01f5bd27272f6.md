# Automata

## DFA

[https://en.wikipedia.org/wiki/Deterministic_finite_automaton](https://en.wikipedia.org/wiki/Deterministic_finite_automaton)

## NFA

[https://en.wikipedia.org/wiki/Nondeterministic_finite_automaton](https://en.wikipedia.org/wiki/Nondeterministic_finite_automaton)

## Regex

Matching a string with a given regex is as simple as testing if a given string can be recognised by a DFA that recognises that particular regular expression. 

This has the implication that testing a regex match has a theoretical worst runtime of O(r), where r is the maximum length the automata. Unfortunately, some languages ship with a backtracking algorithm that has exponential runtime cost, therefore we need to be aware of this when optimising for performance. 

**How to build a regex engine?** 

Parse a regex string and build a NFA as you go along, then run the Powerset construction algorithm to turn this NFA into the equivalent DFA.  If a string can be successfully recognised by this DFA, then it is also in the regular language the DFA was based on.

## DFA minimisation

[https://en.wikipedia.org/wiki/DFA_minimization#Brzozowski's_algorithm](https://en.wikipedia.org/wiki/DFA_minimization#Brzozowski's_algorithm)

## Powerset construction

[https://en.wikipedia.org/wiki/Powerset_construction](https://en.wikipedia.org/wiki/Powerset_construction)

- Resources

    [https://swtch.com/~rsc/regexp/regexp1.html](https://swtch.com/~rsc/regexp/regexp1.html)