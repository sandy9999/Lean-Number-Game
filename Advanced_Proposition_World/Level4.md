**Lemma**
```sh
If P, Q and R are true/false statements, then P ⟺ Q and Q ⟺ R together imply P ⟺ R.
lemma iff_trans (P Q R : Prop) : (P ↔ Q) → (Q ↔ R) → (P ↔ R) :=
```
**Proof**
```sh
begin
    intro h,
    cases h with hpq hqp,
    intro i,
    cases i with iqr irq,
    split,
    intro p,
    apply iqr,
    apply hpq,
    exact p,
    intro r,
    apply hqp,
    apply irq,
    exact r,
end
```