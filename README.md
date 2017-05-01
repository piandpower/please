# "Please" - an experimental programming language

**Simply put:** program by talking to your computer with words that sound *more* like everday English words. 

**More technically:** you can easily write code in Please using speech recognition software (like Mac Dictation) without having to train the software to recognize special keywords and symbols. 

# Example code in Please:

First transcribe this code:

```
Please print this string of words
```

When you run that code, it prints out:

```
this string of words
```

# Use:

1. Download this project from GitHub. https://github.com/hchiam/please/archive/master.zip --> master branch.

2. Open the folder using Terminal or Command-line.

3. Then input the following command and hit enter:

```
python interpreter.py text.txt
```

The *interpreter* will interpret and run the *text* file as "source code" written in Please.

Requires Python: https://www.python.org/downloads

# Why?

What if you could easily write code just by talking with speech recognition software? What if code could be *more* like English sentences? How might you combine these two things (easy-to-parse and easy-to-say code)?

Please is an attempt at that.

Here are 3 ground rules to make commands easier to say, but also easier for speech recognition software and Please's code interpreter to understand:

1. **Just say words that use your ABCs and spaces between**. No special non-letter characters like "?". Why? Speed and recognition. Saying "question mark" just to type out "?" is slow and could be faulty if the speech recognition software thinks you literally want the words "question mark". Please also doesn't differentiate (non-)capital letters because it's a speech-based language (vs. a "written language").
2. **Avoid specialized words or names**. Why? So you don't have to specifically train your speech recognition software to recognize uncommon words like "numpy" (mine thought I said "numb pie"). Workaround/trade-off: you have to spell it out, maybe using the first letters of more common words, like "**N**eptune **u**nicorn **m**oose **p**anda **Y**oda" to spell out "numpy". Afterwards, you can reassign "numpy" to a shorter label that uses more common words, like "numb pie" or "pneumatic".
3. **"Say please"**. Each new sentence starts with "please" and roughly marks out a new command or line in the code. The computer will try to run your code.

# More Example Code:

## Print:

```
Please print this string of words
```
--> This prints out: `this string of words`

## Create Variables:

By design, Please encourages you to use words instead of letters and short forms -- you're saying it out loud.

```
Please create variable apple
```

or

```
Please variable banana
```

## Assign Values to Variables:

```
Please assign one to variable apple
Please assign three hundred to variable banana
Please assign some words to variable coconut
```
--> This generates: `apple = 1`, `banana = 300`, `coconut = 'some words'`.

Note: variables automatically get created if you didn't already create them.

## Math:

```
Please one plus two
```
--> This outputs: `3`

```
Please one plus one equals two
```
--> This outputs: `True`

## If-Then Statement:

```
Please if one equals one then print it works
```
--> This prints out: `it works`

```
Please if one equals two then print it should not print this
```
--> (This doesn't print anything.)

## Comments/Notes:

```
Please note this is a comment
```
--> (The interpreter ignores this sentence.)

## Spell Out a Special Word:

```
Please spell with the first letters of Neptune unicorn moose panda Yoda
```
--> This outputs: `numpy`

Note: capital letters are the same as lowercase letters. Please is case-insensitive.

## Import to Add Functionality:

```
Please import alternate
```
--> This imports: alternate.py (from the local folder)

```
Please import test from library
```
--> This imports: /library/test.py

```
Please import spelled with the first letters of Neptune unicorn moose panda Yoda
```
--> This performs: `import numpy`. (You can spell out "numpy" since it's not an everyday word, and your speech recognition software might not already be trained to recognize it.)

```
Please import spelled with the first letters of Neptune unicorn moose panda Yoda as noodle
```
--> This performs: `import numpy as noodle`. (So no need to spell it out each time you use it.)

```
Please import spelled with the first letters of Neptune unicorn moose panda Yoda as numb pie
```
--> This performs: `import numpy as numb pie`. (You can also just rename it to whatever your speech recognition software thinks you're saying.)

## Use An Import Module's Function:

```
Please import test from library
Please use test_function of test
Please use test_function from test
```
--> This performs twice: `test.test_function()`

--> This prints twice: `Yay the import test_function() of test.py from the "library" folder works!`

# Inspirations for Please:

https://github.com/hchiam/programmingByVoice

https://github.com/AnotherTest/-English

https://www.youtube.com/playlist?list=PLBOh8f9FoHHiKx3ZCPxOZWUtZswrj2zI0

# Ideas for Development:

(See the Issues list. Click the "Issues" tab above or go to https://github.com/hchiam/please/issues)
