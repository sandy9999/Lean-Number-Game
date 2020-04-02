**Definition**
```sh
Given an element of P we can define an element of U.
example : (P Q R S T U: Type)
(p : P)
(h : P → Q)
(i : Q → R)
(j : Q → T)
(k : S → T)
(l : T → U)
: U :=
``` 
**Proof**
```sh
begin
    apply l,
    apply j,
    apply h,
    exact p,
end
```