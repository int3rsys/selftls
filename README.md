# selftls
Sample application to let OpenSSL talk to itself (for fuzzing)

compilation example:
```
intersys@intersys:~/corpus_dir$ cp ../openssl_dir/{libssl.a, libcrypto.a} .
intersys@intersys:~/openssl_dir$ AFL_USE_ASAN=1 ../afl-2.52b/afl-gcc selftls.c -I <open_ssl_include_dir> -L<openssl_ssl_dir> -o selftls libssl.a libcrypto.a -ldl
```
