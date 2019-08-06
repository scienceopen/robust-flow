[![image](https://travis-ci.org/scivision/robust-optical-flow.svg?branch=master)](https://travis-ci.org/scivision/robust-optical-flow)

# Black Robust Optical Flow
===========

Helper code used with [Michael Black\'s Robust optical flow
code](http://cs.brown.edu/people/black/code.html)

## Build

You will need:

-   C compiler (e.g. `gcc` or `clang`)
-   Meson [python3 -m pip install meson]{.title-ref}

```
meson build

meson test -C build
```

## Examples

You will see this plot:

![image](results/quiver_pepsi.jpg)

### Python

    python BlackRobustFlow.py data/pepsi

### Matlab/Octave

```matlab
[u,v] = BlackRobustFlow('data/pepsi');
```

Note, Octave 4.2.2 has a `quiver()` plotting bug (in general). Matlab
R2018a worked fine.

## Functions

GNC is the C program used for [Robust Estimation of Dense Optical Flow
by Michael
Black](http://cs.brown.edu/people/black/Papers/cviu.63.1.1996.html).

* `DemoGNC.sh`: terminal script running the dense robust optical flow code
* `BlackRobustFlow.{m,py}`: Nicer way to call GNC from Matlab with a variety of user-adjustable parameters