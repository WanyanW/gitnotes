
1. main module (the collection of variables that you have access to in a script executed at the top level and in calculator mode).
	1. `python foo.py` means running the module foo (the source file) as the main program
		1. the interpreter will assign the hard-coded string `"__main__"` to the `__name__` variable
	2. `import foo` suppose some other module is the main program and it imports your module
		1. the interpreter will assign the name "foo" from the import statement to the __name__ variable, i.e.
2. Within a module, the module’s name (as a string) is available as the value of the global variable `__name__`
	1. the code in the module will be executed, just as if you imported it, with the `__name__` set to `"__main__"`
3. Packages: collection of modules. 
	1. the module name A.B designates a submodule named B in a package named A.
4. The `__init__.py` files are required to make Python treat directories containing the file as packages. In the simplest case, `__init__.py` can just be an empty file, but it can also execute initialization code for the package or set the `__all__` variable.
5. a package’s `__init__.py` code defines a list named `__all__`, it is taken to be the list of module names that should be imported when from package import * is encountered. 
6. ***Namespace***: a *namespace* is a mapping from names to objects
	1. The namespace containing the built-in names is created when the Python interpreter starts up, and is never deleted. 
	2. The global namespace for a module is created when the module definition is read in; normally, module namespaces also last until the interpreter quits. 
7. class (磨具) -- crea