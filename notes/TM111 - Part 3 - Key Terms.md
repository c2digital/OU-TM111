---
title: TM111 - Part 3 - Key Terms
created: '2024-09-11T19:07:25.908Z'
modified: '2024-09-11T21:20:06.381Z'
---

# TM111 - Part 3 - Key Terms

- ** =**
- **Amplitude =** maximum displacement. For sound this will determine how loud it is. Measured from zero to the peak or from zero to the trough.
- **Analogue =** Defined as 'a thing that is comparable to another'. A contingous values as opposed to the discrete values of a digital signal.
- **Binary Word =** a set of given number of bits
- **Bitmap =** a coding scheme that allocate a binary code to each pixel to define its colour and brightness (often the larger format, not suitable for web due to file sizes)
- **Compression =** converting a digital file to a new file that uses considerbly fewer bits without significantly degrading the quality of the original content
- **Compression Ratio =** Size of uncompressed / size of the compressed (eg: 10MB / 2MB = 5:1)
- **Continguous Value =** a value that is measured
- **Cycle (waveforms)=** the time between adjacent peaks or troughs.
- **Discrete Value=** a value that can be counted
- **Digital Media =** the tools we used to create media (text/image/audio) and the idea of communicating (shring) them via the internet
- **Echo (sound) =** caused by the sound bouncing off a surface and returning. This will be recorded again as a slight delay
- **File Format =** an agreed-upom way of oraganising and storing binary data
- **Frequency =** the number of cycles in a given time period (usually one second)
- **Hertz =** 1Hz = one cycle per second (ie. the period between two adjacent peaks or two adjacent troughs is 1 second).
- **Pressure Wave =** a regular pattern of high and low pressure regions
- **Reverberation (sound) =** caused by sound repeatidly bouncing off a surface in a way that makes it impossible to differentiate from the original. Combines with the original sound to create a new sound - often referred to as 'adding body' to the sound.
- **Sample Rate =** the number of times per second a sample is taken
- **Sound =** the ears intepretation of vibrations in the air (or water etc). An analogue signal.
- **Sound sample =** As images can be split into pixels, a sound waveform can be split into 'samples'
- **Vector Graphic =** Instead of storing pixel information, stores information about the shapes in an image. Most appropriate where the graphic is made up of regular shapes (such as in games). Not useful for photos or videos.

## Notes

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
