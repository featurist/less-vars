## less-vars

Show how variables are defined in your less files, including how their values are changed during the compilation process.

in `my.less`:

```less
@variable: blue;
@variable: red;

@other: lighten(@variable, 10%);

.test {
  color: @variable;
  background-color: @variable;
}
```

```sh
> less-vars my.less
/path/blah.less(1): @variable blue
/path/blah.less(2): @variable red
/path/blah.less(4): @other #ff3333
```
