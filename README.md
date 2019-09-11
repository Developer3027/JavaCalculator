# JavaCalculator

[Intro to WebDev2](https://btholt.github.io/intro-to-web-dev-v2/)

This calculator is built with a html base, css style, and vanilla javascript to make it work. It is a project off of front end masters. 

**Requirement**

![Calculator](img/JS_calc.jpg "JS Calculator")

* The calculator should look like the above image
* The calculator should function like a normal calculator
* Do not implement ```%``` or ```..``` You can assume everything will be an integer.
* ```C``` means clear. When a user clicks it, it should clear everything and go back to the first       state it was in when the page loaded.
* Doing the back arrow is extra credit. It's like pressing backspace; it'll delete the last             character typed. If it's clicked when there's only one digit, it sets the current number to be      0.
* Don't worry about if the number is too long for the screen.
* Calculators tend to have some special behavior when you hit equals: if you type another number it     erases the results and starts over. Feel free to do that but also free free (like me) to just       treat it normally and make the user hit ```C``` if they want to clear it. Let's keep it simple.

## HTML and CSS Tips and Hints

* Programming is all about taking large problems and breaking them into smaller problems. If you're     trying to tackle too much at once, break it into two smaller problems and try to solve one of       those.
* Personally, I wrote the HTML and CSS first. Once that's all taken care of, then I do the              JavaScript.
* For the font of the "result screen" I'd just use ```monospace```.
* There are so many ways to write this. There is no one right way. My solution is not the only nor      is it the best solution. Experiment. Try. Fail. Succeed. It's all about learning here.
* Good idea to use ```<button></button>``` for the buttons. You have to deal with some extra            styling stuff but it will make your code work pretty much automatically for disabled people. In     general when writing HTML, if something serves the function of a button, make it a ```<button></    button>```.
* I used multiple rows of flex layed out divs for the button. You could do it all in one div using      the flex-wrap property.
* The secret to getting equal gutters (which is what you call the black space between buttons): you     can set width to be ```24.5%``` (so four of them fit on a line) and then use ```justify-cotent:     space-between``` to evenly space them. That'll give them a gutter of roughly ```.5%``` of the       whole width. The problem with using percentages in conjunctions with ```heights:``` your            heights and widths are different. 5% of height is not the same of 5% of width, and that'll make     the gutters look weird. You want the bottom gutters to be the same size as the side gutters.        margin-bottom to the resuce! If you give the row a margin-bottom of .5% (if you're using my         same numbers) then that'll work since margin is always measured as a function of width (just        one of those things you have to know!) Hopefully that helps.
* Sometimes I do the math to get things right. Sometimes I just guess-and-check to see if it looks      okay.
* You can add a class to get the orange buttons. Or you could try ```:last-child``` (assuming you       have row div.)

## JavaScript hints and tips

* Again, no wrong way to do this. I wrote about 80 lines of JavaScript to finish the project (not       including empty lines.) I say that so you have an idea of how much code you should be writing. * If you're writing 200+ lines of code, you may want to rethink some of your solutions. Don't feel       like you're going for the smallest possible answer. You're just going for correct.
* I use console.log everywhere while I'm writing code. Just remember to take them out at the end.
* Many small functions is very preferable to one large function. Have each function do one thing        well as opposed to having giant functions that do everything. If you find a function doing too,     break it into smaller pieces. I solved it with eight different functions.
* You'll need to keep track of several variables. Make sure these variables are stored in a place       where they stay in scope.
* You can add an event listener to each button individually, or you can use one listener at the         root of the button. I did the latter but it's up to you