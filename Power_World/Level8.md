**Lemma**
```sh
For all naturals a and b, we have (a + b)^2 = a^2 + b^2 + 2ab.
lemma add_squared (a b : mynat) : (a + b) ^ (2 : mynat) = a ^ (2 : mynat) + b ^ (2 : mynat) + 2 * a * b :=
``` 
**Proof**
```sh
begin
    induction b with b hb,
    rw add_zero,
    rw mul_zero,
    rw add_zero,
    rw two_eq_succ_one,
    rw zero_pow_succ,
    rw add_zero,
    refl,
    rw mul_succ,
    rw two_eq_succ_one,
    repeat {rw pow_succ},
    repeat {rw pow_one},
    rw add_succ,
    rw <- add_succ,
    rw add_mul,
    rw mul_add,
    rw mul_add,
    rw mul_succ,
    rw succ_mul,
    rw mul_succ,
    rw succ_mul,
    rw <- two_eq_succ_one,
    rw add_succ,
    rw two_eq_succ_one,
    rw succ_mul,
    rw one_mul,
    rw add_mul,
    simp,
end
```