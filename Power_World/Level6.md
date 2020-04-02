**Lemma**
```sh
For all naturals a, b, n, we have (ab)^(n) = (a^n)(b^n).
lemma mul_pow (a b n : mynat) : (a * b) ^ n = a^n * b^n :=
``` 
**Proof**
```sh
begin
    induction n with n hn,
    rw pow_zero,
    rw pow_zero,
    rw pow_zero,
    rw one_mul,
    refl,
    rw pow_succ,
    rw pow_succ,
    rw pow_succ,
    rw hn,
    simp,
end
```