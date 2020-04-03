**Lemma**
```sh
If P and Q are true/false statements, then
        P v Q ⟹ Q v P.
lemma or_symm (P Q : Prop) : P ∨ Q → Q ∨ P :=
```
**Proof**
```sh
begin
    intro h,
    cases h with p q,
    right,
    exact p,
    left,
    exact q,
end
```