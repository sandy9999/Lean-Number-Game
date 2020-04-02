**Lemma**
```sh
On the set of natural numbers, addition is associative. In other words, for all natural numbers a, b and c, we have
        (a + b) + c = a + (b + c)
lemma add_assoc (a b c : mynat) : (a + b) + c = a + (b + c) :=
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
    rw add_succ,
    rw hc,
    refl,
end
```