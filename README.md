# Bug in cljs parsing of --compile-opts passed by deps.edn alias via :main-opts

Works if you replace the spaces with `,` in --compile-opts EDN (`,` is treated as whitespace in EDN)

`--compile-opts" "{:optimizations :advanced}"`

vs

`"--compile-opts" "{:optimizations,:advanced}"`

```
clj -Abuild
clj -m cljs.main --serve
```
