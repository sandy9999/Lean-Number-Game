**Lemma**
```sh
For all naturals a, m, n, we have (a^m)^n = a^(mn).
lemma pow_pow (a m n : mynat) : (a ^ m) ^ n = a ^ (m * n) :=
``` 
**Proof**
```sh
begin
    induction n with n hn,
    rw pow_zero,
    rw mul_zero,
    rw pow_zero,
    refl,
    rw pow_succ,
    rw mul_succ,
    rw pow_add,
    rw hn,
    refl,
end
```