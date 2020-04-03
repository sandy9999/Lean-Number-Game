**Lemma**
```sh
If P and Q are true/false statements, then
        Q ⟹ (P v Q).
example (P Q : Prop) : Q → (P ∨ Q) :=
```
**Proof**
```sh
begin
    intro a,
    right,
    exact a,
end
```