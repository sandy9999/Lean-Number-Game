**Lemma**
```sh
For any propositions P and Q, we always have P ==> (Q ==> P).
example (P Q : Prop) : P → (Q → P) :=
``` 
**Proof**
```sh
begin
    intros p q,
    exact p,
end
```