**Theorem**
```sh
For all naturals a and b, if we assume succ(succ(a)) = succ(succ(b)), then we can deduce a = b.
theorem succ_succ_inj {a b : mynat} (h : succ(succ(a)) = succ(succ(b))) :  a = b := 
```
**Proof**
```sh
begin
    apply succ_inj,
    apply succ_inj,
    exact h,
end
```