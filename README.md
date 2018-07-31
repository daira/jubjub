baby\_Jubjub supporting evidence
--------------------------

This repository contains supporting evidence that the twisted Edwards curve
168700.x^2 + y^2 = 1 + 168696.x^2.y^2 of rational points over
GF(21888242871839275222246405745257275088548364400416034343698204186575808495617),
also called babyJubJub based upone ["Jubjub"](https://z.cash/technology/jubjub.html),
satisfies the [SafeCurves criteria](https://safecurves.cr.yp.to/index.html).

The script ``verify.sage`` is based on
[this script from the SafeCurves site](https://safecurves.cr.yp.to/verify.html),
modified

* to support twisted Edwards curves;
* to generate a file 'primes' containing the primes needed for primality proofs,
  if it is not already present;
* to change the directory in which Pocklington proof files are generated
  (``proof/`` rather than ``../../../proof``), and to create that directory
  if it does not exist.

Prerequisites:

* apt-get install sagemath
* pip install sortedcontainers

Run ``sage verify.sage .``, or ``./run.sh`` to also print out the results.

You can generate the curve by running `sage findCurve.sage 168698`
This is the lowest A=168698 of a montgomary curve that statifies the 
critieria defined in [ref7748](https://tools.ietf.org/html/rfc7748)

Note that the "rigidity" criterion cannot be checked automatically.
