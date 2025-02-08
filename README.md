A minimal example of building a duckdb extension using the C API (i.e. via `duckdb_extension.h`),
based off of [duckdb/extension-template-c](https://github.com/duckdb/extension-template-c).

```
$ ./duckdb -unsigned
v1.2.0 5f5512b827
Enter ".help" for usage hints.
D LOAD '~/dev/misc/duckdb-extension-c-minimal/src/capi_quack';
D SELECT multiply_numbers_together(1,2);
┌─────────────────────────────────┐
│ multiply_numbers_together(1, 2) │
│              int64              │
├─────────────────────────────────┤
│                2                │
└─────────────────────────────────┘
```
