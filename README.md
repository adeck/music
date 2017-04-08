# music
## What's this repo?

I keep the musical scores for my original compositions here in vextab format.

## ...Huh?
### First off, what's Vextab?

[Vextab][vextab] is a plaintext file format for describing musical scores, specifically for guitar music. It was intended to be easy to write and, imo, it's better than the alternatives I've looked at. Ideally, my stuff would be translated into MusicXML or some other standard compositional format to make it easier to actually autogenerate playable audio (e.g. MIDI files), but frankly this is good enough for my needs right now.

### "musical compositions"?

I've been playing guitar for 14 years at this point (before that I played violin for four years). Most of that time I've been playing classical-style guitar. For various reasons, though I can read guitar music, my sightreading is really slow. So every piece I know I have memorized.
Playing other people's compositions is a lot of fun- Sor, Carulli, Barrios-Mangore, etc.
However, every time I play I end up composing something and playing that instead.

About a year or two ago I decided to start recording the things I've been composing so I don't forget those pieces. At this point I have a collection of pieces I'm kinda proud of, and don't want to lose. Haven't put the recordings on the internet, because I think they're a bit rough and not ready for public consumption. But I do like them enough that I want to have actual musical scores for them.

<!--
Before two years ago I was terrible about recording things. So the only original composition I have recorded from before two years ago is [this guy][song_for_june], recorded on my phone at two in the morning. Compositionally, it's certainly not my best work. But I dunno. I still like it. Wrote it for my girlfriend at that time.
-->

## What kind of music?

My musical tastes are all over the place, and are inspired by a number of different styles and traditions.
But most of the stuff that's going on here will be classical / celtic / roots blues-inspired. None of the compositions I currently have recorded have any lyrics to them. Frankly, I usually consider adding lyrics to be an admission of musical failure.

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
Then navigate your browser to `http://localhost:1234/flight`, to get the score + tabs for the piece called `flight`. For the list of pieces available, just look in the `pieces` directory in here.

Hopefully obvious, but `example` isn't actually a piece by me. It's just an example (as the name suggests) from the vexflow site.

## Copyright?

I own the copyright for all the music, here, with the exception of the `example` piece.
If you want to use any of it in something, ask my permission, first.

[vextab]: http://www.vexflow.com/vextab/
[song_for_june]: https://soundcloud.com/andrewdeck/song-for-june

