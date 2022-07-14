## Change the colours

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
In this step, you will learn how to choose colours with RGB LEDs and change the colours on the SenseHAT to whatever you like!
</div>
</div>
<div>
<iframe src="https://trinket.io/embed/python/30c415346f?outputOnly=true&runOption=run&start=result" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

</div>

SO far, you have only accessed the default settings for the 64 RGB (Red, Green, Blue) LED bulbs on the SenseHAT - but they can be any colour you like!

[[[generic-theory-colours]]]

We can change how the message is displayed on the SenseHAT by adding some extra **parameters** to the `show_message` command.

You have already used `scroll_speed` - this affects how quickly the text moves across the display. The default value is `0.1`. The bigger the number, the lower the speed. This parameter **only** works with the `show_message` command.

+ `text_colour` changes the colour of the characters and is defined via three values to specify red, green, and blue. These are also called RGB values. This parameter will change the output of both `show_message` and `show_letter`.

+ `back_colour`: changes the colour of the background and works in the same way as `text_colour`. This parameter will change the output of both `show_message` and `show_letter`.

Check out the sections below to learn more about RGB values.

[[[rpi-sensehat-display-colour]]]

--- task ---

**Type:** Add the following to your code <strong>inside the brackets</strong>: `, text_colour=(255,0,0), back_colour=(0,0,255)`. The examples use **red**:`(255,0,0)` and **blue**:`(0,0,255)` but you can choose any colours you like. 

**Tip:** The comma at the beginning is important as it shows where the two parameters are split - don't forget it!

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 25
line_highlights: 27
---
sense.clear()

sense.show_message("SenseHAT is Awesome!", scroll_speed=0.05, text_colour=(255,0,0), back_colour=(0,0,255))

--- /code ---

--- /task ---

--- task ---

**Test:** Run your code. You should see your single characters display in black and white, but your scrolling message should be in colour!

--- /task ---

--- task ---

**Debug:** 
+ What does your error message say? Which line has an error?
+ Does your code match the code above?
 
--- collapse ---
---
title: SyntaxError
---
+ Do you have only numbers after your `scroll_speed=` parameter?
+ Do you have three numbers separated by commas in each of your colour values in `text_colour` and `back_colour`: `(0,0,0)`?
+ Have you got the final closed bracket at the end of your code?

--- /collapse ---

--- collapse ---
---
title: TypeError
---
+ Have you spelled `text_colour=` and `back_colour=` correctly?
+ Do you have an underscore `_` in the middle?

--- /collapse --- 

--- collapse ---
---
title: NameError
---

+ Have you got only numbers between 0 and 255 in all of your colour values in `text_colour` and `back_colour`?

--- /collapse ---

--- collapse ---
---
title: ValueError
---
+ Have you got only numbers between 0 and 255 in all of your colour values in `text_colour` and `back_colour`?


--- /collapse ---
--- /task ---

--- save ---