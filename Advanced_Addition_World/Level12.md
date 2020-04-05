**Theorem**
```sh
For any natural number d, we have d + 1 = succ(d).
theorem add_one_eq_succ (d : mynat) : d + 1 = succ d :=
```
**Proof**
```sh
begin
    rw succ_eq_add_one,
    refl,
end
```