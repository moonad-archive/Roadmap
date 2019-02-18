# Moonad Roadmap

## 2018

### Main Accomplishments:

#### Formality

We designed [Formality](https://github.com/moonad/formality), a minimal programming language and proof assistant. Formality can be used not only to develop everyday applications such as dapps and smart-contracts, but to propose and prove mathematical invariants about those. If there is a huge security gap between a weakly typed language like JavaScript to strongly typed ones like TypeScript, Rust and Haskell, then there is an equally huge security gap between those and a proof language like Idris, Coq and Agda. Sadly, those languages weren't build with smart-contracts and dapps and mind, and, as such, are somewhat unpractical for those applications. Formality was designed for Ethereum, which means it focuses on important features those don't, in special minimality and efficiency.

#### Symmetric Interaction Calculus

We designed [Symmetric Interaction Calculus](https://github.com/maiavictor/symmetric-interaction-calculus), a programming language isomorphic to Symmetric Interaction Combinators. Studying and exploring it gave us insights about Lamping's [abstract algorithm](https://github.com/maiavictor/abstract-algorithm), the optimal implementation of functional programming languages. This is relevant because SIC is the perfect low-level compile target for high-level languages like Formality: it is inherently parallel, garbage-collection free and beta-optimal. It allows us to run our programs efficiently on the front-end, and cheaply inside a resource-sensitive environment like the EVM. Moreover, through this exploration, we managed to develop techniques to optimize certain functional idioms in an unprecedented manner, as detailed [on this article](https://medium.com/@maiavictor/solving-the-mystery-behind-abstract-algorithms-magical-optimizations-144225164b07).

## 2019

Our first goal in 2019 is to release Moonad, a platform similar to Remix, where users will be able to download and edit Formality code, run live apps and build smart-contracts. A very early (started a few days ago) version is available at [https://moonad.org/](https://moonad.org). Someday around March it will be released. After that, the team will focus mostly on developing Formality libraries and proofs, as well as improving Moonad with more features. There are many things that we wish to do:

### On Formality

- Formality-to-EVM compiler (high priority)

- Base libraries (numbers, lists and other structures, functors, monads, algebra, equality...)

- Crypto libraries (hashes, signatures, encryption, merkle structures, EVM, ...)

- Rendering libraries (colors, vector graphs, fonts, matrices, quaternions...)

- Formality-in-Formality

- GPU evaluators (CUDA, OpenCL, Metal...).

- Documentation and learning materials

- Several smart-contracts / DApps on it, like:

    - A "hello world" calculuator that proves it does the algebra correctly

    - A TheDAO-like app that proves it can't be stolen

    - An exchange that proves you're always able to withdrawal your holdings

    - Lottery that proves its fairness

    - Games that prove invariants (nobody enters certain area without certain items, etc.)

    - Whatever our creativity allows us to think

### On Moonad

- A rich IDE (syntax highlighting, hyperlinks, proof search, Swarm/IPFS imports, etc.)

- Improve the DApp renderer: sound, image, animations, etc.

- Ethereum account management (anything MyCrypto doe)

- Ethereum contract interaction (Remix-like features like testing, deploying Formality contracts, etc.)

- Ethereum blockchain explorer (but displaying proofs!)

- And so on

We don't want to commit to any of those in any particular order, though. I find it is more productive to just develop what is needed in order of priority, which may shift depending on community reception, future ideas, marketing insights and so on. But we could arrange a more rigid timeline if demanded.

### Worklog

Victor and Gabriel focused in completing the design of Formality. Getting it right from the beginning is considered extremelly important because, once a vast amount of libraries are built upon it, there is no going back. As such, Formaliy went through several redesigns in a short timespan. Eventually, we settled in a minimalist design very close to the Calculus of Constructions, which he called [ESCoC](https://github.com/maiavictor/escoc). This solves several earlier problems, including implementation complexity (it is down from 3500 to 500 lines of code), expressivity (several datatype-related  limitations were solved by adopting inductive λ-encodings) and security (implementing a termination checker is now much more feasible). The almost-final version is available [here](https://github.com/moonad/formality), including several [libraries and numerical proofs](https://github.com/moonad/Formality/blob/master/main.formality) built using Formality itself.

Leonardo focused in ...

Maisa focused in ...
