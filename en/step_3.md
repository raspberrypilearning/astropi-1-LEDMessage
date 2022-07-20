## Scroll text

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
In this step you will create a text message that will scroll across the LED matrix and change the speed it moves.
</div>
</div>

<div>
<iframe src="https://trinket.io/embed/python/4302ed5794" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
</div>

The SenseHAT can scroll a series of characters stored in a <strong>string</strong> across the LED matrix in any orientation. 


<p style='border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;'>
A <strong>string</strong> is a datatype made up of a series of characters. That means, the computer recognises the series of characters <strong>exactly as they are typed</strong>. Strings in python using quotation marks like this -  `"Hello reader"`
</p>

--- task ---

**Choose:** What message would you like to scroll across the SenseHAT?

--- /task ---
   
--- task ---

**Type:** At the bottom of your script, add the following line. The example uses the string `SenseHAT is awesome!`, but you can change it to anything you like
--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 25
line_highlights: 26
---
#Scroll text on the LED matrix
sense.show_message("SenseHAT is Awesome!")

--- /code ---

--- /task ---

--- task ---

**Test:** Run your code. You should see your single characters spell a word and then your message scroll across the LED array.

--- /task ---

--- task ---

**Debug:** 
+ What does your error message say? Which line has an error?
+ Does your code match the code above?
 
--- collapse ---
---
title: SyntaxError
---
+ Is your message enclosed in quotation marks? `"Hello reader"`

--- /collapse ---

--- /task ---

You are able to make the scrolling message move more quickly or slowly across the screen by changing the `scroll speed` **argument** down or up.

<p style='border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;'>
<strong>Arguments</strong> are the extra information you provide a function in order to have it work in a specific way. If I asked a barista-bot to just 'make me a cup of tea', I would likely get a <strong>default</strong> cup of tea with milk and sugar - the 'normal' version. If I gave <strong> arguments</strong> for my cup of tea when I asked; 'make me a cup of tea with NO milk and FIVE sugars' - that's the output I get. This is the same - we're asking the SenseHAT to scroll a message showing a <strong>specific string</strong>, at a <strong>certain speed</strong>.
</p>

--- task ---

**Type:** Add the following to your code <strong>inside the brackets</strong>: `, scroll_speed=0.05'.

**Tip:** The comma at the beginning is important as it shows where the two arguments are split - don't forget it!

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 25
line_highlights: 26
---
#Scroll text on the LED matrix
sense.show_message("SenseHAT is Awesome!", scroll_speed=0.05)

--- /code ---

--- /task ---

The speed of the message can be controlled by changing the number - the larger the number, the slower your message will move. 

--- task ---

**Try:** Make the decimal larger or smaller and run your code. Your message should change speed. Keep changing the number until you are happy with the speed of your message.

--- /task ---

--- task ---

**Debug:** 
+ What does your error message say? Which line has an error?
+ Does your code match the code above?
 
--- collapse ---
---
title: SyntaxError
---
+ Do you have only numbers after your `scroll_speed=` argument?
+ Have you got the final closed bracket at the end of your code?

--- /collapse ---

--- collapse ---
---
title: TypeError
---
+ Have you spelled `scroll_speed=` correctly?
+ Do you have an underscore `_` in the middle?


--- /collapse ---

--- /task ---

In the next step you are going to change the colours of the SenseHAT's text and background!

--- save ---
