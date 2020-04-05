**Theorem**
```sh
Zero is not the successor of any natural number.
theorem succ_ne_zero (a : mynat) : succ a ≠ 0 := 
```
**Proof**
```sh
begin
    symmetry,
    exact zero_ne_succ a,
end
```