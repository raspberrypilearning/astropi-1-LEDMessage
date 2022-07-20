
--- question ---

---
legend: Question 2 of 3
---

Why would the following lines of code cause and error when it is run.

```python
from sense_hat import SenseHat
sense = SenseHat()

sense.show_message("SenseHAT is Awesome!" scroll_speed=0.05)
```


--- choices ---

- (x) 
There is a missing comma (`,`) between the text and the scroll_speed.
  --- feedback ---
That is correct. Commas are needed to seperate different arguments.
  --- /feedback ---

- ( ) 
The `time` library has not been imported.
  --- feedback ---
The `sense_hat` library does not need the `time` library to control `scroll_speed`
  --- /feedback ---

- ( ) 
You can't use exclamation marks (`!`) in strings.
  --- feedback ---
The `sense_hat` library supports all the latin alphabet and punctuation marks
  --- /feedback ---

- ( ) 
The `scroll_speed` needs to be greater than `1`
  --- feedback ---
The `sense_hat` library is capable of outputing texts at scroll speeds less than `1`
  --- /feedback ---

--- /choices ---

--- /question ---
