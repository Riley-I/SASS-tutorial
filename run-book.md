# SASS Set-up Run-book

*if node.js is installed can install SASS using NPM:*

1. `npm install -g sass` 

2. if not, can download from [GitHub](https://github.com/sass/dart-sass/releases/tag/1.50.0)
**Note:** Detailed instructions here *https://sass-lang.com/install*

Or try:
`sudo apt install ruby-sass`

Check it installed correctly
`sass --version`

3. Create your directories, an *index.html* file and a *styles.scss*.
**Note:** *styles.css* will be created automatically on first --sass watch command but you can create it too if you'd like*

    |-- MY-PROJECT
            |-- index.html
            |-- SCSS
                |-- styles.scss
            
4. Navigate to directory with scss files 

5. Run sass command with --watch tag `sass --watch input.scss output.css` (change *input.scss* to your scss file name ie **styles.scss** and *output.css* to **style.css**)
**Note:** *tells Sass to watch your source files for changes, and re-compiles CSS each time you save your Sass*

You should now get this in your terminal:

`Compiled styles.scss to styles.css.
Sass is watching for changes. Press Ctrl-C to stop.
`

**Note:** a *style.css.map* file will be created in your SASS directory

**Note:** the **styles.scss** file is now where you will do all your edits! :joy: 

6. Now, you can create your partials (ie variables file _variables.scss) and @import to your styles.scss file

