**Theorem**
```sh
Two natural numbers are equal if and only if their successors are equal.
theorem succ_eq_succ_iff (a b : mynat) : succ a = succ b ↔ a = b :=
```
**Proof**
```sh
begin
    split,
    exact succ_inj,
    exact succ_eq_succ_of_eq,
end
```