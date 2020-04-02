**Definition**
```sh
We define an element of Hom(P,Hom(Q,P)).
example (P Q : Type) : P → (Q → P) :=
``` 
**Proof**
```sh
begin
    intro p,
    intro q,
    exact p,
end
```