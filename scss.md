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
  
```.content {
  background-color: $primary-color;
  color: $light;
  }
```

## Benefits:
  - makes CSS more efficient
  - makes stylesheets more maintainable
  - Allows use of variables, nested rules, mixins, functions etc.
  - free / open source
  
## Comments
  ``` /* standard css comments work! */ ```
  ``` // inline comments also work! ```

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

### Built-in modules
https://sass-lang.com/documentation/modules

## Nesting

`nav {
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
}`


## Partials
A way modularize your CSS and help keep things easier to maintain
A partial is a Sass file named with a leading underscore
The underscore lets Sass know that the file is only a partial file and that it should not be generated into a CSS file. 
Sass partials are used with the @use rule.

eg. `_variables.scss`

in styles.scss put 
`@import "variables";` //variables come first so other sass files can use them!

## Modules

## Mixins

groups of CSS declarations that you want to reuse throughout your site

@mixin directive and give it a name

## Extra

### Extend/Inheritance

### Operators

Sass has a handful of standard math operators like +, -, *, math.div(), and %


