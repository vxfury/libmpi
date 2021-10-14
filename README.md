# libmpi

[![license](https://img.shields.io/badge/license-Apache-brightgreen.svg?style=flat)](https://github.com/vxfury/libmpi/blob/master/LICENSE)
[![CI Status](https://github.com/vxfury/libmpi/workflows/ci/badge.svg)](https://github.com/vxfury/libmpi/actions)
[![codecov](https://codecov.io/gh/vxfury/libmpi/branch/main/graph/badge.svg?token=5IfLTTEcnF)](https://codecov.io/gh/vxfury/libmpi)
![GitHub release (latest by date)](https://img.shields.io/github/v/release/vxfury/libmpi?color=red&label=release)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/vxfury/libmpi/pulls)

Multiple Precision Integer and Relevant Algorithms, such as Bignum, RSA, DH, ECDH, ECDSA

```
+--------------------------------+---------------------------+--------------------------+--------------------------+
|     operation with options     | average time(nanoseconds) | coefficient of variation | perfermance ratio to ref |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| from-string(ossl)              |        24172.241800       |         0.006750         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| to-string(ossl)                |        2197.089200        |         0.021739         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| from-string(mpi)               |        2137.128600        |         0.021768         |         11.310616        |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| to-string(mpi)                 |         574.987800        |         0.041993         |         3.821106         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| from-octets(ossl)              |         549.247400        |         0.043430         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| to-octets(ossl)                |        1310.657400        |         0.027754         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| from-octets(mpi)               |         238.723200        |         0.064967         |         2.300771         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| to-octets(mpi)                 |         117.621600        |         0.092208         |         11.142999        |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| add(ossl)                      |         220.362800        |         0.067373         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| add(mpi)                       |         67.241000         |         0.121952         |         3.277209         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| add-assign(ossl)               |         224.263000        |         0.067757         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| add-assign(mpi)                |         67.300800         |         0.121900         |         3.332249         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| sub(ossl)                      |         143.562000        |         0.083477         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| sub(mpi)                       |         52.940600         |         0.137461         |         2.711756         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| sub-assign(ossl)               |         224.023000        |         0.066864         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| sub-assign(mpi)                |         62.980800         |         0.126739         |         3.557005         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| mul(ossl)                      |        9963.472800        |         0.010066         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| mul(mpi)                       |        1595.341200        |         0.025176         |         6.245355         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| sqr(ossl)                      |        6915.892200        |         0.012063         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| sqr(mpi)                       |        1014.313600        |         0.031924         |         6.818298         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| div(ossl)                      |        31212.095800       |         0.005788         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| div(mpi)                       |        3056.300800        |         0.018687         |         10.212377        |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| gcd_consttime(ossl)            |      11963826.925000      |         0.008282         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| gcd_consttime(mpi)             |       3872197.192000      |         0.004772         |         3.089674         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| montgomery-exp(ossl)           |      107685134.800000     |         0.000375         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| montgomery-exp-consttime(ossl) |      114502505.800000     |         0.000469         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| montgomery-exp(mpi)            |       8480278.454545      |         0.000869         |         12.698302        |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| montgomery-exp-consttime(mpi)  |      11783257.000000      |         0.000614         |         9.717390         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| generate_prime(ossl)           |     2260127581.000000     |         0.760948         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| is_prime(ossl)                 |      438702222.000000     |         0.002411         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| MUL2(a * 2 = a + a)            |         56.581800         |         0.132972         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| MUL2(a * 2 = a << 1)           |         73.442200         |         0.124943         |         0.770426         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
```

