# ML-Assignment-3
Helping a Panda Bear to determine what his reflection will look like in a mirror that he has placed at an angle. Assignment submitted for online Machine learning Math course offered by Imperial College London .

import numpy as np
from numpy.linalg import norm, inv
from numpy import transpose
#bear datas are given in the form of bearNecessities
from readonly.bearNecessities import * 
def build_reflection_matrix(bearBasis):
    E=gsBasis(bearBasis)
    TE=np.array([[1,0],[0,-1]])
    T= E @ TE @ inv(E)
    return T
