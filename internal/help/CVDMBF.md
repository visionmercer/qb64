The [CVDMBF](CVDMBF) function decodes an 8-byte [STRING](STRING) generated by [MKDMBF$](MKDMBF$) (or read from a file) to [DOUBLE](DOUBLE) numeric values.

## Syntax

> result# = [CVDMBF](CVDMBF)(stringData$)

## Description

* *CV* functions ([CVD](CVD), [CVS](CVS), [CVI](CVI), [CVL](CVL), [CVDMBF](CVDMBF), [CVSMBF](CVSMBF)) are used to convert values encoded by *MK$* functions ([MKD$](MKD$), [MKS$](MKS$), [MKI$](MKI$), [MKL$](MKL$), [MKDMBF$](MKDMBF$), [MKSMBF$](MKSMBF$)).
* **QB64** has [_CV](_CV) and [_MK$](_MK$) functions which can also deal with extended [Data types](Data-types).
* [DOUBLE](DOUBLE) values can range up to 15 decimal point digits. Decimal point accuracy depends on whole value places taken.

## Example(s)

Showcases the reduced space to store an encoded number.

```vb

a# = 77000.24523213
PRINT "Value of a#:"; a#
b$ = MKDMBF$(a#)
PRINT "Value of a# encoded using MKDMBF$: "; b$
PRINT "The string above, decoded using CVDMBF:"; CVDMBF(b$)

```

```text

Value of a#: 77000.24523213

Value of a# encoded using MKDmbf$:  5─c▼d▬æ

The string above, decoded using CVDMBF: 77000.24523213

```

> Since the representation of a double-precision number can use up to 15 ASCII characters (fifteen bytes), writing to a file using [MKDMBF$](MKDMBF$) conversion, and then reading back with the [CVDMBF](CVDMBF) conversion can save up to 7 bytes of storage space.

## See Also

* [MKD$](MKD$), [MKI$](MKI$), [MKS$](MKS$), [MKL$](MKL$), [MKDMBF$](MKDMBF$), [MKSMBF$](MKSMBF$)
* [CVI](CVI), [CVS](CVS), [CVD](CVD), [CVL](CVL), [CVSMBF](CVSMBF)
* [_CV](_CV), [_MK$](_MK$)