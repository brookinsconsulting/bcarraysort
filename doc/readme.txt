
ArraySortOperator
=================

Wrapper for PHP array sort functions:

sort([$flags])
rsort([$flags])
asort([$flags])
arsort([$flags])
ksort([$flags])
krsort([$flags])

natsort()
natcasesort()

Except for the last two operators, there is an optional argument of type string, which can be either 'regular', 'numeric', 'string', or 'locale_string'.
See also: http://www.php.net/manual/en/ref.array.php

Example:
{def $array = array('zero', 'one', 'two')}
{*
$array = Array(
	0 => 'zero',
	1 => 'one',
	2 => 'two',
)
*}

{def $sorted = $array|sort('string')}
{*
sort reorders keys:
$sorted = Array(
	0 => 'one',
	1 => 'two',
	2 => 'zero',
)
*}

{def $asorted = $array|asort('string')}
{*
asort preserves keys:
$asorted = Array(
	1 => 'one',
	2 => 'two',
	0 => 'zero',
)
*}


----------------------
Marc Boon - March 2006
marcboon[AT]dds[DOT]nl
