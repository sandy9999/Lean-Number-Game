**Lemma**
```sh
From P ==> Q and Q ==> R we can deduce P ==> R.
lemma imp_trans (P Q R : Prop) : (P → Q) → ((Q → R) → (P → R)) :=
``` 
**Proof**
```sh
begin
    intros a b p,
    apply b,
    apply a,
    exact p,
end
```