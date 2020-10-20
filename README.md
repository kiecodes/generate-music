# Can AI make music?

Hello. Thank you for being here. This repository belongs to the youtube video [Can AI make music?](https://youtu.be/aOsET8KapQQ).
If you haven't seen it, please consider watching the video, to get a better understanding of this code.


<p align="center">
  <a href="https://youtu.be/aOsET8KapQQ" target="_blank">
    <img src="http://i3.ytimg.com/vi/aOsET8KapQQ/hqdefault.jpg" alt="Can AI make music?">
  </a>
</p>

## Content

The following files are included:
|File| Description |
|--|--|
| algorithms/genetic.py | The genetic algorithm library. You can find more about it here: https://github.com/kiecodes/genetic-algorithms |
| mgen.py | The actual implementation of the music generation using a genetic algorithm. 
| requirements.txt | Python library requirements to use with pip.

## How to use this script

First you need to install the requirements you need to run everything. This repository contains a requirements.txt file.

To install the needed requirements:

```
$ pip install -r requirements.txt 
```

To start the script call:

```
$ python mgen.py
```

The script will ask you to define couple parameters:

| Name | Description |
| --| -- |
| Number of bars | Length of the generated melody in bars
| Notes per bar | Number of notes inside of a bar
| Number of steps | Number of pitches per note
| Introduce pauses | Should the algorithm introduce pauses betwen notes or do you want a constant stream of notes?
| Key | Key of the scale the melody should fit in
| Scale | Type of scale the melody shoud fit in
| Scale Root | Pitch of the scale (ex.: 4 means C4 is the root note of a scale in C)
| Population Size | Number of melodies per generation to rate and recombine
| Number of mutations | Max number of mutations that should be possible per child generated
| Mutation probability | Probability for a mutation to occur

After you defined all parameters above the genetic algorithm will generate a population of melodies and play each one back to you. After each playback you can rate the melody. 

Each generation all melodies are saved in midi format to disk using the following system:
```
<timestamp>/<generation>/<rating>.mid
```

## Contribution

This melody generation script is far from perfect and any contribution is welcome. Please feel free to fork this repository. Any pull request or comment is welcome!

Have a great day Coders!