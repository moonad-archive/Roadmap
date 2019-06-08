# Moonad Roadmap

## 2018

### Main Accomplishments:

#### Formality

We designed [Formality](https://github.com/moonad/formality), a minimal programming language and proof assistant. Formality can be used not only to develop everyday applications such as dapps and smart-contracts, but to propose and prove mathematical invariants about those. If there is a huge security gap between a weakly typed language like JavaScript to strongly typed ones like TypeScript, Rust and Haskell, then there is an equally huge security gap between those and a proof language like Idris, Coq and Agda. Sadly, those languages weren't build with smart-contracts and dapps and mind, and, as such, are somewhat unpractical for those applications. Formality was designed for Ethereum, which means it focuses on important features those don't, in special minimality and efficiency.

#### Symmetric Interaction Calculus (SIC)

We designed [Symmetric Interaction Calculus](https://github.com/maiavictor/symmetric-interaction-calculus), a programming language isomorphic to Symmetric Interaction Combinators. Studying and exploring it gave us insights about Lamping's [abstract algorithm](https://github.com/maiavictor/abstract-algorithm), the optimal implementation of functional programming languages. This is relevant because SIC is the perfect low-level compile target for high-level languages like Formality: it is inherently parallel, garbage-collection free and beta-optimal. It allows us to run our programs efficiently on the front-end, and cheaply inside a resource-sensitive environment like the EVM. Moreover, through this exploration, we managed to develop techniques to optimize certain functional idioms in an unprecedented manner, as detailed [on this article](https://medium.com/@maiavictor/solving-the-mystery-behind-abstract-algorithms-magical-optimizations-144225164b07).

## 2019

### Q1 Accomplishments

Gabriel and Victor spent this trimester polishing [Formality](https://github.com/MaiaVictor/Formality). We went from the relatively big (~3k LOC) language that was presented on Devcon to a much smaller (~800 LOC) one, which is relevant because one of the goals of the project is to let Formality be, rather than a monolithic reference implementation, a simple specification that anyone can implement independently. We considered several candidate core languages, such as [ESCoC](https://github.com/MaiaVictor/ESCoC), and explored each one extensively, for example, implementing several [proofs and libraries](https://github.com/moonad/formality-stdlib), in order to arrive at the ideal form, in an extensive filtering and polishing process. We also worked on missing aspects: consistency and complete NASIC compatibility. This isn't proven yet, but we have a proper set of restrictions that make the language terminating and fully NASIC compatible. We're starting an Agda formalization, and an informal specification is available on the repository.

We also started designing [Moonad](https://github.com/moonad/moonad), and developed a [prototypal web client](https://moonad.org/). Since Formality-related work was taking most of our time, though, we decided to put Moonad on hold indefinitely, and focus on the language. We consider this a loss, though, because Moonad could be hugely impacting, as we explained here. We also paused the development of the GPU runtime, in order to focus on Ethereum (EVM & EWASM) targets. This, too, is a loss, as it could be hugely impacting. We believe, with proper investment, such runtime could make Formality one of the fastest functional (if not general) languages on the market. We are currently considering external funding sources to develop those things.

Leonardo initially spent his time on the desktop (Windows/OSX/Linux) client for Moonad. Since the team decided to pause it, though, it didn’t make sense to continue this development, so he moved to work on the [NASIC → EVM](https://github.com/moonad/Nasic-to-EVM) compiler, which is the missing piece to run Formality smart-contracts on Ethereum. He had some trouble due to an EthereumJS SEGFAULT issue, which slowed down the development. Right now, the code is mostly done, but there are still a few bugs, which he is investigating, and writing a wide test suite. Once it is fully operational and tested, we’ll build an ABI around it, allowing Formality smart-contracts to be deployed on Ethereum and to interact with existing contracts.

Maisa was initially assigned to develop (iOS/Android) clients for Moonad. Since, again, the team decided to pause it, she, too, moved to Formality. She developed a [visual animator](https://github.com/moonad/Nasic-Render) for NASIC’s operations on HTML5, and worked with freelancers on our visual identity, logo and landing page. Since she isn’t very experienced with theorem proving (mobile being her main skill), she is currently studying Agda to futurely help with Formality development. Her next goals may include: developing demonstrative Formality contracts, writing posts on how it works, developing documentation, working on our visual identity and landing page.

### Q1 Accomplishments

Briefly (will elaborate later):

1. Restructured [Formality](https://github.com/moonad/formality) (the typed proof language) into many sub-projects, including [Formality-Core](https://github.com/moonad/formality-core), which is our untyped, optimal functional compile target. Formality-Core is amazing and very stable right now, and our plan is to build Formality itself on it. Please check the repository!

2. NASIC to EVM compiler working.

3. Tons of Formality-Core and Formality libs and proofs.

4. Working on starting our own company to develop Formality and its related projects.


## Comments

### Why is Formality important to Ethereum?

Formality is valuable to Ethereum because it is a proof language that compiles to the EVM/ewasm, and proofs would have avoided most, if not all, the huge hacks we had. Not everyone agrees with this, though. Many, including [Vitalik](https://www.reddit.com/r/ethereum/comments/7bdm1g/so_can_we_again_have_a_talk_about_formal/dphq7qe/), would argue that, in order for formal proofs to work, you need a "specification", which can, itself, have bugs. While that is absolutely true, it, in practice, is mostly irrelevant. It takes a little bit of practice in proof languages like Agda to realize how those are indeed an enourmous, unprecedented leap in security.

The point that is often missing is that specifications can be much simpler than the code implementing them. For example, it is much easier to write, in code, *"the shortest path between two points in a voxel space"*, than to develop an actual algorithm performing that operation. The catch is that, once an human verifies a small specification, then the machine can verify that the (possibly huge) corresponding implementation is 100% correct and bug-free, no doubts left, no tests needed. And that's amazing! I stand on my grounds that, once we start developing smart contracts in Formality, DAO-like events will be a thing of the past.
