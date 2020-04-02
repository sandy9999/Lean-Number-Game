**Lemma**
```sh
For all naturals m, 1^m = 1.
lemma one_pow (m : mynat) : (1 : mynat) ^ m = 1 :=
``` 
**Proof**
```sh
begin
    induction m with m hm,
    rw pow_zero,
    refl,
    rw pow_succ,
    rw mul_one,
    rw hm,
    refl,
end
```