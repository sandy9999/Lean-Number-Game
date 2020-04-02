**Lemma**
```sh
For any natural number n, we have
        succ(n) = n + 1.
lemma succ_eq_add_one (n : mynat) : succ n = n + 1 :=
``` 
**Proof**
```sh
begin
    induction n with n hn,
    rw one_eq_succ_zero,
    rw zero_add,
    refl,
    rw succ_add,
    rw hn,
    refl,
end
```