Also got support for 1541C/1541-II drives in the process, as well as supporting DolphinDOS 2.0

I did various layouts for the project, which later evolved into the amazing MeGALoDOS by tommy_nrw (in which I had no involvement, due to departing the Commodore community)

Full run of the 64er Speedtest (track display is *not* part of the project, but obviously compatible) here: https://www.youtube.com/watch?v=1nbLhu1RDvs

Only userport variant for now - expansion port variant maybe some day, as others did the layouts there.

Additionally to the files found here you'll need a 1541/1571 parallelcable with the usual pinout.



64'er Speedtest values (Userport - 1541 - 1MHz (@D0, @DY, @DL-)):

| Operation  | Time | Factor |
| ------------- | ------------- | ------------- |
| Format: | 18.1s | 4.12 |
| PRG Save: | 8.7s | 15.75 |
| PRG Load: | 3.8s | 33.42 |
| SEQ Save: | 15.1s | 5.7 |
| SEQ Load: | 14.7s | 5.17 |
| REL new: | 25.9s | 4.57 |
| Validate: | 9.6s | 6.88 |
| Scratch: | 18.3s | 3.77 |
| Transfer: | 16.8s | 4.29 |


64'er Speedtest values (Expansionport - 1541 - 2MHz (@D2, @DY)):

| Operation  | Time | Factor |
| ------------- | ------------- | ------------- |
| Format: | 17.4s | 4.28 |
| PRG Save: | 9.2s | 14.89 |
| PRG Load: | 3.9s | 32.56 |
| SEQ Save: | 11.2s | 7.68 |
| SEQ Load: | 10.0s | 7.6 |
| REL new: | 28.3s | 4.17 |
| Validate: | 9.4s | 7.02 |
| Scratch: | 15.1s | 4.57 |
| Transfer: | 11.1s | 6.49 |



I'm still looking for a C64 Kernal that uses the Expansionport and allows turning off the screen during load (Option "@DL+") which was mentioned in the manual, as well as a way to reproduce the 2.3 seconds for a 202 block read mentioned in the manual as well. Using the maximum options (@D2 (2MHz), @DN (no verify), @DL+ (screen off during load)) I can only get as low as 3.5s on real hardware so far.
