As a developer, you may often be asked to implement designs that someone else has created. Time to practice that!

For this challenge, you're going to partially re-create sections of the Launch home page, following [the design shown here.](http://i.imgur.com/0JsOlMC.jpg) (It's like Slacker News, but prettier!) This will involve both using the tools Foundation provides, and writing your own custom CSS.

### Instructions

Download the challenge to get the starting files. The Foundation files have been set up for you, along with some useful images located in `/public/images`. (To use them in your stylesheets and `img` tags, you can use the filepath `/images/filename.png`.)

Write your own styles in `style.css`. Add the necessary HTML both to `layout.erb` (i.e. for the page header) and `index.erb` (for the page content). Your goal is to create a web page with [this design.](http://i.imgur.com/0JsOlMC.jpg)

For the core assignment, don't worry about changing the font - just use Foundation's default font.

To find the exact hex codes for some of Launch's signature colors, visit our [internal styleguide](https://launchpass.launchacademy.com/styleguide) and copy the hex codes from there! (The styleguide is a tool we build to use with our own development work.) 

### Tips

When approaching this challenge (and all future Foundation work!), you'll have to do some experimenting in order to figure out how to override some of Foundation's base styles. For example, if you try just putting a `background-color` on `.top-bar`, you'll have some success - but you'll see that some elements *within* the top bar still have a grey background color. By digging deeper and experimenting (with a lot of "Inspect Element"), you can find that if you *also* put your own background color on `.top-bar li`, then you'll see the result you want.

When changing the color of the top-bar text, you'll have to get even *more* specific. Changing the `color` property for `.top-bar li` will change the main title's color, but the links are still blue. You'll have to specifically target the `<a>` elements inside the top bar in order to change their color.

Here are some more miscellaneous tips to help you on your way!

- `<hr>` is an HTML element that will draw a horizontal line on the page. (I.e. for underneath the text that says "Campus", "Online", etc!)
- By default, Foundation `row`s have a max-width that constrains their size on large screens. If you want to have a row that has a custom background color, you might need to override that manually by putting `max-width: none` on that specific element.
- If you try wrapping a plain old `div` around things with the class `columns`, [you're going to have a bad time](http://i.imgur.com/hCcdiag.png). Remember, `.columns` automatically have the style `float: left;` or `float: right;`! That means normal parent `div`s will not pay attention to them, and kind of forget they exist. So if you're trying to give a background-color to some parent element, and it never seems to be tall enough to properly contain it's children... that's probably why.
- Foundation `row`s and `columns` are specially equipped to handle that ^problem! They can safely contain other `row`s and `columns` with no problem.
- You are going to be writing a lot of your own styling. Add your own custom class names to specific page elements in order to style them the way you want.
- Don't forget that it's *totally fine* (and even recommended!) to add your own custom class names to page elements that *also* have Foundation-y class names like `row` or `columns` or `callout` or `button`.
- If a background image isn't stretching the full width that you want it to, try `background-size: cover;`

### Bonus: Google Fonts

As a finishing touch, add a Google font to make all your typography prettier!

1. Go to [Google Fonts](https://www.google.com/fonts) and search "Roboto Slab"
2. Click "Add to Collection"
3. At the bottom of the page, click "Use"
4. Part way down the page, they give you a code snippet that you can add to your website to import the Google font. By default, they show you a `link` tag you can add to your HTML. I prefer to add a line to my CSS file to import the font. Click the "@import" tab at the top of the code snippet box. Copy that text and put it at the top of your stylesheet.
5. Now, whenever you want something to be the font Roboto Slab, you can write `font-family: 'Roboto Slab', serif;`. Write the necessary CSS to change all text to Roboto Slab.
6. Make sure all the font-sizes look nice, and change them if they don't!
