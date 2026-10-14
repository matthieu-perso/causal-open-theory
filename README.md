# Causal Open Theory

Machine-checked causal deep learning. This repository owns mechanisms, interventions, and risk under an intervened law. It depends on [OpenTheory](https://github.com/matthieu-perso/open-theory) for observational risk, network semantics, and training.

OpenTheory bounds risk under the training distribution:

```text
population risk ≤ ε_approx + ε_opt + ε_gen
```

Causal Open Theory names the map from that law to a new one. An intervention replaces a structural assignment and pushes the observational law forward. The quantity to bound is then interventional risk, invariance across environments, or identification error.

## What lives here

- Mechanisms, graphs, and exogenous noise
- Interventions and the laws they induce
- Identifiability and invariance
- Theorems that spend an OpenTheory observational budget under an intervened law

## What stays in OpenTheory

- Observations, IID samples, empirical and population risk
- Network semantics, optimization, and observational generalization
- Attention-mask “causal” forward passes, and ablations of a network under a fixed data law

A network appears here as a mechanism or a representation map. Its observational error is an OpenTheory hypothesis. Do not reimplement ridge, attention, or concentration in this repository.

The first join is: if the training law and the intervened law differ by a formalized mechanism, interventional risk is at most the observational excess risk plus the error from that mechanism change.
