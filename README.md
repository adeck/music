# music
## What's this repo?

I keep the musical scores for my original compositions here in vextab format.

## ...Huh?
### First off, what's Vextab?

[Vextab][vextab] is a plaintext file format for describing musical scores, specifically for guitar music. It was intended to be easy to write and, imo, it's better than the alternatives I've looked at. Ideally, my stuff would be translated into MusicXML or some other standard compositional format to make it easier to actually autogenerate playable audio (e.g. MIDI files), but frankly this is good enough for my needs right now.

At the end of the day if push comes to shove I can write my own vextab parser.
The onein the vextab repo's only ~800 lines, after all.
I'm feeling recursive descent...

### "musical compositions"?

I've been playing guitar for most of my life at this point.
Most of that time I've been playing classical-style guitar.
For various reasons, though I can read guitar music, my sightreading is really slow.
So every piece I know I have memorized.
Playing other people's compositions is a lot of fun- Sor, Carulli, Barrios-Mangore, etc.
However, every time I play I end up composing something and playing that instead.

<!--
NOTE: The below paragraph is essentially a lie because I recorded those pieces on my old phone, I didn't keep a backup, and now those recordings are locked away on my old phone that I still have lying around but haven't bothered to retrieve anything from.
No idea if it even still works.
I now keep backups.
But a lot of those recordings are, until / unless I get the data dumped from that old phone, effectively lost.

About a year or two ago I decided to start recording the things I've been composing so I don't forget those pieces. At this point I have a collection of pieces I'm kinda proud of, and don't want to lose. Haven't put the recordings on the internet, because I think they're a bit rough and not ready for public consumption. But I do like them enough that I want to have actual musical scores for them.

Before two years ago I was terrible about recording things. So the only original composition I have recorded from before two years ago is [this guy][song_for_june], recorded on my phone at two in the morning. Compositionally, it's certainly not my best work. But I dunno. I still like it. Wrote it for my girlfriend at that time.
-->

## What kind of music?

My musical tastes are all over the place, and are inspired by a number of different styles and traditions.
But most of the stuff that's going on here will be classical / celtic / roots blues-inspired.
None of the compositions I currently have recorded have any lyrics to them.

<!--
In high school I went through a phase of writing poetry and composed some stuff that was more rock to go along with the poetry. I still find that easy to do, but kind of as a consequence of finding it easy I don't really find it nearly as entertaining. That said, I might decide to do some of that for fun down the road.
-->

## How do I render the score?

Assuming you're using `virtualenvwrapper` you'd first...
```
mkvirtualenv music
```

...otherwise, just go right into:
```
pip install -r devel/requirements.txt
./serve
```
Then navigate your browser to `http://localhost:1234/2017/1/flight`, to get the score + tabs for the piece called `flight`. For the list of songs available, just look in the `songs` directory in here.

## Contributing?

Lol. Don't contribute to this.

That said, since I'm contributing, here are the contribution guidelines for myself:

### Terminology

I'll be calling these things `songs` and not `scores` or `compositions` or `pieces` because, although they don't have lyrics, it just feels more intuitive to keep the language here in line with normal vocabulary.

### Song names

For song names, each song needs a unique ID as well as a normal (display) name.
While the name might change, the unique ID cannot.
The unique IDs will be of the form `songid-{YEAR}-{SEQUENCE_NUMBER}`, where `{YEAR}` is the first year the thing has actually been written down, and `{SEQUENCE_NUMBER}` is an integer value starting at 1.
So the first song I commit to this repo in the year 2200 will have the ID `songid-2200-1`, and the second song will be `songid-2200-2`, etc.

Within the directory structure, the actual names of the files aren't meant to matter too much.
But two things do matter:

1. A given piece of music should have its songid somewhere in its file, and
2. for ease of reference, a song with songid-YEAR-NUM should be kept under `songs/YEAR/NUM/`

### Commits

I'd like to use a variation on [conventional commits] in this repo, whereby the commits might look something like `notes: gave songid-2024-1 an ending`.
The following is the list of commit types I'm using:

- notes -- anything that modifies pitches of the notes. Melody, bassline, countermelody, whatever. Whenever pitches change, it is a notes change.
- phrasing -- [musical phrasing]. Once I've written the notes down for a piece, I'll usually finesse that in a separate PR which fixes the phrasing- note lengths, added rests, time signatures, dynamics, etc.
- docs -- edits to READMEs, comments, etc.

## Copyright?

I own the copyright for all the music here.
If you want to use any of it in something, ask my permission, first.

[vextab]: http://www.vexflow.com/vextab/
[song_for_june]: https://soundcloud.com/andrewdeck/song-for-june
[conventional commits]: https://www.conventionalcommits.org/en/v1.0.0/
[musical phrasing]: https://en.wikipedia.org/wiki/Musical_phrasing

