1. main module (the collection of variables that you have access to in a script executed at the top level and in calculator mode).
2. Within a module, the module’s name (as a string) is available as the value of the global variable `__name__`
	1. the code in the module will be executed, just as if you imported it, with the `__name__` set to `"__main__"`
3. Packages: collection of modules. 
	1. the module name A.B designates a submodule named B in a package named A. 
4. ***Namespace***: a *namespace* is a mapping from names to objects
	1. The namespace containing the built-in names is created when the Python interpreter starts up, and is never deleted. 
	2. The global namespace for a module is created when the module definition is read in; normally, module namespaces also last until the interpreter quits. 