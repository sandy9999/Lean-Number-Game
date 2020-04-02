**Lemma**
```sh
For all naturals a, a^1 = a.
lemma pow_one (a : mynat) : a ^ (1 : mynat) = a :=
``` 
**Proof**
```sh
begin
    induction a with a ha,
    rw one_eq_succ_zero,
    rw zero_pow_succ,
    refl,
    rw one_eq_succ_zero,
    rw pow_succ,
    rw pow_zero,
    rw one_mul,
    refl,
end
```