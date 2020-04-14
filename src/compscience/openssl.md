OpenSSL
=======

Generating RSA keypair
----------------------

* RSA keypairs can be used to create a public/private keypair to facilitate secure communication of short messages and in encrypted manner. Refer [RSA keypair encryption demo].
* Keypair generation
    * Private Key: `openssl genrsa -out key-private.pem 2048` where 2048 is key length
    * Public Key: `openssl rsa -pubout -in key-private.pem -out key-public.pem`
* Keypair validation depends on regenerating the public key again and checking with the stored public key
    * `diff -qsy <(openssl rsa -pubout -in key-private.pem) key-public.pem`











References
----------

* [RSA keypair encryption demo]
* [OpenSSL Commands 1]
* [OpenSSL Cheatsheet]








[RSA keypair encryption demo]:  https://travistidwell.com/jsencrypt/demo/index.html
[OpenSSL Commands 1]: https://www.sslshopper.com/article-most-common-openssl-commands.html
[OpenSSL Cheatsheet]: https://www.freecodecamp.org/news/openssl-command-cheatsheet-b441be1e8c4a/