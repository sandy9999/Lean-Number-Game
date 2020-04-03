**Lemma**
```sh
If P is a proposition then P ==> P.
lemma imp_self (P : Prop) : P → P :=
``` 
**Proof**
```sh
begin
    intro p,
    exact p,
end
```