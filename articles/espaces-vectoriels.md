# Introduction aux espaces vectoriels

Les espaces vectoriels constituent l'un des concepts fondamentaux de l'algèbre linéaire. Ils généralisent les notions de vecteurs dans le plan et l'espace à des contextes plus abstraits.

## Définition formelle

Un espace vectoriel sur un corps $\mathbb{K}$ est un ensemble $E$ muni de deux opérations :

1. **Addition vectorielle** : $(u, v) \mapsto u + v$
2. **Multiplication scalaire** : $(\lambda, v) \mapsto \lambda v$

Ces opérations doivent satisfaire les axiomes suivants :

$$
\forall u, v, w \in E, \forall \lambda, \mu \in \mathbb{K}
$$

- $(u + v) + w = u + (v + w)$ (associativité)
- $u + v = v + u$ (commutativité)
- $\exists 0 \in E : u + 0 = u$ (élément neutre)
- $\lambda(u + v) = \lambda u + \lambda v$ (distributivité)

## Exemple de code

Voici une implémentation simple d'un espace vectoriel en Python :

```python
class VectorSpace:
    def __init__(self, dimension):
        self.dimension = dimension
    
    def add(self, v1, v2):
        return [v1[i] + v2[i] for i in range(self.dimension)]
    
    def scalar_multiply(self, scalar, vector):
        return [scalar * v for v in vector]

