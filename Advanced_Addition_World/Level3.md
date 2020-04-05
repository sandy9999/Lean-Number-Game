**Theorem**
```sh
For all naturals a and b, a = b ==> succ(a) = succ(b).
theorem succ_eq_succ_of_eq {a b : mynat} : a = b → succ(a) = succ(b) :=
```
**Proof**
```sh
begin
    intro e,
    rw succ_eq_add_one,
    rw succ_eq_add_one,
    rw e,
    refl,
end
```