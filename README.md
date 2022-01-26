# ipython-client
Notes about ipython backend and client

On a Mac, ipython uses the default backend `MacOS`

Spawning a server `ipython kernel` and connecting, the backend is still `MacOS`

Connecting via ipython client, code or Jupyter, this changes to
`module://matplotlib_inline.backend_inline`

The Jupyter commands:

* `%notebook inline`  -> `backend=module://matplotlib_inline.backend_inline`, low res embedded PNG image
* `%notebook notebook` -> `backend=nbAgg`, live figure widget with buttons, probably related to ipython.Displays

by default it is `%notebook inline`

```
% ipython kernel
NOTE: When using the `ipython kernel` entry point, Ctrl-C will not work.

To exit, you will have to explicitly quit this process, by either sending
"quit" from a client, or using Ctrl-\ in UNIX-like environments.

To read more about this, see https://github.com/ipython/ipython/issues/2049


To connect another client to this kernel, use:
    --existing kernel-71888.json
```
```
% ipython --existing kernel-71888.json
```

Other backends

https://medium.com/@Med1um1/using-matplotlib-in-jupyter-notebooks-comparing-methods-and-some-tips-python-c38e85b40ba1

%notebook widget

seems to be the same as %notebook ipympl

%matplotlib --list

On Colab is agg by default

Each cell ends with an implicit show. The current axes is cleared, plt.gca()
