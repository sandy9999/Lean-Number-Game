**Lemma**
```sh
Multiplication is associative. In other words, for all natural numbers a, b and c, we have
        (ab)c = a(bc)
lemma mul_assoc (a b c : mynat) : (a * b) * c = a * (b * c) :=
``` 
**Proof**
```sh
begin
    induction c with c hc,
    rw mul_zero,
    rw mul_zero,
    rw mul_zero,
    refl,
    rw mul_succ,
    rw mul_succ,
    rw mul_add,
    rw hc,
    refl,
end
```