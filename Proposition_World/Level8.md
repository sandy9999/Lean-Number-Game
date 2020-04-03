**Lemma**
```sh
If P and Q are propositions, and P⟹Q, then ¬Q⟹¬P.
lemma contrapositive (P Q : Prop) : (P → Q) → (¬ Q → ¬ P) :=
```
**Proof**
```sh
begin
    intro a,
    intro b,
    rw not_iff_imp_false,
    intro p,
    apply b,
    apply a,
    exact p,
end
```