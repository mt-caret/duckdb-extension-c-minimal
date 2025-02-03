.PHONY: clean

capi_quack: capi_quack.so
	python3 ../../extension-template-c/extension-ci-tools/scripts/append_extension_metadata.py --library-file ./capi_quack.so --extension-name capi_quack --out-file capi_quack --duckdb-platform linux_amd64_gcc4 --duckdb-version v1.2.0 --extension-version f616006

capi_quack.so: add_numbers.c capi_quack.c
	gcc -I../duckdb_capi/ -I./include capi_quack.c add_numbers.c -D DUCKDB_EXTENSION_NAME=capi_quack -fPIC -rdynamic -shared -Lstatic -o capi_quack.so

clean:
	rm -f capi_quack capi_quack.so
