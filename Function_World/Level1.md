**Definition**
```sh
Given an element of P and a function from P to Q, we define an element of Q.
example (P Q : Type) (p : P) (h : P --> Q) : Q :=
``` 
**Proof**
```sh
begin
    exact h(p),
end
```