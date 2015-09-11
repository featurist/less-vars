## less-vars

Debug your less: less-vars shows how variables are defined progressively in your less files, showing where they are defined and what values they evaluate to.

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
