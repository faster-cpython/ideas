# StackRef Semantics
Author: Ken Jin

This is the formal definition for live and dead references
(expressed in operational semantics).

We define two initial sets:
$$
\color{blue} live_{PyStackRef} \color{black}
= \{l \; \lvert \; type(l) = PyStackRef \}
\\
\color{red} dead_{PyObject} \color{black}
= \{l \; \lvert \; type(l) = PyObject * \}
$$

The program state is defined as the two-tuple:
$$
(\color{blue} live_{PyStackRef} \color{black},
\; \color{red} dead_{PyObject} \color{black} )
$$

All operations are defined as operations on this two-tuple.

$$
borrow(A):
(\color{blue} live_{PyStackRef} \color{black},
\; \color{red} dead_{PyObject} \color{black} )
\rightarrow
    (\color{blue} live_{PyStackRef} \color{black},
    \; \color{red} dead_{PyObject} \color{black} )
\\
steal(A)\{PyObject\;to\;StackRef\}:
(\color{blue} live_{PyStackRef} \color{black},
\; \color{red} dead_{PyObject} \color{black} )
\rightarrow
    (\color{blue} live_{PyStackRef} - \{A\} \color{black},
    \; \color{red} dead_{PyObject} - \{A\} \color{black} )
\\
steal(A)\{StackRef\;to\;PyObject\}:
(\color{blue} live_{PyStackRef} \color{black},
\; \color{red} dead_{PyObject} \color{black} )
\rightarrow
    (\color{blue} live_{PyStackRef} + \{A\} \color{black},
    \; \color{red} dead_{PyObject} + \{A\} \color{black} )
\\
new(A)\{PyObject\;to\;StackRef\}:
(\color{blue} live_{PyStackRef} \color{black},
\; \color{red} dead_{PyObject} \color{black} )
\rightarrow
    (\color{blue} live_{PyStackRef} + \{A\} \color{black},
    \; \color{red} dead_{PyObject} \color{black} )
\\
new(A)\{StackRef\;to\;PyObject\}:
(\color{blue} live_{PyStackRef} \color{black},
\; \color{red} dead_{PyObject} \color{black} )
\rightarrow
    (\color{blue} live_{PyStackRef} \color{black},
    \; \color{red} dead_{PyObject} - \{A\} \color{black} )       
$$