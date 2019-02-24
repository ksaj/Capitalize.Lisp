# Capitalize.Lisp
## An interesting and somewhat unorthodox way to capitalize things in Common Lisp

Lisp has been called "the most intelligent way to misuse a computer". Check out this elegant solution to a Common Lisp programming issue:

```lisp
[25]> (SETQ *PRINT-CASE* :CAPITALIZE)
:Capitalize
[26]> (DEFPARAMETER CAPITALIZE 'CAPITALIZE)
Capitalize
[27]> (DEFMACRO CAPITALIZE(&BODY BODY)  
"CAPITALIZE 
(DECLARE(IGNORE BODY)))
(CAPITALIZE NIL) 
Nil"       
(DECLARE(IGNORE BODY)))
Capitalize
[28]> (capitalize nil)
Nil
[29]> (EVAL CAPITALIZE)
Capitalize
[30]> (FORMAT T "~S" capitalize)  ; It works! ;)
Capitalize
Nil
[31]> 
````

I admit it's hard to imagine a more expressive way to do it. Next weekend I'll find a solution for those pesky brackets. Or Parens. Whatever you young whippersnappers call them nowadays.
