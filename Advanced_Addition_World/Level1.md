**Theorem**
```sh
For all naturals a and b, if we assume succ(a) = succ(b), then we can deduce a = b.
theorem succ_inj' {a b : mynat} (hs : succ(a) = succ(b)) :  a = b := 
```
**Proof**
```sh
begin
    apply succ_inj,
    exact hs,
end
```

(Or)

```sh
begin
    revert hs,
    exact succ_inj,
end
```