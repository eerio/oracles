# oracles
Proof of concept: Oracle-Oriented Programming

Turing machines are too strong. We practically cannot reason about them in general, due to the implications of Rice's theorem.

No perfect programming language exists - as no perfect natural language exists. Different tribes have short words for frequently used things.

Things in real life are typed in the sense of natural languages - you can ,,eat a sandwich'', but you wouldn't say you ,,breathe a sandwich''; even though at the end of the day, it's all just atoms, untyped. Same with programming languages - even though in the end it all compiles to untyped assembly language instructions, at a higher level we operate in a typed world. We need types in our language, as also we need a way to describe objects and their transformations.

The data and the functions are not something we create. It's something we discover or merely describe. We describe data using a logic (e.g. first order logic). Thus we can describe infinite data like
V("start node"), V("end node"), E("start node", "end node")
Forall n: Nat, V(n), E(n, n+1)

We want to strenghten our type theory to have more Theorems for free
We want to weaken our type theory to be able to compute more


Objects of our language are graphs.
A ,,type'' is a model of a logical sentence
i.e. a ,,type'' is described exactly by a logical sentence

FO: can talk about vertices, edges
MSO1: can talk about vertices, edges, sets of vertices
MSO2: can talk about vertices, edges, sets of vertices and edges

equality is graph isomorphism

Trakhtenbrot's theorem: it is undecidable whether FO sentence
  can be realized by a finite undirected graph




What is in
