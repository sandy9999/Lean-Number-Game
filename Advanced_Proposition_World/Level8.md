**Lemma**
```sh
If P, Q and R are true/false statements, then
        P ∧ (Q v R) ⟺ (P ∧ Q) v (P ∧ R).
lemma and_or_distrib_left (P Q R : Prop) : P ∧ (Q ∨ R) ↔ (P ∧ Q) ∨ (P ∧ R) :=
```
**Proof**
```sh
begin
    split,
    intro h,
    cases h with p qr,
    cases qr with q r,
    left,
    split,
    exact p,
    exact q,
    right,
    split,
    exact p,
    exact r,
    intro i,
    cases i with ipq ipr,
    split,
    cases ipq with p q,
    exact p,
    left,
    cases ipq with p q,
    exact q,
    split,
    cases ipr with p r,
    exact p,
    right,
    cases ipr with p r,
    exact r,
end
```