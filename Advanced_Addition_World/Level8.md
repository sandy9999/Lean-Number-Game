**Lemma**
```sh
If a and b are natural numbers such that
        a + b = a, then b = 0
lemma eq_zero_of_add_right_eq_self (a b : mynat) : a + b = a → b = 0 :=
```
**Proof**
```sh
begin
    intro h,
    apply add_left_cancel,
    exact h,
end
```