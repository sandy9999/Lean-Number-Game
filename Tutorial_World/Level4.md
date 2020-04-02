**Lemma**
```sh
For all natural numbers a, we have
    a + succ(0) = succ(a).
lemma add_succ_zero (a : mynat) : a + succ(0) = succ(a) :=
``` 
**Proof**
```sh
begin
    rw add_succ,
    rw add_zero,
    refl,
end
```