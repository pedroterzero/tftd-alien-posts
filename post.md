**Title:** TFTD: aliens abandon their posts (DOS vs OpenXcom test)

Hi all,

Something about the second stage of the Artefact Site has bugged me for a long time, so I finally tested it.

**What I remember from the DOS game.** The big chamber you cross on the way to the Synomium Device was one of the riskiest rooms in the game. Aliens sat in the alcoves high in its walls and stayed there until you killed them. The Tentaculats in particular camped up there and only came out when one of your aquanauts walked into view, and then you had a zombie. You had to take that room alcove by alcove.

**What happens in OpenXcom.** The same room always feels empty by the time I get there, and it turns out that is exactly what happens: the room empties itself. The aliens that start in the alcoves leave on the first turns and spread over the map, so they reach you a few at a time in the corridors, and by the time you get to the chamber it is a large deserted hall. The set piece the level seems to be built around never takes place.

**The test.** I generated battles in the DOS game (under DOSBox), saved on turn 1, and converted that save into an OpenXcom save: same map, same aliens on the same tiles with the same equipment. Then I let 30 turns pass in each game with my squad standing still at its starting point, saving every turn, and compared where every alien was. OpenXcom was a current nightly (commit 4a4bae5), vanilla TFTD rules.

Aliens that started in the final room:

| Battle | Started in the room | DOS: left within 30 turns | OpenXcom: left within 30 turns |
|---|---|---|---|
| B (Beginner) | 7 | 0 | 7, six of them by turn 5 |
| C (Beginner in DOS, Veteran in OpenXcom) | 11 | 0 | 10, all on the first alien turn |
| D (Veteran) | 12 | 4 | 12, eleven by turn 4 |
| F (Veteran) | 12 | 2 | 10, all by turn 5 |

**The pounce.** I then put one unarmed aquanaut on the chamber floor in view of the alcoves. In the DOS game a Tentaculat left its alcove on the very first alien turn and zombified him (same outcome on a second try), while the other six Tentaculats stayed where they were. In OpenXcom, from the same position, nobody charged him in 12 turns.

**It is not only that room.** TFTD's maps have more places where aliens start at a post of their own, away from the main patrol routes. I ran the same test on three of them, all on Veteran:

- **Alien Colony, first stage.** The centre of the map holds a garrison of six, and there are smaller posts around it, 20 aliens in all. In the DOS game the garrison circled inside its own block for all 30 turns and none of the 20 left their post. In OpenXcom all 20 left, most within five turns.
- **Port terror site.** A Tasoth started on the upper floor of the dock building, the one with the outside staircase. In the DOS game he stayed upstairs for 30 turns; in OpenXcom he came down on turn 6. Of five aliens at posts like this, none left in DOS and four left in OpenXcom.
- **Artefact Site, first stage.** Two Tentaculats and a Tasoth started at posts of this kind, two of them on the upper floors of the pyramid. All three stayed in DOS; all three left in OpenXcom by turn 6.

In every one of these battles the aliens on the main patrol routes roamed the map in both games, so this is not the DOS aliens being passive across the board. The DOS game has aliens that roam and aliens that hold a post, and in OpenXcom nearly all of them roam.

This looks specific to TFTD. Going by the map files, TFTD has about a hundred posts of this kind and UFO: Enemy Unknown has none, which may be why it went unnoticed.

Whether a room full of camping Tentaculats is good design is a matter of taste. Whether the DOS game played that way is not, and the test says it did.

For me that room is one of the things that made TFTD what it was. I would like to see these places work in OpenXcom the way they did in the original, even if only for these specific parts of the game and even if only as an option. I have the saves from both games, the per-turn positions of every alien and the save converter, and I am glad to share them or run more comparisons if that helps.

Timelapses (DOS left, OpenXcom right; each page is interactive, with a per-alien table):

- [Artefact Site final room, battle B](https://pedroterzero.github.io/tftd-alien-posts/artefact-final-room-B.html)
- [Artefact Site final room, battle D](https://pedroterzero.github.io/tftd-alien-posts/artefact-final-room-D.html)
- [Artefact Site final room, battle F](https://pedroterzero.github.io/tftd-alien-posts/artefact-final-room-F.html)
- [Alien Colony entrance](https://pedroterzero.github.io/tftd-alien-posts/colony-entrance.html)
- [Port terror site](https://pedroterzero.github.io/tftd-alien-posts/port-terror.html)
- [Artefact Site, first stage](https://pedroterzero.github.io/tftd-alien-posts/artefact-stage-1.html)
- [Recording of the DOS alien turns, battle B](https://pedroterzero.github.io/tftd-alien-posts/media/rec_B_dos_alien_turns.mp4) (map and aliens made visible)

![Artefact Site final room, battle B](https://pedroterzero.github.io/tftd-alien-posts/media/timelapse_B.gif)
