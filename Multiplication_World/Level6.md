**Lemma**
```sh
For all natural numbers a and b, we have
        succ(a) x b = ab + b
lemma succ_mul (a b : mynat) : succ a * b = a * b + b :=
``` 
**Proof**
```sh
begin
    induction b with b hb,
    rw mul_zero,
    rw mul_zero,
    rw add_zero,
    refl,
    rw mul_succ,
    rw mul_succ,
    rw add_succ,
    rw add_succ,
    rw hb,
    rw add_right_comm,
    refl,
end
```