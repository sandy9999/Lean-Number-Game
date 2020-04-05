**Lemma**
```sh
If a and b are natural numbers such that a + b = 0, then b = 0.
lemma add_left_eq_zero (a b : mynat) (H : a + b = 0) : b = 0 :=
```
**Proof**
```sh
begin
    cases b with d,
    rw add_zero at H,
    refl,
    rw add_succ at H,
    exfalso,
    apply succ_ne_zero,
    exact H,
end
```