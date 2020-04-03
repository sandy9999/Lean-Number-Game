**Lemma**
```sh
If P and Q are true/false statements, then P ∧ Q ==> Q ∧ P.
lemma and_symm (P Q : Prop) : P ∧ Q → Q ∧ P :=
```
**Proof**
```sh
begin
    intro h,
    cases h with p q,
    split,
    exact q,
    exact p,
end
```