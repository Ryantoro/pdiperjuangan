--
# Collection Types #############################################################
################################################################################

# http://yaml.org/type/map.html -----------------------------------------------#

map:
  # Unordered set of key: value pairs.
  Block style: !!map
    Clark : Evans
    Ingy  : döt Net
    Oren  : Ben-Kiki
  Flow style: !!map { Clark: Evans, Ingy: döt Net, Oren: Ben-Kiki }

# http://yaml.org/type/omap.html ----------------------------------------------#

omap:
  # Explicitly typed ordered map (dictionary).
  Bestiary: !!omap
    - aardvark: African pig-like ant eater. Ugly.
    - anteater: South-American ant eater. Two species.
    - anaconda: South-American constrictor snake. Scaly.
    # Etc.
  # Flow style
  Numbers: !!omap [ one: 1, two: 2, three : 3 ]

# http://yaml.org/type/pairs.html ---------------------------------------------#

pairs:
  # Explicitly typed pairs.
  Block tasks: !!pairs
    - meeting: with team.
    - meeting: with boss.
    - break: lunch.
    - meeting: with client.
  Flow tasks: !!pairs [ meeting: with team, meeting: with boss ]
  # http://yaml.org/type/set.html -----------------------------------------------#

set:
  # Explicitly typed set.
  baseball players: !!set
    ? Mark McGwire
    ? Sammy Sosa
    ? Ken Griffey
  # Flow style
  baseball teams: !!set { Boston Red Sox, Detroit Tigers, New York Yankees }

# http://yaml.org/type/seq.html -----------------------------------------------#

seq:
  # Ordered sequence of nodes
  Block style: !!seq
  - Mercury   # Rotates - no light/dark sides.
  - Venus     # Deadliest. Aptly named.
  - Earth     # Mostly dirt.
  - Mars      # Seems empty.
  - Jupiter   # The king.
  - Saturn    # Pretty.
  - Uranus    # Where the sun hardly shines.
  - Neptune   # Boring. No rings.
  - Pluto     # You call this a planet?
  Flow style: !!seq [ Mercury, Venus, Earth, Mars,      # Rocks
                      Jupiter, Saturn, Uranus, Neptune, # Gas
                      Pluto ]                           # Overrated
