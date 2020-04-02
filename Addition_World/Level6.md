**Lemma**
```sh
For all natural numbers a, b and c, we have
        a + b + c = a + c + b
lemma add_right_comm (a b c : mynat) : a + b + c = a + c + b :=
``` 
**Proof**
```sh
begin
    induction c with c hc,
    rw add_zero,
    rw add_zero,
    refl,
    rw add_succ,
    rw add_succ,
    rw succ_add,
    rw hc,
    refl,
end
```