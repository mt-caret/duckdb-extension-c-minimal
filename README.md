A minimal example of building a duckdb extension using the C API (i.e. via `duckdb_extension.h`).

Currently only works with the bleeding edge duckdb version:

```
$ ./duckdb -unsigned
v1.1.4-dev5147 3240832cdd
Enter ".help" for usage hints.
D LOAD '~/.../duckdb-extension-c-minimal/src/capi_quack';
D SELECT multiply_numbers_together(1,2);
┌─────────────────────────────────┐
│ multiply_numbers_together(1, 2) │
│              int64              │
├─────────────────────────────────┤
│                2                │
└─────────────────────────────────┘
```
