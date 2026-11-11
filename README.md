# CSShiny
> by cerah #559

CSShiny is a CSS and HTML framework used to develop custom layouts for player catteries (profiles), player shops, and forum topics on the pet sim website [Mweor](https://www.mweor.com/). It is intended to streamline functionality while decreasing the amount of code exposed to the player, making it easier to prevent broken code.

In addition to the development framework, hosted files may include:
> Privately owned cattery custom layouts, commissioned cattery layouts, free-for use cattery layouts, forum topic layouts.
> Some content is pulled directly from Mweor's codebase for the sole purpose of local testing purposes.


Use of any code from this repo on Mweor without expressed permission is a violation of Mweor's Terms of Service section 3.6: Art Theft and will be reported.

Commands
> npx @11ty/eleventy --watch
> watches your files (and builds them when a change happens)

> npx webpack --watch
> watches your files (and builds them when a change happens)

> npm run watch
> runs both above commands

> ctrl + c 
> ends watch script

https://petrapixel.neocities.org/coding/git-tutorial#additional-commands


# Framework Structure
> Archive Folder
All old content pulled in from prior versions of CSShiny to be reworked for current version.

> Content Folder
Duplicates of Mweor HTML files for the use of local layout testing and building.

> Core Folder
CSS files to be called within a layouts main file. Reduces redundant code and allows for ease of remote updates.
core.css - Main resets file
Blocks - resuable chunks of CSS to be used with their corresponding HTML block in Nunjucks
Components - reusable chunks of CSS altering portions of out-of-the-box Cattery code.

> Layouts Folder
Compilation of SCSS/CSS, HTML, and images for use in player Catteries. Original SCSS and Nunjuck files are kept for updates, recompilation, and recovery purposes. Live layout assets; files are called when a layout is loaded.

> Nunjucks Folder
Reusable HTML content for testing and layout building purposes.
Notifications - Local duplicates of Mweor notifications soley for the purpose of local testing.
Blocks - reusable chunks of HTML providing functionality outside of Mweor's base HTML.
descbox.njk - Main file to be compiled and pasted into the Cattery description box. All HTML and CSS goes through this file.
starter.njk - Starter file for the Cattery Description box HTML.

> Public Folder
Compiled CSS files and HTML files for local testing purposes.

> SCSS Folder
Uncompiled SCSS for use of layout development. Files must be compiled by running them through the main.scss file before moving them to the Core folder.
Blocks - resuable chunks of CSS to be used with their corresponding HTML block in Nunjucks
Components - reusable chunks of CSS altering portions of out-of-the-box Cattery code.
core.css - Main resets file
starter.scss - Starter file for new Cattery Layouts

> main.scss
Main file in compiling SCSS files and layout testing; all SCSS goes through this file