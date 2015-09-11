## less-vars

Show how variables are defined in your less files, including how their values are changed during the compilation process.

```sh
npm install less-vars
```

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

Then `less-vars my.less`:

```sh
.../my.less(1): @variable: blue; => blue
.../my.less(2): @variable: red; => red
.../my.less(4): @other: lighten(@variable, 10%); => #ff3333
```
