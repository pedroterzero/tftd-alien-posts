**Title:** TFTD: aliens abandon their posts (DOS vs OpenXcom test)

Hi all,

Something about the second stage of the Artefact Site has bugged me for a long time, so I finally tested it.

What I remember from the DOS game: the big chamber you cross on the way to the Synomium Device was one of the riskiest rooms in the game. Aliens sat in the alcoves high in its walls, sniping at you, and stayed there until you killed them. They overlooked the hall you had to cross and the stairs you had to climb. The Tentaculats in particular camped up there and only came out when one of your aquanauts walked into view, and then you had a zombie. You had to take that room alcove by alcove.

In OpenXcom the same room always feels empty by the time I get there. I wanted to know if that's just my impression, and it isn't. The aliens that start in the alcoves leave in the first few turns and spread over the map. They come at you a few at a time in the corridors, and when you finally reach the chamber it's a big empty hall.

Here's how I tested it. I generated battles in the DOS game (under DOSBox), saved on turn 1, and converted that save into an OpenXcom save: same map, same aliens on the same tiles with the same equipment. Then I let 30 turns pass in each game with my squad standing still where it started, saved every turn, and compared where every alien was. OpenXcom was a current nightly (commit 4a4bae5) with vanilla TFTD rules.

These are the aliens that started in the final room, over four battles:

| Battle | Started in the room | DOS: left within 30 turns | OpenXcom: left within 30 turns |
|---|---|---|---|
| B (Beginner) | 7 | 0 | 7, six of them by turn 5 |
| C (Beginner in DOS, Veteran in OpenXcom) | 11 | 0 | 10, all on the first alien turn |
| D (Veteran) | 12 | 4 | 12, eleven by turn 4 |
| F (Veteran) | 12 | 2 | 10, all by turn 5 |

I also tried baiting them. I put one unarmed aquanaut on the chamber floor where the alcoves could see him. In the DOS game a Tentaculat came out of its alcove on the very first alien turn and zombified him, and did the same when I repeated it. The other six Tentaculats didn't move. In OpenXcom, from the same position, nobody charged him in 12 turns.

It's not only that room. TFTD's maps have more places where aliens start at a post of their own, away from the main patrol routes, so I ran the same test on two of them, both on Veteran.

The first stage of the Alien Colony has a garrison of six in the centre of the map and some smaller posts around it, 20 aliens in all. In the DOS game the garrison kept circling inside its own block for all 30 turns and none of the 20 left their post. In OpenXcom all 20 left, 18 of them within five turns. This is that battle, DOS on the left and OpenXcom on the right:

![Alien Colony entrance](https://pedroterzero.github.io/tftd-alien-posts/media/timelapse_H.gif)

In the port terror site a Tasoth started on the upper floor of the dock building, the one with the outside staircase. In DOS he stayed upstairs for 30 turns, in OpenXcom he came down on turn 6. There were five aliens at posts like that on the map; none left in DOS and four left in OpenXcom.

The aliens on the main patrol routes roamed the map in both games in all of these battles, so it's not that the DOS aliens are just passive.

I don't mean this as a complaint about OpenXcom's AI. Its aliens move around with a lot more purpose than the DOS ones, which often just stand there, and for most of the game that's clearly better. This looks to me like a side effect of that: the aliens that used to hold a post now get to wander like everyone else. It's probably also easy to miss because it seems to be a TFTD thing. Going by the map files TFTD has about a hundred posts like these and UFO: Enemy Unknown has none.

Whether a room full of camping Tentaculats is good design is a matter of taste, but the DOS game did play that way.

For me that room is one of the things that made TFTD what it was. I would like to see these places work in OpenXcom the way they did in the original, even if only for these specific parts of the game. I have the saves from both games, the per-turn positions of every alien and the save converter, if anyone wants them.

Timelapses for all the battles (DOS left, OpenXcom right, each page is interactive with a table per alien):

- [Alien Colony entrance](https://pedroterzero.github.io/tftd-alien-posts/colony-entrance.html)
- [Artefact Site final room, battle B](https://pedroterzero.github.io/tftd-alien-posts/artefact-final-room-B.html)
- [Artefact Site final room, battle D](https://pedroterzero.github.io/tftd-alien-posts/artefact-final-room-D.html)
- [Artefact Site final room, battle F](https://pedroterzero.github.io/tftd-alien-posts/artefact-final-room-F.html)
- [Port terror site](https://pedroterzero.github.io/tftd-alien-posts/port-terror.html)
- [Artefact Site, first stage](https://pedroterzero.github.io/tftd-alien-posts/artefact-stage-1.html) (not discussed above, three aliens at posts, same result)
- [Recording of the DOS alien turns, final room battle B](https://pedroterzero.github.io/tftd-alien-posts/media/rec_B_dos_alien_turns.mp4) (map and aliens made visible)
