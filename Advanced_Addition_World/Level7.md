**Theorem**
```sh
For all natural numbers a, b and t,
        a + t = b + t <==> a = b
theorem add_right_cancel_iff (t a b : mynat) :  a + t = b + t ↔ a = b :=
```
**Proof**
```sh
begin
    split,
    exact add_right_cancel a t b,
    intro h,
    induction t with t ht,
    rw add_zero,
    rw add_zero,
    exact h,
    rw add_succ,
    rw add_succ,
    apply succ_eq_succ_of_eq,
    exact ht,
end
```