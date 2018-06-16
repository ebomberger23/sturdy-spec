Current EBNF grammar:
```
ident_first_char := "a" | "A" | "b" | "B" | ... | "z" | "Z" | "_"
ident_char := ident_first_char | "0" | "1" ... | "9"
ident := ident_first_char, {ident_char}

base_expr = literal | ident | "(", expr, ")"
dot_expr := base_expr, {".", ident}
call_arg_list := "(", ")" | "(", expr, {",", expr}, [","], ")"
call_expr := dot_expr | call_expr, call_arg_list
un_expr := "+" | "-" | "~", call_expr
shift_expr := un_expr, {"<<" | ">>", un_expr}
binary_expr := shift_expr, {"&" | "|" | "^", shift_expr}
pow_expr := binary_expr, {"**", binary_expr}
mul_expr := pow_expr, {"*" | "/" | "%", pow_expr}
add_expr := mul_expr, {"+" | "-", mul_expr}
cmp_expr := add_expr, {"==" | "!=" | "<" | ">" | "<=" | ">=", add_expr}
```
