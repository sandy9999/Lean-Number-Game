**Lemma**
```sh
For all natural numbers n, we have 0 + n = n.
lemma zero_add (n : mynat) : 0 + n = n :=
``` 
**Proof**
```sh
begin
    induction n with n hn,
    rw add_zero,
    refl,
    rw add_succ,
    rw hn,
    refl,
end
```