**Lemma**
```sh
For all natural numbers a, b and c, we have
        a(bc) = b(ac)
lemma mull_left_comm (a b c : mynat) : a * (b * c) = b * (a * c) :=
``` 
**Proof**
```sh
begin
    induction c with c hc,
    rw mul_zero,
    rw mul_zero,
    rw mul_zero,
    refl,
    rw mul_succ,
    rw mul_add,
    rw mul_succ,
    rw mul_add,
    rw hc,
    rw mul_comm a b,
    refl,
end
```