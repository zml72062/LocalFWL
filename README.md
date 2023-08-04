# LocalFWL
Implementations for local versions of FWL(2).

## Aggregation types & implementations
| Aggregation |  Matrix Formula |
| :---:     |:---:|
| $h(u,v)$ | $X$|
| $h(v,u)$ | $X^T$|
| $h(u,u)$ | $\mathrm{diag}(X)11^T$ |
| $h(v,v)$ | $11^T\mathrm{diag}(X)$ |
| $\sum_{w\in V_G} h(u,w)$ | $X11^T$ |
| $\sum_{w\in V_G} h(w,v)$ | $11^TX$ |
| $\sum_{w\in \mathcal{N}(v)} h(u,w)$ | $XA^T$ |
| $\sum_{w\in \mathcal{N}(u)} h(w,v)$ | $AX$ |
| $\sum_{w\in V_G} h(u,w)h(w,v)$ | $XX$ |
| $\sum_{w\in \mathcal{N}(v)} h(u,w)h(w,v)$ | $X(A^T\odot X)$ |
| $\sum_{w\in \mathcal{N}(u)} h(u,w)h(w,v)$ | $(A\odot X)X$ |

## FWL(2) variants
| FWL(2) Variant | Operations |
| :---: |:---:|
| SWL  |  $X, XA^T, \mathrm{diag}(X) 11^T, X11^T$ |
| PSWL |  $X, XA^T, \mathrm{diag}(X) 11^T, 11^T\mathrm{diag}(X), X11^T$ |
| GSWL |  $X, XA^T, \mathrm{diag}(X) 11^T, 11^T\mathrm{diag}(X), X11^T, 11^TX$ |
| SSWL |  $X, X^T, XA^T, AX, \mathrm{diag}(X) 11^T, 11^T\mathrm{diag}(X), X11^T, 11^TX$ |
| LFWL(2) |  $X, X(A^T\odot X)$ |
| SLFWL(2) | $X, X(A^T\odot X), (A\odot X)X$ |
| FWL(2) | $X, XX$  |
| $\delta$-LWL(2) | $X, XA^T, AX$ |
| $\delta$-WL(2) | $X, XA^T, AX, X11^T, 11^TX$ |