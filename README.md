# libmpi

[![license](https://img.shields.io/badge/license-Apache-brightgreen.svg?style=flat)](https://github.com/vxfury/libmpi/blob/master/LICENSE)
[![CI Status](https://github.com/vxfury/libmpi/workflows/ci/badge.svg)](https://github.com/vxfury/libmpi/actions)
[![codecov](https://codecov.io/gh/vxfury/libmpi/branch/main/graph/badge.svg?token=5IfLTTEcnF)](https://codecov.io/gh/vxfury/libmpi)
![GitHub release (latest by date)](https://img.shields.io/github/v/release/vxfury/libmpi?color=red&label=release)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/vxfury/libmpi/pulls)

Multiple Precision Integer and Relevant Algorithms, such as Bignum, RSA, DH, ECDH, ECDSA
## Benchmark(libmpi VS openssl)

| brief | average time<br>(nanoseconds) | instability<br>(coefficient of variation) | rating | 
| :-- | :-: | :-: | :-: |
| from-string(mpi vs openssl) | 2124.69<br>29033.7* | 0.0277376 | <span style="color:#008000;font-weight:bold;text-decoration:blink;">13.6649<br>(Tu es mon meilleur frère...)</span> | 
| to-string(mpi vs openssl) | 948.755<br>2905.94* | 0.0534082 | <span style="color:#008000;font-weight:bold;">3.0629<br>(Tu peux faire mieux, continue)</span> | 
| from-octets(mpi vs openssl) | 223.779<br>772.516* | 0.0669006 | <span style="color:#008000;font-weight:bold;">3.45214<br>(Tu peux faire mieux, continue)</span> | 
| to-octets(mpi vs openssl) | 102.259<br>1538.83* | 0.0988902 | <span style="color:#008000;font-weight:bold;text-decoration:blink;">15.0483<br>(Tu es mon meilleur frère...)</span> | 
| add(mpi vs openssl) | 42.3998<br>291.898* | 0.153625 | <span style="color:#008000;font-weight:bold;text-decoration:blink;">6.88443<br>(C'est super, dessine-toi une tarte)</span> | 
| add-assign(mpi vs openssl) | 40.8398<br>344.758* | 0.1565 | <span style="color:#008000;font-weight:bold;text-decoration:blink;">8.44172<br>(C'est super, dessine-toi une tarte)</span> | 
| sub(mpi vs openssl) | 40.9398<br>169.699* | 0.156331 | <span style="color:#008000;font-weight:bold;">4.14509<br>(Tu peux faire mieux, continue)</span> | 
| sub-assign(mpi vs openssl) | 44.5798<br>299.138* | 0.149996 | <span style="color:#008000;font-weight:bold;text-decoration:blink;">6.71018<br>(C'est super, dessine-toi une tarte)</span> | 
| mul(mpi vs openssl) | 1892.97<br>12086.4* | 0.0301221 | <span style="color:#008000;font-weight:bold;text-decoration:blink;">6.38489<br>(C'est super, dessine-toi une tarte)</span> | 
| sqr(mpi vs openssl) | 1155.01<br>8348.86* | 0.138431 | <span style="color:#008000;font-weight:bold;text-decoration:blink;">7.22836<br>(C'est super, dessine-toi une tarte)</span> | 
| MUL2(a * 2 = a + a) | 32.9798 | 0.174251 | <span style="font-style:italic;">N/A</span> | 
| MUL2(a * 2 = a << 1) | 64.8396 | 0.124198 | <span style="font-style:italic;">N/A</span> | 
