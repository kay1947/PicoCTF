Python Wrangling
Overview
Points: 10 Category: General Skills

Description
Python scripts are invoked kind of like programs in the Terminal... Can you run this Python script using this password to get the flag?

Hints
Get the Python script accessible in your shell by entering the following command in the Terminal prompt: $ wget https://mercury.picoctf.net/static/8e33ede04d02f3765b8c6a6e24d72733/ende.py
$ man python
Approach
I tried running the code in the IDE but that didn't work. I navigated to the directory where the Python file was (make sure the flag file is in the same directory) and used python -d flag.txt.en (-d for decode I'm guessing, -e is probably encode). This asked for the password which I pasted from pw.txt and then it outputted the flag.

Note  if you are running this on Python 2, buffer doesn't work the same way as it does in Python 3. Line 49 of the Python script:

sys.stdout.buffer.write(data_c)
needs to be replaced with

sys.stdout.write(data_c)
Flag
picoCTF{4p0110_1n_7h3_h0us3_aa821c16}
