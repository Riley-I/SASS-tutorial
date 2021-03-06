# Intro to SCSS (SASS)

## SASS
  - stands for 'Syntactically Awesome Stylesheet' :joy: 
  - open source
  - CSS pre-processor scripting language
  - compatible with all versions of CSS
  - designed & developed by Hampton Catlin by Natalie Weizenbaum in 2006
  - works with four syntax parsers: scss, sass, CSS, and less (scss most common)
  
## SCSS (stands for 'Sassy CSS') 
  - most commonly used syntax
  - uses curly brackets & semi-colons
  
```
  .content {
    background-color: $primary-color;
    color: $light;
    }
```

## Benefits:
  - makes CSS more efficient
  - makes stylesheets more maintainable
  - Allows use of variables, nested rules, mixins, functions etc.
  - free / open source
  - very flexible (can use any combination of functionality or, for example, only use variable)
  
## Comments
  ` /* standard css comments work! */ `
  
  ` // inline comments also work! `

## Preprocessing

## Variables

Sass uses the **$** symbol to make something a variable
```
  /* define variables for the primary colors */
  
    $primary: #a2b9bc;
    $secondary: #b2ad7f;
    $tertiary: #878f99;


  /* use the variables */
  
  .main-header {
    background-color: $primary;
  }

  .menu-left {
    background-color: $secondary;
  }

  .menu-right {
    background-color: $tertiary;
  }
```

https://sass-lang.com/documentation/variables

## Nesting

```
  nav {
    ul {
      margin: 0;
      padding: 0;
      list-style: none;
    }
      li { 
      display: inline-block; 
      }

      a {
        display: block;
        padding: 6px 12px;
        text-decoration: none;
      }
  }
```


## Partials
- A way modularize your CSS and help keep things easier to maintain
- A partial is a Sass file named with a leading underscore
- The underscore lets Sass know that the file is only a partial file and that it should not be generated into a CSS file. 
- Sass partials are used with the @use or @import (older) rule.

eg. `_variables.scss`

in styles.scss put 
`@import "variables";` //variables come first so other sass files can use them!

## Modules
- developed to solve some issues with @import used with partials
- newer functionality
- built-in modules: ??? math, color, string, list, map, selector, and meta

[css-tricks.com/introducing-sass-modules/](https://css-tricks.com/introducing-sass-modules/)

[sass-lang.com/documentation/modules](https://sass-lang.com/documentation/modules)

## Mixins

- groups of CSS declarations that you want to reuse throughout your site

- @mixin directive and give it a name
- uses @include at-rule

```
   @mixin clear-list {
    margin: 0;
    padding: 0;
    list-style: none;
  }
```

```  
   nav ul {
    @include clear-list;
  }
```
  

- Mixins can also take arguments, which allows their behavior to be customized each time they???re called.

[/sass-lang.com/documentation/at-rules/mixin](https://sass-lang.com/documentation/at-rules/mixin)

## Extra

### Extend/Inheritance
- Addresses the situation where one class should have all the styles of another class, as well as its own specific styles
- Sass???s @extend rule solves this.
- it tells Sass that one selector should inherit the styles of another.

``` 
  .awesome-class {
    border: 1px #f00;
    background-color: #fdd;

    &--serious {
      @extend .awesome-class;
      border-width: 3px;
    }
  }
```

### Operators

Sass has a handful of standard math operators like +, -, *, math.div(), and %


