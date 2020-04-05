**Theorem**
```sh
On the set of natural numbers, addition has the left cancellation property. In other words, if there are natural numbers a,b and c such that a + b = a + c then we have b = c.
theorem add_left_cancel (t a b : mynat) : t + a = t + b → a = b :=
```
**Proof**
```sh
begin
    intro h,
    induction t with t ht,
    rw zero_add at h,
    rw zero_add at h,
    exact h,
    rw succ_add at h,
    rw succ_add at h,
    apply ht,
    apply succ_inj,
    exact h,
end
```

(Or)

```sh
begin
    rw add_comm t a,
    rw add_comm t b,
    exact add_right_cancel a t b,
end
```