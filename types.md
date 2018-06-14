Atomic types:
- `char`:
  Standard 8-bit signed char type.

- `uchar`:
  Unsigned version of `char`.

- `short`:
  16 bit signed integer.

- `ushort`:
  Unsigned version of `short`.

- `int`:
  32 bit signed integer.

- `uint`:
  Unsigned version of `int`.

- `int{num}`:
  {num} bit signed integer. Num can be 8, 16, 32, or 64. For example, `int8`. `int16`, etc.

- `uint{num}`:
  {num} bit unsigned integer.

Composite types:
- `type*`:
  A pointer to a `type`.

- `type[{num}]`:
  An array of `num` `type`s. Unlike C, this doesn't get turned into a pointer when passed.

- `struct<<name1 type1> <name2 type2> ...>`:
  A struct with member types `type1`, `type2`, ... . Members can be accessed with `var.name`.

- `func<ret_type><arg1_type, arg2_type, ...>`:
  A function taking arguments of types specified by the `argn_type`s and returning type `ret_type`.
