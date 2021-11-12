Tested or identified homomorhic encryption libraries

Section describes/investigates tools and use cases that could be merged to semaciti demo flow.

We use many methods to meet the requirements of zero-trust architecture aproach like trusted execution environments but also we made an effort to onborad homomorhic encryption techniques.
To facilitate the use of cloud computing by data owners (federated organizations) to get the desired computations
and analysis done on their sensitive data, while preserving the benefit of cloud computing, we identify tools supporting homomorhic encryption for confidential computing.



## fully-homomorphic-encryption by Google
\url{https://www.nucypher.com/fully-homomorphic-encryption}
Apache-2.0 License
FHE C++ Transpiler
The FHE C++ Transpiler is a general purpose library that converts C++ into FHE-C++ that works on encrypted input.

The transpiler has a modular architecture that allows varying the underlying FHE library, the high-level program description and the output language as well. We hope that this flexibility will allow researchers from different fields to work together on this exciting goal of making FHE more efficient and broadly applicable.

The code, examples, and more information is in the transpiler subdirectory.

Fully Homomorphic Encryption (FHE)
This repository contains open-source libraries and tools to perform fully homomorphic encryption (FHE) operations on an encrypted data set.

About Fully Homomorphic Encryption

Fully Homomorphic Encryption (FHE) is an emerging cryptographic technique that allows developers to perform computations on encrypted data. This represents a paradigm shift in how data processing and data privacy relate to each other.

Previously, if an application had to perform some computation on data that was encrypted, this application would necessarily need to decrypt the data first, perform the desired computations on the clear data, and then re-encrypt the data. FHE, on the other hand, simply removes the need for this decryption-encryption steps by the application, all at once.

In practice, for an application that needs to perform some computation F on data that is encrypted, the FHE scheme would provide some alternative computation F' which when applied directly over the encrypted data will result in the encryption of the application of F over the data in the clear. More formally: F(unencrypted_data) = Decrypt(F'(encrypted_data)).

As a result, FHE can have an enormous impact to our society. It can change the way computations are performed by preserving end-to-end privacy. For example, users would be able to offload expensive computations to cloud providers in a way that cloud providers will not have access to the users' data at all.

The main hindrance for the adoption of FHE has been its very poor performance. Despite significant scientific improvements, performing computations on encrypted data using FHE is still orders of magnitude slower than performing the computation on the plaintext. On top of that, converting a program that operates on unencrypted data to one that FHE-operates on encrypted data is far from being a trivial translation. If not properly done, this translation can significantly increase the performance gap between computing on unencrypted data and the FHE-computation on encrypted data, thus precluding wide FHE adoption.


## nuFHE
\url{https://github.com/nucypher/nuFHE}


--------------------bib

@misc{tseng2021encrypted,
      title={Encrypted Data Processing}, 
      author={Jessica Tseng and Gianfranco Bilardi and Kattamuri Ekanadham and Manoj Kumar and Jose Moreira and P. C. Pattnaik},
      year={2021},
      eprint={2109.09821},
      archivePrefix={arXiv},
      primaryClass={cs.CR}
}

----------------------------------------todo
https://arxiv.org/abs/2109.09821




https://nufhe.readthedocs.io/en/latest/
https://nufhe.readthedocs.io/en/latest/api.html
https://github.com/IBM/fhe-toolkit-linux
https://github.com/IntelAI/he-transformer
https://github.com/intel/he-toolkit
https://github.com/homenc/HElib
https://github.com/ldsec/lattigo
https://github.com/microsoft/SEAL
seal w node: https://github.com/morfix-io/node-seal
https://palisade-crypto.org/software-library/
https://github.com/MarbleHE/Marble
https://github.com/gdanezis/petlib
https://github.com/Georeactor/encrypted-geofence


homomorficzny kalendarz: https://github.com/ldsec/lattigo-polls-demo
własne doodle? ja lubię. plugin do chrome

https://morfix.io/sandbox
postaw bazę:
https://github.com/CryptDB/cryptdb
https://github.com/pdroalves/encrypted-mongodb
https://github.com/aprismatic/prismadb
https://github.com/nucypher/zerodb
baza w sgx?

https://github.com/TimeCrypt/timecrypt
https://www.usenix.org/system/files/nsdi20-paper-burkhalter.pdf


wrapper na seal i palisade: https://github.com/ibarrond/Pyfhel
seal binding do python: https://github.com/Huelse/SEAL-Python/

https://docs.zama.ai/concrete/lib/demos.html#example-1-homomorphic-arithmetic-over-3-bit-integers
concrete allows:
addition between a ciphertext and a constant
subtraction between a ciphertext and a constant
multiplication between a ciphertext and a constant
addition between two ciphertexts
subtraction between two ciphertexts
multiplication between two ciphertexts
max between two ciphertexts

wystaw lambdy wrnaglerem?

The key-switching allows to convert a ciphertext encrypted with a secret key, to a ciphertext encrypted with another secret key. This requires a special Key-switching key ().
Key-switching is used primarily to change the dimension security parameter of a ciphertext, and as part of the bootstrapping procedure.
https://docs.zama.ai/concrete/lib/simple-operations/key-switching.html


https://github.com/data61/python-paillier
The homomorphic properties of the paillier crypto system are:
Encrypted numbers can be multiplied by a non encrypted scalar.
Encrypted numbers can be added together.
Encrypted numbers can be added to non encrypted scalars.

szyfrowanie symetryczne prince?
https://github.com/vernamlab/cuHE/blob/master/examples/Prince/Prince.cu
e basic polynomial arithmetic operations, such as multiplication,
addition and polynomial modular reduction are implemented efficiently on CUDA GPUs

Interfacing with NTL. We build our library to interface with the NTL library by Shoup [30].
Most implementations of polynomial based HE schemes are built on NTL. We provide an interface
to NTL data types, in particular to the polynomial class ZZX so that GPU acceleration can be
achieved with very little modification to a program. Another reason is that we only support very
limited types of polynomial operations. Therefore, until non performance critical operations, e.g. a
polynomial inversion in a polynomial ring, are implemented we may still utilize the NTL library.

https://eprint.iacr.org/2015/818.pdf

To demonstrate the performance gain achieved with cuHE, by employing the DHS scheme [11], along with
many optimizations, to implement the Prince block cipher and a homomorphic sorting algorithm
on integers.

https://github.com/snucrypto/HEAAN
HEAAN is software library that implements homomorphic encryption (HE) that supports fixed point arithmetics. This library supports approximate operations between rational numbers. The approximate error depends on some parameters and almost same with floating point operation errors. The scheme in this library is on the paper "Homomorphic Encryption for Arithmetic of Approximate Numbers" (https://eprint.iacr.org/2016/421.pdf).
HEAAN is a software library that implements homomorphic encryption (HE) that supports fixed point arithmetics. This library supports approximate operations between rational numbers. The approximate error depends on some parameters and almost same with floating point operation errors. The scheme in this library is on the paper.
https://github.com/Huelse/HEAAN-Python


https://github.com/K-miran/HEMat
HEMat is a software package for performing a secure outsourced matrix computation using homomorphic encryption (https://dl.acm.org/citation.cfm?id=3243837).

https://github.com/kryptnostic/krypto
C++ Implementation of Multivariate Quadratic FHE
https://github.com/kryptnostic/krypto/blob/develop/krypto-lib/src/main/V2/V2Specification.pdf
https://www.npmjs.com/package/krypto-js

https://arxiv.org/pdf/2109.09821.pdf

https://fhe.org/talks/introduction-to-fhe-by-pascal-paillier

https://fhe.org/talks/introduction-to-mpc-by-yehuda-lindell
https://fhe.org/talks/tfhe-deep-dive-by-ilaria-chillotti
https://fhe.org/talks/fhe-development-tools-by-alexander-viand
https://fhe.org/talks/googles-c-to-fhe-transpiler-by-shruthi-gorantala-and-rob-springer

tota We present fully homomorphic encryption schemes for fixed-point arithmetic with fixe
