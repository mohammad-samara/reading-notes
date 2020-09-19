# Authentication

----------------------------------

## Authentication

* **Authentication** is an identifier that is used to verify identity or validate the authenticity of data such as messages. They are often hashcodes that are designed to be infeasible to guess

## User Modiling

* Allocate user data with the same user, used to generate or adapt user interfaces at runtime, to address particular user needs and preferences.

## Cryptography

* **Cryptology**, is the practice and study of techniques for secure communication in the presence of third parties called adversaries.
* **Cryptography** The science which studies methods for encoding messages so that they can be read only by a person who knows the secret information required for decoding,it could be(Cryptographic Hash Algorithm/Cryptographic Cypher Algorithm).

## Hash Algorithms

* A **hashing algorithm** is a cryptographic hash function. It is a mathematical algorithm that maps data of arbitrary size to a hash of a fixed size.
* A**cryptographic hash function** is an algorithm that can be run on data such as an individual file or a password to produce a value called a checksum. The main use of a cryptographic hash function is to verify the authenticity of a piece of data.
* It takes a piece of data and produces a hash that is deliberately difficult to reverse.

## Cypher Algorithms

* A **cipher** (or cypher) is a pair of algorithms that create the **encryption** and the reversing **decryption**.
* **Cryptographic Cypher Algorithm** takes a piece of data and a key and produces encrypted data. Later the encrypted data can be reversed into the original data by decrypting it using the same key.

## Basic Authorization

* **Basic authentication** is a simple authentication scheme built into the HTTP protocol. The client sends HTTP requests with the Authorization header that contains the word Basic word followed by a space and a base64-encoded string `username:password`. For example, to authorize as demo / p@55w0rd the client would send: `Authorization: Basic ZGVtbzpwQDU1dzByZA==`
* We get `atob` and `btoa` to convert to/from “Base64 Encoding”.

## JSON Web Token (JWT)

* **JWT** is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object.
* **JWT** is an internet standard for creating data with optional signature and/or optional encryption.
* JSON Web Tokens consist of three parts separated by dots`xxxxx.yyyyy.zzzzz`:
   1. Header
   2. Payload
   3. Signature

## Authentication Cheat Sheet

 `https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html`
