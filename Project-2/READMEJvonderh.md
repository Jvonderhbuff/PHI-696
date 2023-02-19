# Project 2

Your second project will require you to answer each of the 10 questions below.  You will be expected to open a pull request with your initial answers by the second class meeting, giving you one week to work on these problems. You and your peers will then have one week to work together to refine your respective initial answers, so they are ready for final submission. Once your pull requests have been reviewed and merged to the development branch, I will review them, then merge to the master branch. 

```
Tip #1: Carefully study the Baader, et. al. selections assigned on bisimulation; it is deceptively subtle, and quite powerful. 
Tip #2: Google is still your friend. So is stackexchange...
Tip #3: Work together to solve these problems, even for initial submissions and when you do, document this in github. 
Tip #4: Work together as a team. 
```

1. Let V be a vocabulary of ALCI consisting of a role name "P". Interpret part_of as "x is a part of y". Using this role name, define the following formulas in this language:
```
  (a)  PP that says that x is a proper part of y
  PP= ∀part_of
  (b)  iPP that says that y is a proper part of x
  iPP= ∀part_of
  (c)  iP that says that y has x as part
  ip= ∀part_of-
  (d)  O that says that x overlaps y
  O= ∀part_of^∃part_of
  (e)  D that says that x and y are disjoint
  D= ∀~part_of
```

2. Use your axioms from question 1 as the basis of an ALCI T-Box. Supplement this T-box with whatever other axioms you like, as well as an A-box, so that you ultimately construct a knowledge base K = (T,A). Provide a _model_ of K. This may be graphical or symbolic or both. 
PP= ∀part_of
ipp= ∀part_of
ip= ∀part_of-
O= ∀part_of^∃part_of
D= ∀~part_of

Lazarus: PP, x
(Lazarus, City)
City: Ipp, Y
Lazarus: Part_of City
City: Part_of Lazarus
Proper part: x, y
overlaps: x, y
Disjoint: none

3. Translate the following first-order logic axioms into ALCI: 
```
(a) ∀x∃y∀z(R(x,y) ∧ R(x,z) ∧ R(y,z))
∀R.(∃R.^∀R.)
(b) ∃x∀y∃z(R(x,y) ∧ R(x,z) ∧ R(y,z))
∃R.(∀R.^∃R.)
(c) ∀y(R(x, y) → ∃x(R(y, x) ∧ ∀y(R(x, y) → A(y))))
Note that there is an unbound x in this axiom.
∀R.(
(d) (∀y)(R(x, y) → A(y)) ∧ (∃y)(R(x, y) ∧ B(y))
Note that there is an unbound x in this axiom
∀R.(
```
4. Provide an interpretation I<sub>1</sub> for ALC and an interpretation I<sub>2</sub> for ALCN - each distinct from any interpretation covered in class so far - and construct a bisimulation that demonstrates ALCN is more expressive than ALC. Use the [mermaid syntax](https://github.com/mermaid-js/mermaid) of markdown to provide a graphical representation of your work. Feel free to use the [mermaid live editor](https://mermaid.live/) when diagramming. 

Interpretation:

Bisimulation:

5. Provide an interpretation I<sub>1</sub> for ALC and an interpretation I<sub>2</sub> for ALCN - each distinct from any interpretation covered in class so far - and construct a bisimulation that _does not_ demonstrate ALCN is more expressive than ALC. Use the [mermaid syntax](https://github.com/mermaid-js/mermaid) of markdown to provide a graphical representation of your work. Feel free to use the [mermaid live editor](https://mermaid.live/) when diagramming. 

Interpretation:

Bisimulation:

6. Explain the difference - using natural language - between the description logic expressions:
  ```
  (a) ∃r.C and ∀r.C
  The first is saying that there is something such that it is an instance of the concept r and the second says that every instance of C is an instance of concept r.
  (b) ∃r-.C and ∀r-.C
  The first claims that there is some instance of C where it is the inversion of the concept r and the second claims that all instances of C are an inversion of concept r.
  (c) <=nr and <=nr.C
  The first claims that there is something that is less than or equal to the concept nr and the second claims that there is something that is less than or C which is an instance of concept nr.
  (d) ∃r-.C and ∃r-.{a} 
  The first claims that there is some instance of C which is an inversion of concept r and the second claims that the singleton set of a includes an instance of an inversion of the concept of r.
```

7. There is a delightfully helpful subreddit called "ELI5" which stands for something like "explain it like I'm 5" where users post conceptually challenging questions and other users attempt to provide explanations in simple, jargon-free, terms that presumably a 5 year-old could understand. Using this as a model, explain the _finite model property_. Be sure to provide a simple example and explain when the property might be important, and when it is not so important. 

The finite model property is 

8. Following up on the preceding , explain the _tree model property_. Be sure to provide a simple example and explain when the property might be important, and when it is not so important. 

The Tree model property is 

9. Open the Protege editor and create object properties for each of the role names that you constructed in question 1. You should have at least 6 object properties. Assert in the editor that P is a sub-property of O, that P is transitive, and that O is symmetric. Next, add individuals - a, b, c - to the file and assert that c is part of a and that c overlaps b. Running the reasoner should reveal - highlighted in yellow if you select the individual c - that c overlaps a. Using the discussion in the selections from chapter 4 of the Baader, et. al. text as a guide, explain how the tableau algorithm is generating this inference. Also, provide a screenshot of the results of your reasoner run with c highlighted. 

The tableau algorithm is generating this inference by 

10. Following up on your work in question 9, adjust/add/remove/etc. object properties and individuals in your Protege file so that when you run a reasoner in Protege, you return the following consequences: 
```
  (a) a is a proper part of b and disjoint from e
  (b) a overlaps c
  (c) a is part of b, b is part of f, and a is part of f
  (e) There are no parts between a and g in common
```
Provide a screenshot of your results here. 
