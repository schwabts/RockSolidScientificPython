# Rock-Solid Scientific Python

This repo does not contain my own code!

It is just a fork of David Ketcheson's useful tutorial
[12 steps toward rock-solid scientific Python code](https://www.davidketcheson.info/2015/05/10/rock_solid_code.html).
David provides a demo of best practices for reliable scientific code as described in 
[a series of blog posts](http://davidketcheson.info/2015/05/12/rock_solid_code.html).

All rights related to this contents are his!

The code in this repo implements Gaussian elimination without pivoting.  Given a square matrix,
it constructs factors L and U that are lower-triangular and strictly-upper-triangular (respectively)
such that LU = A.  The algorithm is not numerically stable and should not be used for large matrices due
to the tendency for roundoff errors to be amplified.  The implementation is also very slow, since it uses
Python loops.

## Dependencies

This code requires Python and numpy.  If you have Python and pip, you can get numpy via

    pip install numpy

## Installation
To use this code, you should first copy it to your computer via

    git clone https://github.com/schwabts/rock-solid-code-demo.git

or - even better - get the original from 

    git clone https://github.com/ketch/rock-solid-code-demo.git
    
## Usage

Then you can invoke it from the IPython prompt via

```python
    cd rock-solid-code-demo
    import factor
    import numpy as np
    A = np.random.rand(3,3)
    L, U = factor.LU(A)
```