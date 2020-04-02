**Definition**
```sh
Whatever the sets P and Q are, we make an element of Hom(Hom(P,Q),Hom(Hom(Q,∅),Hom(P,∅))).
example (P Q F : Type) : (P → Q) → ((Q → F) → (P → F)) :=
``` 
**Proof**
```sh
begin
    intros f g p,
    apply g,
    apply f,
    exact p,
end
```