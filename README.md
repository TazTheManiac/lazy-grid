# lazy-grid
#### The grid generator for the lazy developer (or just the time conserving one).
###### NOTE! You will have to compile the SCSS file yourself.
## How to use
The first few lines in the file are some variables, namely these.  
```sass  
$number-of-columns: 12;  

$breakpoint-sm: 768px;  
$breakpoint-lg: 992px;  

$container-width: 100%;  
$container-max-width: 1200px;  
$gutter-width: 1.5rem;  
```
These control how your grid will generate, if you want a grid with only four columns, just change `$number-of-columns: 12;` to `$number-of-columns: 4;` and compile.  
If you want your container to have a max width of 960px, just change `$container-max-width: 1200px` to `$container-max-width: 960px` and compile.  
If you want to change a breakpoint, just... Yeah, you get it.  

### Column sizes  
  By default, there are three column sizes. sm, md and lg. If you want another size, just add one more breakpoint, copy a media query and change the prefix to any other prefix you would like.

### The structure
The basic structure of the grid looks like this.
```html
<div class="container">
  <div class="row">
    <div class="col md-12">
      "Content here"
    </div>
  </div>
</div>
```

It is also perfectly fine to nest it, just add another row inside a column.
```html
<div class="container">
  <div class="row">
    <div class="col md-12">
      <div class="row">
        <div class="col sm-6">
          "content here"
        </div>
        <div class="col sm-6">
          "content here"
        </div>
      </div>
    </div>
  </div>
</div>
```

One last thing, you can also omit the size specification of the column, and just add the class `.col`. That column will then take up the whole row.
```html
<div class="container">
  <div class="row">
    <div class="col">
      "This column will take up the whole row"
    </div>
  </div>
</div>
```

## License
Just do what you want with it really.
