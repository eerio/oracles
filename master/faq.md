- Does it make sense to consider a category of all NP-complete problems, with morphisms as poly-time reductions between different instances?
> https://cstheory.stackexchange.com/questions/3074/a-category-of-np-complete-problems

- Term algebras are initial objects in the category of algebras over a given signature
> https://en.wikipedia.org/wiki/Term_algebra#:~:text=From%20a%20category%20theory%20perspective,all%20algebras%20in%20the%20category.

- Under the Curry-Howard correspondence, natural deduction corresponds to simply typed lambda calculus

- Any inductive type can be encoded in System F as polymorphic functions  
  Parametricity is anti-classical
> https://xavierleroy.org/CdF/2018-2019/6.pdf

- Numeric functions expressible in STLC = extended polynomials

- Minimal logic + ex falso quodlibet = intuitionistic logic  
  Intuitionistic logic + excluded middle = classical logic
> https://xavierleroy.org/CdF/2018-2019/4.pdf

- Is ex falso quodlibet modeled by the exception monad?

- Glivenko, 1929: Classical logic proves Phi iff intuitionistic logic proves ~~Phi

- Grädel's theorem: on the class of finite structures with a successor relation, the collection of polynomial-time decidable properties coincides with those expressible in the Horn-fragment of existential second-order logic
> https://cstheory.stackexchange.com/questions/869/is-there-a-logic-without-induction-that-captures-much-of-p?rq=1

- Barrington's theorem: polynomial-size bounded-width branching programs have the same computation power as Boolean formulas
> https://blog.computationalcomplexity.org/2008/11/barringtons-theorem.html

- Theory of species, derivative of a data structure, quantum field theory
> http://lambda-the-ultimate.org/node/1957

- How to add axiom of dependent/countable choice to classical logic?
> https://ieeexplore.ieee.org/document/6280455

- How to add dependent types to classical logic?
> Compiling with dependent types: https://www.williamjbowman.com/resources/wjb-dissertation.pdf  
> This chapter explicitly avoids control effects and dependent types to focus on type preservation. However, in general, we may want to combine the two. Herbelin (2005) shows that unrestricted use of call/cc and throw in a language with $\Sigma$ types and equality leads to an inconsistent system.  The inconsistency is caused by type dependency on terms involving control effects.  Herbelin (2012) solves the inconsistency by constraining types to depend only on negative-elimination-free (NEF) terms, which are free of effects. This restriction makes dependent types compatible with classical reasoning enabled by the control operators.

- Impredicativity of Set + excluded middle + axiom of unique choice is inconsistent
> http://pauillac.inria.fr/~herbelin/talks/cic.pdf

- Continuations must be used linearly to avoid control effects, which are known to cause inconsistency with dependent types
> https://www.williamjbowman.com/resources/wjb-dissertation.pdf

- No Continuation-passing-style translation is possible along the same lines for small $\Sigma$-types and sum types with dependent case
> https://dl.acm.org/doi/10.1145/509799.503043

- Typed Exceptions and Continuations Cannot Macro-Express Each Other
> https://link.springer.com/content/pdf/10.1007/3-540-48523-6_60.pdf

- How type theory is the syntax of category theory
> https://ncatlab.org/nlab/show/type+theory

- Physics, Topology, Logic and Computation: A Rosetta Stone  
  parallel execution = proofs carried out in parallel = disjoint union of cobordisms = tensor product of morphisms
> https://arxiv.org/pdf/0903.0340.pdf

- Type theory is both a logic and a computation: this is the C-H isomorphism
> https://math.stackexchange.com/a/2811256/876802

- Homotopy Type Theory should eat itself (but so far, it’s too big to swallow); related to the limitations of the expressibility of the metalanguage:
> https://homotopytypetheory.org/2014/03/03/hott-should-eat-itself/

- What is the expressibility of simply-typed lambda calculus, really?
> Complexity class: REG (https://mathoverflow.net/a/296879)
> wtf???
> (1. FO with arbitrary predicates = AC^0)
> (2. FO in a signature with only the order relation = star-free languages)
> (3. https://nguyentito.eu/2018-11-scalp.pdf - ELEMENTARY)
> (4. tak, to jest REG: https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.23.8845&rep=rep1&type=pdf)
> (5. depends on the input/output representation!!! 
  https://cstheory.stackexchange.com/a/52102)

- logic, category and type theory connection:
  * Logic: minimal logic = simply typed lambda calculus (positive, implicational fragment of intuitionistic logic)
  * Category: Cartesian closed categories
  * Type theory: finite products only so curry/uncurry enough,
  because we can construct finite products from binary products?

- Computational trilogy: programming languages, type theory and algebraic topology
> https://ncatlab.org/nlab/show/computational+trilogy


1. znaleźć programy dla aksjomatów
  DC = quote
  Peirce = call/cc
  ZF = ?
  AC = ?
  CH = ? (forcing)
2. programowanie w teorii zbiorów?
3. strony izomorfizmu: rachunek lambda, logika, języki, klasy złożoności,
    automaty? co jeszcze?
4. przykłady niespójnych systemów logicznych
5. w Coq = konstruktywnie nie da się praktycznie nic nie policzyć
6. co zrobić żeby można było policzyć? Writer monad dla printów?
  jakie są możliwe skutki uboczne póki co? czy one odpowiadają konkretnym
  aksjomatom? np. pętlenie się (call/cc), exceptions (Markov's rule, Friedman's trick), global cell (~CH (forcing)), delimited continuations (double negation shift)
7. znaczenie twierdzeń:
  - axiom: system primitive
  - soundness theorem: compiler
  - completeness theorem: debugger
  - incompleteness theorem: infinite loops
  - axiom of choice trivial in intuitionistic logic, monster in classical


https://math.stackexchange.com/questions/2862220/curry-howard-for-an-imperative-programming-language
https://www.xn--pdrot-bsa.fr/slides/inria-junior-02-15.pdf

descriptive complexity theory:
FO: AC0
FO + Transitive closure operator = NL, nondeterministic logarithmic space
FO + Least fixed point operator = P, polynomial deterministic time
Existential SO = NP


I have to design a programming language and write an interpreter for it
in Haskell. I want the language to be functional and need it to support
the following features:
-static typing with polymorphism (like in Caml or Haskell without classes)
-type inference
-GADTs with full pattern matching and exhaustiveness checking
the syntax of the language has to be based on SML/Caml or Haskell


encoding of data types: scott encoding, church encoding, functional pearls
http://kseo.github.io/posts/2016-12-13-scott-encoding.html

existential types in ml:
http://gallium.inria.fr/~remy/mpri/cours.pdf

Każdy program może mieć tylko jednego while:
https://www.cs.cornell.edu/~kozen/Papers/kat.pdf
https://en.wikipedia.org/wiki/Structured_program_theorem
https://dl.acm.org/doi/pdf/10.1145/256167.256195
https://www.sciencedirect.com/science/article/pii/S1567832611000191
http://lem12.uksw.edu.pl/images/6/62/Mirkowska-II-147-165.pdf


closures + tail-call optimization => continuations
https://stackoverflow.com/q/75299540/3622836

deriving functor in ghc
https://byorgey.wordpress.com/2010/03/03/deriving-pleasure-from-ghc-6-12-1/?fbclid=IwAR0i7UXI1S6z0zTAKGjedf1cPcQK_E5vT0hOUYwe_9gbWBk7v3DhdD5lyow

związek tk i logiki
https://ncatlab.org/nlab/show/internal+logic

fajne slajdy o tk?
https://camdar.io/static/h4t/stuff/10/categoryTheory.pdf

tk w SMLu
https://jeremykun.com/2013/04/07/a-sample-of-standard-ml-and-the-treesort-algorithm/

existential types
https://cs.stackexchange.com/q/65746

gadts in SML: (bardzo ciekawy gist!!!)
https://gist.github.com/bobatkey/8272004

mocny filmik o teorii zaawansowanych typów dancyh, tutaj: GADTs,
np. ze nie sa funktorialne
https://www.youtube.com/watch?v=w3n8NXaADdg

continuations in SML:
https://www.cs.cmu.edu/~rwh/papers/callcc/popl91.pdf

PLT Redex
https://redex.racket-lang.org/

dobra.
-czy inferencję typów można dosłać w II terminie?
tak!
-czy język musi mieć printa?
1. to ma być funkcyjny język na JPP, zatem:
-język musi być typowany
-typowanie musi być statyczne, wspierać polimorfizm i inferencję typów
-musi mieć pattern matching i GADTs w pełnej ogólności
-'lambda calculus forms the basis of all functional programming languages'
-czyli nasz formalizm to rachunek lambda i nie ma co pierdolić!!
  żadne alternatywne definicje typu combinatory logic
-można robic polimorfizm poza systemem F, tj. np. subtyping,
  ale my nie będziemy wychodzić poza rachunek lambda
-laziness seems to be independent from the type system -
  lazy evaluation only impacts the runtime, whereas
  the types only mattter at the compile time and may be discarded after
  the type checking step

można przeszukać nieskończony zbiór w skończonym czasie
https://www.cs.bham.ac.uk/~mhe/papers/exhaustive.pdf

weryfikacja SML w Coq
https://types22.inria.fr/files/2022/06/TYPES_2022_paper_15.pdf
http://web4.ensiie.fr/~dubois/tphols00-corr.pdf

semantyka monadyczna
https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.136.1656&rep=rep1&type=pdf

Bayes rule in haskell
http://www.randomhacks.net.s3-website-us-east-1.amazonaws.com/2007/02/22/bayes-rule-and-drug-tests/

ważna książka Pierce'a
https://www.cis.upenn.edu/~bcpierce/tapl/

w ml kontynuacje moga sie nie dac zrobic
https://www.cs.cmu.edu/~rwh/papers/callcc/jfp.pdf

język Plotkina z game semantics!!
https://en.wikipedia.org/wiki/Programming_Computable_Functions


to jest chyba rozwiązanie zadania jednocześnie!!!
o tym dlaczego gadt są trudne pod względem inferencji typów:
https://www.microsoft.com/en-us/research/uploads/prod/2016/02/outsidein-icfp09.pdf

inferencja typów dla GADT, taka jak w Haskellu ale prosta:
https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/gadt-pldi.pdf

-coq type inference is not known to be decidable but seems so?
  even though it has dependent types?
-use hs-to-coq to prove my compiler

papery:
https://www.cis.upenn.edu/~sweirich/talks/GADT.pdf
fajny paper o polimorfizmie:
http://lucacardelli.name/papers/onunderstanding.a4.pdf


zajebisty!!! artykuł o TK w funkcyjnym
A Neighborhood of Infinity: A Partial Ordering of some Category Theory applied to Haskell
http://blog.sigfpe.com/2010/03/partial-ordering-of-some-category.html


polynomial System F:
-Simona delarocce

linear types for linear algebra
https://www.cl.cam.ac.uk/~nk480/numlin.pdf

Hindley-Milner isn't compatible with e.g. overloading (ad-hoc polymorphism)
and subtyping

what's difficult in Haskell but not in Scala?
zipWithN

what can't be typed in haskell?
-functions on church numerals
https://stackoverflow.com/questions/23995736/example-of-type-in-system-f-that-is-not-available-in-hindley-milner-type-inferen?rq=1

lazy vs eager evaluation doesn't matter when there is no general recursion

różnica między let-polimorfizmem, a beta-redukcją:
https://cstheory.stackexchange.com/a/39835

haskell doesn't have dependent types
existential types and GADTs are both GHC extensions

https://stackoverflow.com/questions/23995736/example-of-type-in-system-f-that-is-not-available-in-hindley-milner-type-inferen?rq=1


how strong a type theory do we need?
https://queuea9.wordpress.com/2010/01/17/how-strong-a-type-theory-do-we-need/


https://ncatlab.org/nlab/show/game+theory
open games from compositiona game theory are morphisms
in symmetrical monoidal categories.
the internal language of symmetric monoidal categories
is the linear logic
tu nie ma nic chyba:
https://arxiv.org/pdf/1603.04641.pdf
https://arxiv.org/pdf/1904.11287.pdf
to jest mocne!:
https://www.cs.ox.ac.uk/people/julian.hedges/papers/Thesis.pdf
co do podejścia teorio-growego: czy mi nie chodziło dokładnie o
  wiki: game semantics?
game semantics:
https://www.cs.uoregon.edu/research/summerschool/summer18/lectures/ghica1.pdf


fajny paper
https://xavierleroy.org/CdF/2018-2019/2.pdf

system typów w core haskella, System FC:
https://repository.brynmawr.edu/cgi/viewcontent.cgi?article=1015&context=compsci_pubs


w Haskellu mozna zaimplementowac SK calculus w systemie typow
i nawet zrobic cos czego typowanie sie nie konczy! (duza Omega)
https://stackoverflow.com/a/34003628/3622836
ciekawe!!

fajny paper o inferencji
http://gallium.inria.fr/~fpottier/mpri/cours01.pdf

principal type property

ML with call/cc is unsound
https://www.cis.upenn.edu/~bcpierce/types/archives/1991/msg00034.html

+Twierdzenie Rice'a
Twierdzenia godla o niezupelnosci:
https://stackoverflow.com/a/21437375/3622836
nie mozemy miec systemu typow, ktory bedzie sound i complete,
ale ktory jednoczesnie bedzie miec decidable checker


GADTs as initial algebras:
https://www.cl.cam.ac.uk/~mpf23/papers/Types/gadtif.pdf

existential types in ocaml:
https://stephenebly.medium.com/an-introduction-to-existential-types-25c130ba61a4


każdy program z whilem może być symulowany programem z maks. jednym whilem
https://www.cs.cornell.edu/~kozen/Papers/kat.pdf


NetKAT:
https://www.cs.cornell.edu/~jnfoster/papers/frenetic-netkat.pdf

fajna konferencja
https://popl20.sigplan.org/track/POPL-2020-tutorialfest#program


sequent calculus, lambda-mu calculus, continuations
https://en.wikipedia.org/wiki/Lambda-mu_calculus

Curry-Howard
https://xavierleroy.org/CdF/2018-2019/4.pdf
https://en.wikipedia.org/wiki/List_of_Hilbert_systems
https://ncatlab.org/nlab/show/minimal+logic


fajna prezentacja o typach egzystencjalnych: (że one = ADTs?)
https://www.ps.uni-saarland.de/courses/seminar-ws02/ExistentialTypes.slides.pdf
