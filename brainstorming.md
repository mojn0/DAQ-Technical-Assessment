# Brainstorming

This file is used to document your thoughts, approaches and research conducted across all tasks in the Technical Assessment.

## Firmware

Added the library dbcppp to the firmware, was confused about how to do this, but a simple search led me to git's own website where they stated that you could add a submodule with the command:
```
$ git submodule add [URL]
```

Added dbcppp to the CMakeLists file, not sure if its correct or not, i simply copied how solution was added to the Lists file.

Added Dockerfile to support dbcppp, had to search up what Docker was, since i was not familiar with it at all.

Currently, i have 2 main ideas on how to extract the timestamp, frameID and data bytes from the dump file:
1. Use a Python script to go through the dump
2. Make a bash script to split all fields and then remove all unnecessary values

Before doing extracting the dump file, i decided to parse the three DBC files first. For this, i looked through the repo and refered to the examples on how to use the parser. I then piped the output of the parsing to three text files which now contain the human readable versions of the dbc files.

I also experimented with the other formats of the parsing but found them to be of no use, at least currently.



## Spyder

## Cloud