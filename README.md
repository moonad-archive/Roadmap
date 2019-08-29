# Moonad Roadmap

## 2018

### Main Accomplishments:


- Designed the first version of [Formality](https://github.com/moonad/formality) with the aim of developing an efficient proof language for smart-contracts and applications. It included native datatypes and a prototypal interaction-net compiler.

- Designed [Symmetric Interaction Calculus](https://github.com/maiavictor/symmetric-interaction-calculus), a parallel model of computation with applications to efficient, optimal and parallel evaluation of functional programs.

- Explored it and [wrote a blog post](https://medium.com/@maiavictor/solving-the-mystery-behind-abstract-algorithms-magical-optimizations-144225164b07) detailing our insights.

## 2019

### Q1 Accomplishments

- Implemented and explored [Cedille-Core](https://github.com/MaiaVictor/Cedille-Core), a minimal proof language designed by Aaron Stump.

- Based on it, developed a 800 LOC type-theory compatible with optimal reductions, previously called Formality, which we now call [Elementary Affine Type Theory (EA-TT)](https://github.com/moonad/elementary-affine-type-theory).

- Based on [Symmetric Interaction Combinators](https://pdfs.semanticscholar.org/1731/a6e49c6c2afda3e72256ba0afb34957377d3.pdf), developed [Elementary Affine Net (EA-Net)](https://github.com/moonad/elementary-affine-net), an interaction net system and compile target for EA-TT. 

- [Stated and proved several theorems on EA-TT]([proofs and libraries](https://github.com/moonad/Elementary-Affine-Type-Theory-libs)), to validate and explore its expressivity.

- Wrote a [blog post](https://medium.com/@maiavictor/introduction-to-formality-part-1-7ae5b02422ec) introducing it. 

- Started working on the [Moonad Operating System](https://github.com/moonad/moonad), but stopped to focus in developing an efficient proof language.

- Started a [compiler to the EVM](https://github.com/moonad/Elementary-Affine-Net-to-EVM). 

- Developed a HTML/JS [animation tool](https://github.com/moonad/Elementary-Affine-Net-Render) for EA-Net.

### Q2 Accomplishments

- Developed [Elementary-Affine-Core (EA-TT)](https://github.com/moonad/elementary-affine-core), the untyped version of EA-TT.

- Restructured [Formality](https://github.com/moonad/formality) (the typed proof language) into many sub-projects:

  - [Formality-Core (FM-TT)](https://github.com/moonad/formality-core): Formality's untyped core, which extends EA-Core with numbers.

  - [Formality-Net (FM-Net)](https://github.com/moonad/formality-net): Formality's interaction-net, an efficient compile target which extends EA-Net with numbers.

  - Formality-Type-Theory (FM-TT): Formality's underlying type theory, which extends EA-TT with numbers (ongoing).

- Wrote several [FM-Core libraries](https://github.com/moonad/Formality-Core/tree/master/examples), including:

  - In-place array library, thanks to linear types!

  - Lists, numbers, tuples and other core FP libs.

  - Ongoing implementation of FM-Core within itself, which will be the base of Formality-Lang.

  - Keccak!

  - A toy game as a demo of its power (and of non-Turing-complete languages!).

- Finished the [EA-Net->EVM](https://github.com/moonad/Elementary-Affine-Net-to-EVM) compiler. Still needs optimizations. FM-Net next.

- A prototypal [C-backend](https://github.com/moonad/Formality-Net/blob/master/c/fm-net) for FM-Net. (Soon we'll have C++/LLVM experts optimizing it!)

- Wrote a [Github Wiki](https://github.com/moonad/Formality-Core/wiki) for Formality-Core.

### Q3 Accomplishments

Way too many things to type here now :) Formality is getting mature, nearing a stable 0.1 release, its base libs are growing, everything is great. Check out https://github.com/formality! Yay. (For any questions, feel free to open an issue here.)
