# How to do things

Notes for myself because I keep forgetting. A lot of these notes are in the context of work and not necessarily generally applicable. A lot of this is stuff I asked people at work, or just top google results for the questions.

## Haskell

#### How do you load the interpreter (`ghci`) with all the modules for a project imported?
Do `stack ghci` from the project root.

#### Does `stack ghci` look at the `stack.yaml` or just `hitl.cabal`?
> both - my understanding is that stack.yaml is used to specify options that hitl.cabal can't specify, but that might be naive - but in particular stack.yaml is useful for specifying how to resolve dependencies
> hitl.cabal will state which dependencies (external projects) you want to pull in, stack.yaml states where to pull those dependencies from - which stackage LTS to use
