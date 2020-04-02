**Definition**
```sh
Whatever the sets P and Q and F are, we make an element of
    Hom(Hom(P,Q),Hom(Hom(Q,F),Hom(P,F))).
example (P Q F : Type) : (P → Q) → ((Q → F) → (P → F)) :=
``` 
**Proof**
```sh
begin
    intros a b c,
    apply b,
    apply a,
    exact c,
end
```