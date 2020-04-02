**Lemma**
```sh
For any natural number m, we have
        1 x m = m.
lemma one_mul (m : mynat) : 1 * m = m :=
``` 
**Proof**
```sh
begin
    induction m with m hm,
    rw mul_zero,
    refl,
    rw one_eq_succ_zero,
    rw mul_succ,
    rw add_succ,
    rw add_zero,
    rw <- one_eq_succ_zero,
    rw hm,
    refl,
end
```