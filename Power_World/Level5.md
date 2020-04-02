**Lemma**
```sh
For all naturals m, a, b, we have a^(m+n) = (a^m)(a^n).
lemma pow_add (a m n : mynat) : a^(m + n) = a^m * a^n :=
``` 
**Proof**
```sh
begin
    induction m with m hm,
    rw zero_add,
    rw pow_zero,
    rw one_mul,
    refl,
    rw succ_add,
    rw pow_succ,
    rw pow_succ,
    rw hm,
    rw mul_right_comm,
    refl,
end
```