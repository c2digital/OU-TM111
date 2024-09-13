---
title: TM111 - Part 3 - Notes
created: '2024-09-12T07:51:05.410Z'
modified: '2024-09-12T07:51:16.297Z'
---

# TM111 - Part 3 - Notes

- Almost any analogue quyantity can be represented digitally and therefore coded as binary numbers
- A set of given number of bits used for data representation is called a binary word
- Sound can be visualised by drawing a graph of how far an air particle moves back a forth (displacement) as time passes.
- For sound, frequency determines the pitch (low/high) and amplitude determine the volume.

### Recording Sound:
- Sound is record using a microphone and converted to digital form. This provides immunity from signal corruption when being extensively processed and stored.
  - Step 1: Sampling
    - Sound is recorded by measuring the amplitude of the sound wave at regular intervals (called sampling). The number of times the same is taken per second is called the 'sample rate'.
    - A lower sample rate will result in a poor quality sound.
    - As digital sound is made up of discrete values it is impossible to perfectly reproduce the sound
  - Step 2: Quantisation
    - The maximum voltage range of the signal is divided into a number of discrete voltage bands
    - Each band is represented by a number (0.01V = 001, 0.02V = 010 etc)
    - Each sample is then mapped onto a band and is given the number which represents the band
    - This results in a string of numbers at regular intervals.
    - Sound waves of often mapped to 16-bit numbers which represent the quantisation levels
    - These can be plotted onto a graph and will show the waveform again
    - The faithfulness of the digital copy will depend on how many numbers we use to divide the voltage (eg. 8-bit will have less bands than 16-bit)
    - The ear generally cannot tell the different in pitch of less than a few hertz
  - Audio in raw form takes alot of memory

## Compression

### Lossless Compression
- Stored in a way whereby the original can be restored with nothing altered. Nothing taken away or lost.
- Examples are .zip
- One example of lossless encoding is 'dictionary-based encoding'.
- In most digital files, the same data is repeated many times. The compression algorithum scans for these patterns and translates them into something that takes less space.
- Run length encoding can take repeated contiguous data and replace them with one instance and the number of times to repeat it

## Lossy Compression
- Data will be removed and cannot be recovered, hopefully data that is redundant or won't be noticeable
- 
