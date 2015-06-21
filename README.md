# SQLiteGlue-core for sqlcipher

Low-level Android &amp; other Java native glue interface to sqlcipher using Gluegen.

Unlicense (public domain).

Inculudes sqlcipher (BSD-style license) and part of TomCrypt (public domain)

## About

SQLiteGlue provides the basic low-level functions necessary to use sqlite from an Android or other
Java application over JNI (Java native interface). This is accomplished by using
[GlueGen](http://jogamp.org/gluegen/www/) around a simple wrapper C module.

This project is meant to help build a higher-level sqlite interface library, with the JNI layer completely isolated and may be embedded with the package name changed.

**NOTE:** This project references the `gluegentools` & `sqlite-amalgamation` subproject, which are resolved by: $ `make init` (see [REF-BUILDING.md](REF-BUILDING.md)).

**WARNING:** The sqlite database and statement handles that are returned by the `SQLiteGlue` library functions are raw C pointer values (with `0x100000000` added). If someone uses a sqlite database or statement handle that is not valid, or no longer valid with the `SQLiteGlue` library the behavior is undefined (typically a crash that cannot be recovered). It is *NOT* recommended to use this API directly unless you really understand how this library works internally.

## Usage

See [REF-API-USAGE.md](REF-API-USAGE.md).

## Building

See [REF-BUILDING.md](REF-BUILDING.md).

# Automatic testing

Tested on Android in [sqlg / SQLiteGlue-test-Android](https://github.com/sqlg/SQLiteGlue-test-Android).

