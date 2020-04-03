**Lemma**
```sh
In the maze of logical implications above, if P is true then so is U.
lemma maze (P Q R S T U: Prop)
(p : P)
(h : P → Q)
(i : Q → R)
(j : Q → T)
(k : S → T)
(l : T → U)
: U :=
``` 
**Proof**
```sh
begin
    apply l,
    apply j,
    apply h,
    exact p,
end
```