# Moonad Roadmap

## 2018

### Main Accomplishments:

#### Formality

We designed [Formality](https://github.com/moonad/formality), a minimal programming language and proof assistant. Formality can be used not only to develop everyday applications such as dapps and smart-contracts, but to propose and prove mathematical invariants about those. If there is a huge security gap between a weakly typed language like JavaScript to strongly typed ones like TypeScript, Rust and Haskell, then there is an equally huge security gap between those and a proof language like Idris, Coq and Agda. Sadly, those languages weren't build with smart-contracts and dapps and mind, and, as such, are somewhat unpractical for those applications. Formality was designed for Ethereum, which means it focuses on important features those don't, in special minimality and efficiency.

#### Symmetric Interaction Calculus (SIC)

We designed [Symmetric Interaction Calculus](https://github.com/maiavictor/symmetric-interaction-calculus), a programming language isomorphic to Symmetric Interaction Combinators. Studying and exploring it gave us insights about Lamping's [abstract algorithm](https://github.com/maiavictor/abstract-algorithm), the optimal implementation of functional programming languages. This is relevant because SIC is the perfect low-level compile target for high-level languages like Formality: it is inherently parallel, garbage-collection free and beta-optimal. It allows us to run our programs efficiently on the front-end, and cheaply inside a resource-sensitive environment like the EVM. Moreover, through this exploration, we managed to develop techniques to optimize certain functional idioms in an unprecedented manner, as detailed [on this article](https://medium.com/@maiavictor/solving-the-mystery-behind-abstract-algorithms-magical-optimizations-144225164b07).

## 2019

### Main Accomplishments so far:

- Redesign Formality based on [ESCoC](https://github.com/MaiaVictor/ESCoC).

- Prove ESCoC can derive induction for the main λ-encodings: [Scott](https://github.com/moonad/Formality/blob/master/examples/Nat.fm), [Parigot](https://github.com/moonad/Formality/blob/master/examples/Rat.fm), [Church](https://github.com/moonad/Formality/blob/master/examples/Cat.fm).

- Implement several proofs and libraries ([formality-stdlib](https://github.com/moonad/formality-stdlib)).

- A demo of [Moonad](https://github.com/moonad/moonad) ([moonad.org](https://moonad.org/)).

### Current focus

Our first goal in 2019 was to release Moonad, a minimal, Linux-like operating system based on Ethereum/Formality. On it, users would be able to load, check and run Formality code from IPFS/Swarm, run graphical applications (such as text editors), deploy formally verified smart-contracts, etc. While an initial version is available on https://moonad.org/, this project is now paused due to time and resource constraints. We're now focusing on the more immediate goal of polishing Formality, which we believe is more valuable on the short term. Our main priorities now are:

1. Providing a semantics for Formality and identifying a consistent fragment. (Victor)

2. Growing Formality's libraries with important datatypes, algorithms and proofs. (Gabriel and Victor)

3. The Formality-to-EVM compiler. (Leonardo)

4. Formality's landing page, example applications, documentation. (Maisa)

## Comments

### Dilema: abandoning Moonad or externally funding it?

Moon's original idea evolved from a simple browser to something much bigger, a decentralized operating system, Moonad, based on Formality, Swarm/IPFS, Ethereum, etc. Sadly, we also realized building it would require increasing the team's size considerably, and we obviously can't use EF's resources for that. As such, we've decided to downgrade our internal goals, and now we'll focus exclusively on Formality and its EVM/ewasm targets, which are much more relevant and directly appliable to Ethereum.

When it comes to Moonad, though, I still think it is an amazing concept that deserves to be developed. For that reason, I'm writting the [Moonad Manifesto](https://github.com/moonad/manifesto), an informal document explain all of its "why"s. We're considering if we should abandon Moonad entirely, or pursue external funding in order to develop all the non-Ethereum-relevant pieces necessary to build it.

### Why is Formality important to Ethereum?

Formality is valuable to Ethereum because it is a proof language that compiles to the EVM/ewasm, and proofs would have avoided most, if not all, the huge hacks we had. Not everyone agrees with this, though. Many, including [Vitalik](https://www.reddit.com/r/ethereum/comments/7bdm1g/so_can_we_again_have_a_talk_about_formal/dphq7qe/), would argue that, in order for formal proofs to work, you need a "specification", which can, itself, have bugs. While that is absolutely true, it, in practice, is mostly irrelevant. It takes a little bit of practice in proof languages like Agda to realize how those are indeed an enourmous, unprecedented leap in security.

The point that is often missing is that specifications can be much simpler than the code implementing them. For example, it is much easier to write, in code, *"the shortest path between two points in a voxel space"*, than to develop an actual algorithm performing that operation. The catch is that, once an human verifies a small specification, then the machine can verify that the (possibly huge) corresponding implementation is 100% correct and bug-free, no doubts left, no tests needed. And that's amazing! I stand on my grounds that, once we start developing smart contracts in Formality, DAO-like events will be a thing of the past.
