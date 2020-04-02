**Lemma**
```sh
Multiplication is distribution over addition. In other words, for all natural numbers a, b and t, we have
        t(a + b) = ta + tb.
lemma mul_add (t a b : mynat) : t * (a + b) = t * a + t * b :=
``` 
**Proof**
```sh
begin
    induction b with b hb,
    rw add_zero,
    rw mul_zero,
    rw add_zero,
    refl,
    rw mul_succ,
    rw add_succ,
    rw mul_succ,
    rw hb,
    rw add_assoc,
    refl,
end
```