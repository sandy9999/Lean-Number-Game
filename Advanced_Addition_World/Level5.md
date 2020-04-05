**Theorem**
```sh
On the set of natural numbers, addition has the right cancellation property. In other words, if there are natural numbers a,b and c such that a + t = b + t then we have a = b.
theorem add_right_cancel (a t b : mynat) : a + t = b + t → a = b :=
```
**Proof**
```sh
begin
    intro h,
    induction t with t ht,
    rw add_zero at h,
    rw add_zero at h,
    exact h,
    rw add_succ at h,
    rw add_succ at h,
    apply ht,
    apply succ_inj,
    exact h,
end
```