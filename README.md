# LLVM_test

Generate LLVM IR:

`clang main.c -emit-llvm -S`

Generate CFG:
```
llvm-as-7 < main.ll | opt-7 -analyze -dot-cfg
dotty cfg.main.dot
```

JIT
```
clang -c -emit-llvm main.c -o t.bc
lli-7 t.bc
```
