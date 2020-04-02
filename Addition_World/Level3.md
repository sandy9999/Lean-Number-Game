**Lemma**
```sh
For all natural numbers a, b, we have
        succ(a) + b = succ(a + b).
lemma succ_add (a b : mynat) : succ a + b = succ(a + b) :=
``` 
**Proof**
```sh
begin
    induction b with b hb,
    rw add_zero,
    rw add_zero,
    refl,
    rw add_succ,
    rw add_succ,
    rw hb,
    refl,
end
```