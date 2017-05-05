# arducky
Parser that reads duckyscript from a file and generates an Arduino sketch

## How to use:
First you have to compile the c++ program to an executable.
To do so, navigate to the folder with the terminal

`cd path/to/folder`

Then compile it with g++

`g++ -o [executable_name] [source_name.cpp]`

Once it is compiled, you can interpret as many duckyscripts as you like, without compiling it again

To actually interpret the code, you have to put a file called `input.txt` in the same folder as the executable with the duckyscript in it and run it by executing it with `./[executable_name]`. A new `output.ino` file will be created, wich you can upload to the Arduino.

You can change the input or output file by adding args (input: -i), (output: -o).
For example: [executable_name] -i custom_file.txt -o test_project.ino

## Differences with other interpreters:
- It creates an Arduino file directly, not a text you have to copy-paste into a new file
- You can write Arduino code directly, for example a for loop and it won't get parsed
- More commands:
  `LOOP` will put all following code in `void loop(){}` so it keeps repeating forever

Thanks to [Seytonic](https://www.youtube.com/seytonic) and [Dckuino.js](https://github.com/Thecakeisgit/Dckuino.js)
