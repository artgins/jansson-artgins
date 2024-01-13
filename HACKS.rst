Hacks of External libraries
===========================


Hack of jansson
===============

Function that return the pointer of a json integer
--------------------------------------------------

Let quick access to write and read integer values

diff -r jansson-2.14/src/jansson.h jansson-2.14-gines/src/jansson.h
316a317,318
> json_int_t *json_integer_value_pointer(const json_t *integer);
>

diff -r jansson-2.14/src/value.c jansson-2.14-gines/src/value.c
901a902,908
> json_int_t *json_integer_value_pointer(const json_t *json) {
>     if (!json_is_integer(json))
>         return 0;
>
>     return &(json_to_integer(json)->value);
> }
>


