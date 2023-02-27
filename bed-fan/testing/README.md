[:arrow_left: Back to Table of Contents](/README.md)

### Test setup
All these tests were only performed once. No averages taken.

The ambient temperature was around 70F for each test.

I'm running [Darkdogs ender 3 conversion](https://github.com/boubounokefalos/Ender_SW ) Rev1, with modifications of my own (mostly to do with the enclosure). 
These tests are using that encloser's dimensions. I am using thicker plexiglass (6mm) and wood panels instead of coriplast. I also added some 'insulation' to some areas.

### Tested with 110V / 500W bed
A big factor in theses tests. I'm running a 110v AC bed heater, 500W. A stock ender bed might in theory would get similar results, but it will take so long to heat up while bed fans keep cooling it off, that it will throw a klipper error after a few mintues. Yeah you can monkey with that stuff, but I don't really recommend it. Even if you got past the warnings/errors, it'd take 45+ minutes to get to temperature for every print.

Chamber Thermistor location
![](/bed-fan/testing/images/chamber_thermistor.jpg)

I added a nevermore to the back of the enclosure, it blows across the top of the chamber, towards the doors
![](/bed-fan/testing/images/nevermore.jpg)

All tests used a macro to set the same bed (105C) and hotend (115C) and to 'park' the bed and hotend in the center. I took the final measurement whenever "I felt like" the temerapure stopped climing. Typically if I didn't see an upward trend over about 20 minutes, I called the test and moved on. 

Each test took about an hour or so to run.

I wanted to share these results for a couple reasons, but mostly so I can test other's ideas too. So, let me know if you have a fan position you want to test!

### Test results

Baseline test - no fans - 55.6
![](/bed-fan/testing/images/no_fans.jpg_)

Test 1 - only parts fan - 53.6
![](/bed-fan/testing/images/only_part_fan.jpg_)

Test 2 - Nevermore and parts fan - 53
![](/bed-fan/testing/images/parts_and_nevermore_fans.jpg_)

Test 3 - Only bed fans (pos 1) - 57.5

Test 4 - All 3 fans, pos 1 - 62.2
![](/bed-fan/testing/images/pos_1.jpg)

Test 5 - All 3 fans, pos 1 flat- 57.1
![](/bed-fan/testing/images/pos_1_flat.jpg)

Test 6 - All 3 fans, pos 2 - 56.6
![](/bed-fan/testing/images/pos_2.jpg)

Test 7 - All 3 fans, pos 3 - 53.3
![](/bed-fan/testing/images/pos_3.jpg)
