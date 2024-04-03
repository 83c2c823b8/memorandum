In the vim
## excute bash command to the vim line
```sh
echo $((2**3))
```
and in normal mode,
```vim
:.!bash
```
the result is 8.

## handling buffer
```vim
:enew
```
make a new buffer.
```vim
:bd
```
close the current buffer.

## normal
```vim
:normal iHello
```
this is useful when you treat multiline. For example
```
hello
hello
hello
hello
hello
hello
hello
hello
hello
hello
hello
hello
hello
hello
```
If you want to append ! after "hello" to the all lines. Selecting all and 
```vim
:normal A!
```
then you obtain what you want.

## encription
```vim
:X
```
and enter key twice.
when you want to unlock the key, set key nothing.
