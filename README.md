# Moonad Roadmap

## 2018

### Main Accomplishments:

#### Formality

We designed [Formality](https://github.com/moonad/formality), a minimal programming language and proof assistant. Formality can be used not only to develop everyday applications such as dapps and smart-contracts, but to propose and prove mathematical invariants about those. If there is a huge security gap between a weakly typed language like JavaScript to strongly typed ones like TypeScript, Rust and Haskell, then there is an equally huge security gap between those and a proof language like Idris, Coq and Agda. Sadly, those languages weren't build with smart-contracts and dapps and mind, and, as such, are somewhat unpractical for those applications. Formality was designed for Ethereum, which means it focuses on important features those don't, in special minimality and efficiency.

#### Symmetric Interaction Calculus

We designed [Symmetric Interaction Calculus](https://github.com/maiavictor/symmetric-interaction-calculus), a programming language isomorphic to Symmetric Interaction Combinators. Studying and exploring it gave us insights about Lamping's [abstract algorithm](https://github.com/maiavictor/abstract-algorithm), the optimal implementation of functional programming languages. This is relevant because SIC is the perfect low-level compile target for high-level languages like Formality: it is inherently parallel, garbage-collection free and beta-optimal. It allows us to run our programs efficiently on the front-end, and cheaply inside a resource-sensitive environment like the EVM. Moreover, through this exploration, we managed to develop techniques to optimize certain functional idioms in an unprecedented manner, as detailed [on this article](https://medium.com/@maiavictor/solving-the-mystery-behind-abstract-algorithms-magical-optimizations-144225164b07).

## 2019

In 2019, our goal is to develop Formality dapps and smart-contracts, as well as Moonad, a platform for developing and running those. This includes:

- An efficient Formality-to-EVM compiler.

- Ethernal, a separate blockchain capable of running Formality contracts natively.

- On Moonad: a rich Formality IDE (syntax highlighting, hyperlinks, proof checking, proof search, etc.).

- On Moonad: a renderer for interactive Formality dapps with monadic blockchain access.

- On Formality: completion of its design and specificaition.

- On Formality: a plenty of example smart-contracts and dapps.

- Documentation and learning material.

### Q1. 2019

#### Summary

Victor and Gabriel focused in completing the design of Formality. Getting it right from the beginning is considered extremelly important because, once a vast amount of libraries are built upon it, there is no going back. As such, Formaliy went through several redesigns in a short timespan. Eventually, we settled in a minimalist design very close to the Calculus of Constructions, which he called [ESCoC](https://github.com/maiavictor/escoc). This solves several earlier problems, including implementation complexity (it is down from 3500 to 500 lines of code), expressivity (several datatype-related  limitations were solved by adopting inductive λ-encodings) and security (implementing a termination checker is now much more feasible). The almost-final version is available [here](https://github.com/moonad/formality), including several [libraries and numerical proofs](https://github.com/moonad/Formality/blob/master/main.formality) built using Formality itself.

Leonardo focused in ...

Maisa focused in ...
