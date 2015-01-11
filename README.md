Provides glsl completion by using glslangValidator.
glslangValidator can be found from:
  https://www.khronos.org/opengles/sdk/tools/Reference-Compiler/

To use this package with company-mode run;
  (add-to-list 'company-backends 'company-glsl)

To use this package, you must be in glsl major mode. But it doesn't
require any functionality from there yet.

This package is still quite incomplete, but it does basic symbol
completion. It finds all the symbols that are referenced in the
code or references by the linker. It can also reference function
names, but at the moment no other information is retained.

There is also no scoping, so completion candidates includes all
symbols, even if they are not available in the current scope. Even
any function parameters are seen as candidates in all other
functions.
