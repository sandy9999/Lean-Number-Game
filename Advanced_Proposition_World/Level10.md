**Lemma**
```sh
If P and Q are true/false statements, then
        (P ∧ ¬P)⟹Q.
lemma contra (P Q : Prop) : (P ∧ ¬ P) → Q :=
```
**Proof**
```sh
begin
    intro f,
    cases f with p np,
    rw not_iff_imp_false at np,
    exfalso,
    apply np,
    exact p,
end
```