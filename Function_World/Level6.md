**Definition**
```sh
Whatever the sets P and Q and R are, we make an element of 
Hom(Hom(P,Hom(Q,R)),Hom(Hom(P,Q),Hom(P,R))).
example (P Q R : Type) : (P → (Q → R)) → ((P → Q) → (P → R)) :=
``` 
**Proof**
```sh
begin
    intros f j p,
    apply f,
    exact p,
    apply j,
    exact p,
end
```