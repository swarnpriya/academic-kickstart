---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Propositions"
subtitle: ""
summary: ""
authors: []
tags: []
categories: []
date: 2020-07-02T20:55:31-04:00
lastmod: 2020-07-02T20:55:31-04:00
featured: false
draft: false
math: true

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

**Coq represents propositions as types**

-   **What are propositions?**

    Propositions are statements representing an idea which can be true
    or false. It is a bearer of truth or falsity. But how do we know
    whether it represents truth or falsity? The truth or falsity of the
    propositional statements should be established with proofs.

-   **Propositions in Coq**

    Coq represents propositions as types (here these types represent the
    types that live in universe $P$). But as we know we should have a
    proof which establishes the truth or falsity of these propositional
    types. The inhabitants of a propositional type serve as proofs of
    the proposition. **What are inhabitants?** The inhabitants of a type
    are the values that can be described through canonical terms
    ($normal$ and $closed$ terms) of this type. **What are closed
    terms?** A term is closed if it has no free variables. **What are
    normal terms?** A term is in normal form if it cannot be further
    reduced, no reduction rule applies to it and it has reduced to a
    unique value or a term.

-   **Propositions**

    Logical connectives are used to join two or more logical statements
    (propositions). For joining two statements we use binary logical
    connectives like or, and, implication etc. These binary connectives
    can be extended to join more logical statements. Compound
    propositions can be formed using basic propositional logics. In the 
    table below the last two examples comes under the category called
    \"First-order logic\" while the rest comes under the category
    \"Propositional logic\". \"Higher order logic is a different
    category which is stronger than the \"first order logic\" but weaker
    than \"set theory\". Higher order logic can argue about the
    properties about the elements over the domain in addition over the
    elements itself.

    All these propositions are provable if it has an inhabitant.

    <!DOCTYPE html>
<html>
<body>

<h2>Propositions and First Order Connectives</h2>

<table style="width:100%">
<col style="width:25%">
	<col style="width:15%">
	<col style="width:15%">
  <col style="width:45%">
  <tr>
    <th>Name</th>
    <th>Representation</th> 
    <th>How to read?</th>
    <th>Explanation</th>
  </tr>
  <tr>
    <td>Equality</td>
    <td>a=b</td>
    <td>a equals b</td>
    <td>a and b are equivalent in every scenario. They are computationally equal.</td>
  </tr>
  <tr>
    <td>True</td>
    <td>T</td>
    <td>true</td>
    <td>proof of truth</td>
  </tr>
    <tr>
    <td>False</td>
    <td>F</td>
    <td>false</td>
    <td>proof of false</td>
  </tr>
  <tr>
    <td>Negation</td>
    <td> <text>$\neg$P </text></td>
    <td>not P</td>
    <td>if P is true then $\neg$ P is false and vice versa.</td>
  </tr>
    <tr>
    <td>Conjunction</td>
    <td>P $\wedge$ Q</td>
    <td>P and Q</td>
    <td>P $\wedge$ Q evaluates to true only when both P and Q have inhabitants that provides proofs for both P and Q to be true.</td>
  </tr>
    <tr>
    <td>Disjunction</td>
    <td>P \/ Q</td>
    <td>P or Q</td>
    <td>P \/ Q evaluates to true when either P or Q have inhabitants that provides proofs for either P or Q to be true.</td>
  </tr>
    <tr>
    <td>Implication</td>
    <td>P $\rightarrow$ Q</td>
    <td>P implies Q</td>
    <td>It is also read as "If P then Q". It evaluates to false if and only if P is true and Q is false.</td>
  </tr>
    <tr>
    <td>Equivalence</td>
    <td>P $\equiv$ Q</td>
    <td>P if and only if Q</td>
    <td>It evaluates to true only when both P and Q are true or both are false.</td>
  </tr>
  <tr>
    <td>Universal Quantifier</td>
    <td>$\forall$ x: X. P(x)</td>
    <td>forall x in X, P(x) </td>
    <td>P can be satisfied or proved to be true for all values of x present in the set X.</td>
  </tr>
    <tr>
    <td>Existential Quantifier</td>
    <td>$\exists$ x: X. P(x)</td>
    <td>forsome x in X, P(x)</td>
    <td>P can be satisfied or proved to be true for some value (not all values) of x present in the set X.</td>
  </tr>
  
</table>

</body>
</html>

**Now lets talk about propositions in Coq**

As we know Coq is a typed language, which means every expression (ofcourse sensible ones) are well-typed (has an associated type). Hence any proposition statement we write or try to prove in Coq has a type called $Prop$. All propositional statements have type "Prop" in Coq regardless of whether they are true or false. In addition to being as types in Coq, propositions are also "first-class entity" that can be manipulated in all possible ways. We can also give a name to a propositional statement and later use that name. 

- **De Morgan's Law**

$\neg$(P$\wedge$Q)$\iff$($\neg$P)\/($\neg$Q)
and
$\neg$(P \/ Q)$\iff$($\neg$P)$\wedge$($\neg$Q)










   