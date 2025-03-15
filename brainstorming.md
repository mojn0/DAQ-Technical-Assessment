# Brainstorming


This file is used to document your thoughts, approaches and research conducted across all tasks in the Technical Assessment.


## Firmware


Added the library dbcppp to the firmware, was confused about how to do this, but a simple search led me to git's own website where they stated that you could add a submodule with the command:
```
$ git submodule add [URL]
```


Added dbcppp to the CMakeLists file, not sure if it's correct or not, I simply copied how solution was added to the Lists file.


Added Dockerfile to support dbcppp, had to search up what Docker was, since I was not familiar with it at all.


Currently, I have 2 main ideas on how to extract the timestamp, frameID and data bytes from the dump file:
1. Use a Python script to go through the dump
2. Make a bash script to split all fields and then remove all unnecessary values


Before doing extracting the dump file, I decided to parse the three DBC files first. For this, I looked through the repo and referred to the examples on how to use the parser. I then piped the output of the parsing to three text files, which now contain the human-readable versions of the dbc files.


I also experimented with the other formats of the parsing but found them to be of no use, at least currently.


In the end, I have decided to use a python notebook file to extract and parse the dump.log file. Currently, I am still trying to figure out how to parse and decode the can frames in dump.log.


For now, I will move on to the next stage for the sake of time.


Researching these protocols has been interesting, they all have their use cases and limitations. I can especially see why the CAN protocol is used as heavily in the automotive industry, its reliability makes it perfect to use as the connection between the many ecu's of modern cars. I can especially see why Redback Racing would use it considering how for their application, making a Race car, would require a robust and manageable system to interconnect all the systems of the car.


While choosing the chip, I was left with 21 different options, all of them stating that they have the same feature set as required. In order to cut all of these options down further, I first tried to limit them by the ones which consume the least amount of power, however, all 21 options had the same power consumption, both min max, thus I limited the options by max operating temp, a feature which can be necessary considering this will be used in mainly Australia and that race cars can get quite hot and at certain sections, specifically the batteries, motors and gears, will get to extremely high temperatures. Thus, this left me with 8 options. To pick the chip, I then chose by the median expensive chip, the STM32F765ZI.


For the physical requirements, I was not 100% sure, as there was no strict size listed anywhere.


## Spyder


## Cloud

