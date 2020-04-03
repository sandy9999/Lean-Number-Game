**Lemma**
```sh
If P, Q and R are true/false statements, then P ∧ Q and Q ∧ R together imply P ∧ R.
lemma and_trans (P Q R : Prop) : P ∧ Q → Q ∧ R → P ∧ R :=
```
**Proof**
```sh
begin
    intro a,
    cases a with p q,
    intro b,
    cases b with q r,
    split,
    exact p,
    exact r,
end
```