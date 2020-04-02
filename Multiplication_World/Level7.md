**Lemma**
```sh
Addition is distributive over multiplication. In other words, for all natural numbers a, b and t, we have
        (a + b) x t = at + bt
lemma add_mul (a b t : mynat) : (a + b) * t = a * t + b * t :=
``` 
**Proof**
```sh
begin
    induction a with a ha,
    rw zero_mul,
    rw zero_add,
    rw zero_add,
    refl,
    rw succ_mul,
    rw succ_add,
    rw succ_mul,
    rw ha,
    rw add_right_comm,
    refl,
end
```