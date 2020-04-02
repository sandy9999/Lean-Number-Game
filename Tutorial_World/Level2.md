**Lemma**
```sh
If x and y are natural numbers, and y = x + 7, then 2y = 2(x+7).
lemma example2 (x y z : mynat) (h : y = x + 7) : 2 * y = 2 * (x + 7) :=
``` 
**Proof**
```sh
begin
    rw h,
    refl,
end
```