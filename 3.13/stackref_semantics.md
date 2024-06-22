# StackRef Semantics

This is the formal definition for live and dead references
(expressed in operational semantics).

We define two initial sets:

$$
\begin{align}
    & \color{blue} live_{\text{PyStackRef}} \color{black}
    & = \\{l  \mid  type(l) = \text{PyStackRef} \\}
    \\
    & \color{red} dead_{\text{PyObject}} \color{black}
    & = \\{l  \mid  type(l) = \text{PyObject *} \\}
\end{align}
$$

The program state is defined as the two-tuple:

$$
(\color{blue} live_{\text{PyStackRef}} \color{black},
 \color{red} dead_{\text{PyObject}} \color{black} )
$$

All operations are defined as operations on this two-tuple.

$$
\begin{align}
& borrow(A):
(\color{blue} live_{\text{PyStackRef}} \color{black},
\color{red} dead_{\text{PyObject}} \color{black} )
\rightarrow
    (\color{blue} live_{\text{PyStackRef}} \color{black},
    \color{red} dead_{\text{PyObject}} \color{black} )
\\
& steal(A)[\text{PyStackRef} \hookrightarrow \text{PyObject}]:
(\color{blue} live_{\text{PyStackRef}} \color{black},
\color{red} dead_{\text{PyObject}} \color{black} )
\rightarrow
    (\color{blue} live_{\text{PyStackRef}} \color{black} - A,
    \color{red} dead_{\text{PyObject}} \color{black} - A)
\\
& steal(A)[\text{PyObject} \hookrightarrow \text{PyStackRef}]:
(\color{blue} live_{\text{PyStackRef}} \color{black},
\color{red} dead_{\text{PyObject}} \color{black} )
\rightarrow
    (\color{blue} live_{\text{PyStackRef}} \color{black} + A,
    \color{red} dead_{\text{PyObject}} \color{black} + A)
\\
& new(A)[\text{PyStackRef} \hookrightarrow \text{PyObject}]:
(\color{blue} live_{\text{PyStackRef}} \color{black},
\color{red} dead_{\text{PyObject}} \color{black} )
\rightarrow
    (\color{blue} live_{\text{PyStackRef}} \color{black},
    \color{red} dead_{\text{PyObject}} \color{black} - A)
\\
& new(A)[\text{PyObject} \hookrightarrow \text{PyStackRef}]:
(\color{blue} live_{\text{PyStackRef}} \color{black},
\color{red} dead_{\text{PyObject}} \color{black} )
\rightarrow
    (\color{blue} live_{\text{PyStackRef}} \color{black} + A,
    \color{red} dead_{\text{PyObject}} \color{black})
\\
\end{align}
$$