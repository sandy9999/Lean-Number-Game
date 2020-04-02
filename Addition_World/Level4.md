**Lemma**
```sh
On the set of natural numbers, addition is commutative. In other words, for all natural numbers a and b, we have
        a + b = b + a.
lemma add_com (a b : mynat) : a + b = b + a :=
``` 
**Proof**
```sh
begin
    induction b with b hb,
    rw add_zero,
    rw zero_add,
    refl,
    rw add_succ,
    rw succ_add,
    rw hb,
    refl,
end
```