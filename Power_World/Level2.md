**Lemma**
```sh
0^succ(m) = 0.
lemma zero_pow_succ (m : mynat) : (0 : mynat) ^ (succ m) = 0 :=
``` 
**Proof**
```sh
begin
    rw pow_succ,
    rw mul_zero,
    refl,
end
```