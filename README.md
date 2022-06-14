# Ergo-stylus-converter

A fork of [Stylus-converter](https://github.com/txs1992/stylus-converter), modified to better suit our needs.

## Installation

1. Install stylus-converter globally


> npm i -g stylus-converter

2. Clone this repo to a local folder of your choosing and make it your cd

> git clone git@github.com:peaksandpies/ergo-stylus-converter.git  
> 
> cd "your cool folder"

3. Install the dependencies

> npm i

4. Build the project

> npm run build

5. Link the local build to the globally installed module. **Important!**

> npm link
  

(The next two steps refer to the conversion of all Stylus files in a folder)

6. Make sure you are on the latest version of the master branch of [ergo-landing-pages](https://github.com/peaksandpies/ergo-landing-pages). Verify that you can locate **/nextjs/migration-styl-sass-script/migrate.sh**

7. Add this line to your .zshrc file:

> alias migrate-styl="sh ~/Documents/ergo-landings/ergo-landing-pages/nextjs/migration-styl-sass-script/migrate.sh"

Change the path to your ergo-landings folder if needed.

8. Restart any open terminals

9. You're good to go! Run the tool according to the examples below.


## Use examples

```js
// Convert a single file
stylus-conver -i test.styl -o test.scss

// Convert all Stylus files in a folder
cd <your folder>
migrate-styl
```

## stylus-converter config

### converter options

| Attribute | Description | Type | Accepted Values | Default |
| ---- | ---- | ---- | ---- | ---- |
| `quote` | The quote type to use when converting strings | string | `'` / `"` | `'` |
| `conver` | Conversion type, such as conversion to scss syntax | string | scss | scss |
| `autoprefixer` | Whether or not to automatically add a prefix, stylus will automatically add prefixes when converting stylus grammars. `@keyframes` | boolean | true / false | true |
| `indentVueStyleBlock` | Indent the entire style block of a vue file with a certain amount of spaces. | number | number | 0 |

### cli options

| Attribute | Shorthand | Description | Accepted Values | Default |
| ---- | ---- | ---- | ---- | ---- |
| `--quote` | `-q` | The quote type to use when converting strings | single / dobule | single |
| `--input` | `-i` | Enter a name, which can be a path to a file or a folder | - | - |
| `--output` | `-o` | Output name, can be a path to a file or a folder | - | - |
| `--conver ` | `-c` | Conversion type, such as conversion to scss syntax | scss | scss |
| `--directory` | `-d` | Whether the input and output paths are directories | yes / no | no |
| `--autoprefixer` | `-p` | Whether to add a prefix | yes / no | yes |
| `--indentVueStyleBlock` | `-v` | Indent the entire style block of a vue file with a certain amount of spaces. | number | 0 |
