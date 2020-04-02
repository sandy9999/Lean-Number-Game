**Lemma**
```sh
If succ(a) = b, then succ(succ(a)) = succ(b).
lemma example3 (a b : mynat) (h : succ a = b) : succ(succ(a)) = succ(b) :=
``` 
**Proof**
```sh
begin
    rw h,
    refl,
end
```