Introduction
------------

Currently (as of June 2011), **RogueStars** is nothing more than a little idea
and barely a skeleton of a program sitting somewhere in my PC. And, truth be
told, I cannot promise it will ever go further than that.

Assuming I can get it pass the vaporware stage, what is (or rather will be)
**RogueStars**? Well, it is sort of the bastard child of *Rogue* and the old
BASIC *Star Trek* game: a roguelike, in the tradition of such wonderful games as
[NetHack](http://www.nethack.org),
[Omega](http://www.alcyone.com/max/projects/omega/), [ADOM](http://www.adom.de)
and [DungeonCrawl Stone Soup](http://crawl.develz.org/wordpress/), but with a
Space Opera theme.

How does that differ from a myriad other science fiction roguelikes? For
starters, the player does not control some armor-clad, sword-bearing adventurer
going deep into a dungeon to fight monsters; he or she will instead command a
starship as it travels far and wide through the galaxy. Commerce, exploration,
piracy and the navy will be some of the available career options, as member of
one of several starfaring species, each with their own strengths and weaknesses.

The more traditional single-character viewpoint will still be available in some
situations, like starbase exploration and ship boarding. Or at least, that's the
plan.


Implementation
--------------

**RogueStars** is being written in the Ada programming language. Why? Because I
like it a lot more than C, C++ or Java, and, frankly, programming this game is
supposed to be fun, or I would be doing something else entirely with my time.

**RogueStars** will be implemented as a client/server application, where the
server handles the game in abstract terms, and the client provides the user
interface entirely: keybindings, ASCII vs. tiles, etc.

The default client will only support ASCII (or, more accurately, Unicode),
although it won't necessarily be a console app.

The server will be able to handle several games simultaneously, and each game
will be available to several clients at once: one playing client, and any number
of lower-priority read-only viewers.

The intent behind this client/server architecture is not providing a generic
"game engine", which **RogueStars** will definitely *not* be, but to facilitate
developing third party applications, like computer players and alternate
clients.

Currently, no part of the game is scheduled to be scriptable, though I don't
dismiss the idea of adding that capability to the client at some point.

Finally, I'd like the game to be localizable, but this is at the moment a low
priority goal.


Requirements
------------

To build **RogueStars** you will need the *GNAT GPL 2011* Ada compiler and the
*AUnit* Ada testing framework.

Both can be freely downloaded from the [Libre](http://libre.adacore.com/libre/)
website.


License
-------

**RogueStars** will be released under the [GNU General Public License, version
3](http://www.gnu.org/licenses/gpl.html).


Credits
-------

Currently, **RogueStars**' only author is Juanma Barranquero
<<lekktu@gmail.com>>.

Ideas, but no code, are stolen from the aforementioned games. Specifically:

* From *NetHack*, the value of deepness and replayability; and of course also
  the humor.
* From *Omega*, the belief that there's always room to be original and think
  outside the box.
* From *ADOM*, the knowledge that a well thought out setting goes a long way in
  making a game feel alive.
* From *Stone Soup*, the realization that a good user interface is paramount.
* And, from *Star Trek*, the whole crazy idea that an ASCII spaceship game can
  be fun.
