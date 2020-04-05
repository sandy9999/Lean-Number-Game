**Lemma**
```sh
If a and b are natural numbers such that a + b = 0, then a = 0.
lemma add_right_eq_zero (a b : mynat) : a + b = 0 → a = 0 :=
```
**Proof**
```sh
begin
    intro h,
    rw add_comm at h,
    apply add_left_eq_zero,
    exact h,
end
```