**Lemma**
```sh
If P and Q are true/false statements, then
        (¬Q⟹¬P)⟹(P⟹Q).
lemma contrapositive2 (P Q : Prop) : (¬ Q → ¬ P) → (P → Q) :=
```
**Proof**
```sh
begin
    by_cases p : P; by_cases q : Q,
    repeat {cc},
end
```