**Lemma**
```sh
If P and Q and R are true/false statements, then
        P ==> (Q ==> R) ==> ((P == Q) ==> (P ==> R)).
example (P Q R : Prop) : (P → (Q → R)) → ((P → Q) → (P → R)) :=
``` 
**Proof**
```sh
begin
    intros a b p,
    apply a,
    exact p,
    apply b,
    exact p,
end
```