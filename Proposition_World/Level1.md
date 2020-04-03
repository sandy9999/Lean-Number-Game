**Lemma**
```sh
If P is true, and P ==> Q is also true, then Q is true.
example (P Q : Prop) (p : P) (h : P → Q) : Q :=
``` 
**Proof**
```sh
begin
    exact h(p),
end
```