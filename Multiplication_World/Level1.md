**Lemma**
```sh
For all natural numbers m, we have
        0 x m = 0.
lemma zero_mul (m : mynat) : 0 * m = 0 :=
``` 
**Proof**
```sh
begin
    induction m with m hm,
    rw mul_zero,
    refl,
    rw mul_succ,
    rw hm,
    rw add_zero,
    refl,
end
```