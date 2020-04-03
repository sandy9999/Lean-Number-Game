**Lemma**
```sh
If P and Q are true, then P ∧ Q is true. 
example (P Q : Prop) (p : P) (q : Q) : P ∧ Q :=
```
**Proof**
```sh
begin
    split,
    exact p,
    exact q,
end
```