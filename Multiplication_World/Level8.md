**Lemma**
```sh
Multiplication is commutative.
lemma mull_comm (a b : mynat) : a * b = b * a :=
``` 
**Proof**
```sh
begin
    induction a with a ha,
    rw zero_mul,
    rw mul_zero,
    refl,
    rw succ_mul,
    rw mul_succ,
    rw ha,
    refl,
end
```