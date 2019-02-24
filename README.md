# Capitalize.Lisp
## An interesting and somewhat unorthodox way to capitalize things in Common Lisp

Lisp has been called "the most intelligent way to misuse a computer". Check out this elegant solution to a Common Lisp programming issue:

```lisp
[25]> (SETQ *PRINT-CASE* :CAPITALIZE)         ; Weird ugly Lisp :Output
:Capitalize
[26]> (DEFPARAMETER CAPITALIZE 'CAPITALIZE)   ; Remove the annoying colon
Capitalize
[27]> (DEFMACRO CAPITALIZE(&COLON COLON)      ; Apply it to everything
"CAPITALIZE 
(DECLARE(IGNORE COLON)))
(CAPITALIZE NIL) 
Nil"       
(DECLARE(IGNORE COLON)))
Capitalize
[28]> (capitalize nil)            ; Test 1
Nil
[29]> (EVAL CAPITALIZE)           ; Test 2
Capitalize
[30]> (FORMAT T "~S" capitalize)  ; Test 3   It works!
Capitalize
Nil
[31]> 
````

I admit it's hard to imagine a more expressive way to do it. Next weekend I'll find a solution for those pesky brackets. Or Parens. Whatever you young whippersnappers call them nowadays.
