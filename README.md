# Мир, какой он есть (The World as It Is)

Track 10 of 10 on «Крылья» (_Krylya_, “Wings”), the album by за/обложкой (_za/oblozhkoy_).

On the site: https://vovazakharov.com/music/world-as-it-is

## Files

- `world-as-it-is_mix.mp3` — the mix, unmastered: what the master was made from.
- `world-as-it-is.mp3` — the master, as the site plays it.
- `mastering/` — the script that made the master: `master.py`, the `spectrum.py` it imports, and their `requirements.txt`.

## How it was mastered

```sh
pip install -r mastering/requirements.txt
python mastering/master.py world-as-it-is_mix.mp3 letim.flac world-as-it-is.mp3 --strength 0.5
```

with `ffmpeg` on `PATH` and `letim.flac` downloaded from below. Each song on the album was
mastered on its own against that reference, at half strength: Matchering
matches the mix to the reference, half of the EQ difference between that match
and the mix goes onto the mix, and a limiter keeps the decoded mp3 under
-1 dBTP. `master.py`'s docstring has the whole chain.

## The reference

`letim.flac`, a later за/обложкой master of «Летим» (_Letim_, “Let’s Fly”), at
[vovas-music/letim@abb7652](https://github.com/vovas-music/letim/blob/abb76529abd53ce4216181243875d534e9a9638c/letim.flac) — raw download:
https://raw.githubusercontent.com/vovas-music/letim/abb76529abd53ce4216181243875d534e9a9638c/letim.flac

It is linked rather than copied here: it is 24 MB and already lives in this
organization.
