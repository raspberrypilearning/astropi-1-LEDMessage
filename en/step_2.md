## Display single characters

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
In this step you will show single characters on the SenseHAT LED array in different rotations. Additionally, if you have a physical Sense HAT and Raspberry Pi, you will learn how to connect the two.

</div>
</div>
<div>
<iframe src="https://trinket.io/embed/python/27ab62b808?outputOnly=true&runOption=run&start=result" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
</div>

The Sense HAT is an add-on board for the Raspberry Pi, made especially for the [Astro Pi](http://astro-pi.org/){:target="_blank"} competition. The board allows you to make measurements of temperature, humidity, ambient light and colour, pressure and orientation, and to output information using its built-in LED matrix.

![Sense HAT](images/sense-hat.png)

You can program the Sense HAT using an online emulator.

[[[rpi-sensehat-emulator]]]

If you have access to a real Sense HAT you can attach it to your Raspberry Pi, using the instructions below.

[[[rpi-sensehat-attach]]]

The LED matrix on the SenseHAT is made of an 8 by 8 grid of RGB LEDs. Using python, you can control the LEDs to be any colour you like! 

Part of the `sense_hat` library allows you to show single characters on the LED array using `show_letter`. 

--- task ---

Open the [Trinket SenseHAT starter project](https://trinket.io/python/2064060101){:target="_blank"}. Trinket will open in another browser tab.

--- /task ---

With any python program, we start by `importing` the libraries we need. In this project you need `sense_hat` library which to control the SenseHAT, and the `time` library which allows you to pause your program.

--- task ---
**Add:** At the top of your new code window add the following lines: 

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 2-3
---
#Import the libraries
from sense_hat import SenseHat
from time import sleep
--- /code ---

--- task ---

Then set up the Sense HAT so that it can be controlled.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 7
---
#Import the libraries
from sense_hat import SenseHat
from time import sleep


#Set up the SenseHat
sense = SenseHat()
--- /code ---

--- /task ---

--- /task ---

Now, we need to add some code that will show a single character on your SenseHAT's LED array. The example uses the character `S`, but you can use any letter (capital or lower-case) or symbol you like from the latin alphabet.

<p style='border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;'>
There are many alphabets in the world, though the most commonly used one is the <strong>latin alphabet</strong>: ABCDEFGHIJKLMNOPQRSTUVWXYZ. At the moment, the SenseHAT only supports latin characters and symbols (!?$%^&*]>@\:;~[<+-=./,'#) but support for both the <strong>greek</strong> and <strong>cyrillic</strong> alphabets is in development.
</p>

--- task ---

Add code to output a single character to the LED matrix.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1 
line_highlights: 11
---
#Import the libraries
from sense_hat import SenseHat
from time import sleep


#Set up the SenseHat
sense = SenseHat()


#Show letters on the LED matrix
sense.show_letter("S")
--- /code ---

The final line calls the SenseHat library class `show_letter` and tells it you want to display a capital S.

**Tip:** When using `show_letter` you can only supply a single character. Trying to add multiple characters inside the brackets will result in a `ValueError`. 

--- /task ---

--- task ---

**Test:** Run your code. You should see your letter appear on the SenseHAT array.

--- /task ---

--- task ---

**Debug:**
+ What does your error message say? Which line has an error?
+ Does your code match the code above?

--- collapse ---
---
title: NameError
---
+ Have you got the capital letters and brackets correct in `SenseHat()` on line 7 and line 2?
+ Are you using `sense.show_letter`?
+ Is your letter inside quotation marks on the last line?


--- /collapse ---

--- collapse ---
---
title: ValueError
---
+ Are you trying to show more than one character at a time?
+ Are you using latin characters?

--- /collapse ---

--- /task ---

To spell a word, you need to display a series of letters in sequence.

--- task ---

**Choose:** What word would you like to display on your SenseHAT?

**Type:** At the bottom of your code, add two more lines. One which sets a time in seconds for the letter to be shown, and another to display the  second letter of your word. 

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1
line_highlights: 12-13
---
#Import the libraries
from sense_hat import SenseHat
from time import sleep


#Set up the SenseHat
sense = SenseHat()


#Show letters on the LED matrix
sense.show_letter("S")
sleep(0.5)
sense.show_letter("e")
--- /code ---

--- /task ---

--- task ---

**Test:** Run your code. You should see your letter change after half a second.

The number used in the brackets after `sleep` determines how long your letter will show for in seconds. The example uses half a second, but you can make it faster or slower by changing this value down or up. 

[[[generic-python-sleep]]]

--- /task ---

--- task ---

**Type:** Continue spelling your word one letter at a time until you have finished. 

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 1 
line_highlights: 14-28
---
#Import the libraries
from sense_hat import SenseHat
from time import sleep


#Set up the SenseHat
sense = SenseHat()


#Show letters on the LED matrix
sense.show_letter("S")
sleep(0.5)
sense.show_letter("e")
sleep(0.5)
sense.show_letter("n")
sleep(0.5)
sense.show_letter("s")
sleep(0.5)
sense.show_letter("e")
sleep(0.5)
sense.show_letter("H")
sleep(0.5)
sense.show_letter("A")
sleep(0.5)
sense.show_letter("T")
sleep(0.5)
sense.show_letter("!")
sleep(0.5)
--- /code ---

--- /task ---

--- task ---

**Type:** Add `sense.clear()` at the end of your code to clear the LED matrix:

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 27 
line_highlights: 32
---
sense.show_letter("!")
sleep(0.5)


#Clear the LED matirx
sense.clear()

--- /code ---

--- /task ---

You can rotate the LED matrix, so that it doesn't matter which way is up.

[[[rpi-sensehat-rotate-led]]]


--- task ---

**Type:** On line 5 in your code, add `sense.set_rotation(180)`:

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 5
line_highlights: 6
---
#Set up the SenseHat
sense = SenseHat()
sense.set_rotation(180)
--- /code ---

--- /task ---

--- task ---

**Test:** Run your code. The SenseHAT should display your text upside down.

--- /task ---

--- task ---

**Try:** Change the number from `180` to `90` or `270` and Run your code. 

What number do you need to use to show it the right way up? 

--- /task ---

--- task ---

**Debug:**
+ What does your error message say? Which line has an error?
+ Does your code match the code above?
 
--- collapse ---
---
title: ValueError
---
You can only use the values `90`, `180` and `270` in your rotation angle. 

--- /collapse ---

--- /task ---

In the next step, you will display a scrolling message on your SenseHAT display!

--- save ---
