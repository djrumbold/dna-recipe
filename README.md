## Useful Information
This project is built using the [DNA Recipe](https://github.com/dnadesign/dna-recipe)
Jira Board for this project - _add link_
Job Numbers: 
Read the [Standards Document](STANDARDS.md) before you do anything else

## Getting started
_NOTE: assumes you have node setup and gulp installed. If not, you should go do those things first_

Clone this repo
Using terminal:

	cd your-project
	composer update
	cd themes/default
	npm install
	gulp

Composer dependencies are intentionally not tied to versions, but you should update these to use specific releases before the site you are working on goes live

## Theme
The default theme uses:
* Sass: http://sass-lang.com/
* Gulp: http://gulpjs.com/
* Postcss + autoprefixer: This means we don't need to worry about browser prefixes in our own css. Autoprefixer will add these for us. http://postcss.org/
* Rucksack: "PostCSS CSS super powers library":  http://simplaio.github.io/rucksack/ This lets us do things like clear: fix;
* The PureCSS micro framework: http://purecss.io/ This is included via npm and a gulp task. If your project requires a more fully featured framework, just remove the references to pure.

Basic templates are provided, based on CWP templates using pure as a framework. Delete what you don't need.

## Styleguide
Once you have your silverstripe project setup, the styleguide should be available at:
	http://yourprojectdomain/sg/

Docs for the styleguide are available here: https://github.com/benmanu/silverstripe-styleguide

When you create a new component, please document it in the scss file, as we have in the examples.

## Custom breakpoints
It is recommended you work with the default grid where possible, but sometimes the 3, 5 and 24 grid may not be enough. Adding extra breakpoints and altering the grid units can be managed from the [breakpoints file](themes/default/build/sass/utilities/_var-breakpoints.scss). Please be cautious changing these in non-new projects, as some components are likely to have been built with the breakpoints and grid units as they are. 