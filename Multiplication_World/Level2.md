**Lemma**
```sh
For any natural number m, we have
        m x 1 = m.
lemma mul_one (m : mynat) : m * 1 = m :=
``` 
**Proof**
```sh
begin
    induction m with m hm,
    rw zero_mul,
    refl,
    rw one_eq_succ_zero,
    rw mul_succ,
    rw mul_zero,
    rw zero_add,
    refl,  
end
```