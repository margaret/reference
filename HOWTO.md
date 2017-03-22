# How to do things

Notes for myself because I keep forgetting. A lot of these notes are in the context of work and not necessarily generally applicable. A lot of this is stuff I asked people at work, or just top google results for the questions.

## Haskell

#### How do you load the interpreter (`ghci`) with all the modules for a project imported?
Do `stack ghci` from the project root.

#### Does `stack ghci` look at the `stack.yaml` or just `hitl.cabal`?
> both - my understanding is that stack.yaml is used to specify options that hitl.cabal can't specify, but that might be naive - but in particular stack.yaml is useful for specifying how to resolve dependencies
> hitl.cabal will state which dependencies (external projects) you want to pull in, stack.yaml states where to pull those dependencies from - which stackage LTS to use


## Misc system things

### Check which process is using a port on OS X
One of these, depending on your particular OS
```bash
lsof -n -i4TCP:$PORT | grep LISTEN
lsof -n -iTCP:$PORT | grep LISTEN
lsof -n -i:$PORT | grep LISTEN
```
From [stackoverflow](http://stackoverflow.com/questions/4421633/who-is-listening-on-a-given-tcp-port-on-mac-os-x)

### Wrest control of audio back to keyboard (OSX) from overzealous headphones
`sudo killall coreaudiod`
