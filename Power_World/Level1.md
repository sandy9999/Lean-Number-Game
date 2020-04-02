**Lemma**
```sh
0^0 = 1.
lemma zero_pow_zero (0 : mynat) ^ (0 : mynat) = 1 :=
``` 
**Proof**
```sh
begin
    rw pow_zero,
    refl,
end
```