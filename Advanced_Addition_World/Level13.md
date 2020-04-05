**Lemma**
```sh
For any natural number n, we have n ≠ succ(n).
lemma ne_succ_self (n : mynat) : n ≠ succ n :=
```
**Proof**
```sh
begin
    intro h,
    apply zero_ne_succ 0,
    rw ← one_eq_succ_zero,
    rw succ_eq_add_one at h,
    symmetry at h,
    have g:= eq_zero_of_add_right_eq_self n 1 h,
    symmetry,
    exact g,
end
```