### Challenge
My local pizzeria is trying out a new logo that is bringing in a lot of new customers. I think something fishy is going on. What are they doing?

### Løsning
Extracted strings from the jpg, flag revealed.
```
$ strings hiddenmsg.jpg | grep UMDCTF                                     1 ⨯
\f0\fs24 \cf0 \'93UMDCTF-{W3_ar3_th3_b3st_P1ZZ3r1a}\'94}
```

Flag:
> UMDCTF-{W3_ar3_th3_b3st_P1ZZ3r1a}
