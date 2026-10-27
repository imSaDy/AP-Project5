# Plants vs. Zombies in C++

A version of Plants vs. Zombies written in C++ with SFML for the Advanced Programming course at the University of Tehran, Spring 2024. I built it with [Fatemeh Boloukazari](https://github.com/FatemehBoloukazari).

The game has five plants (peashooter, snow pea, melon-pult, sunflower and walnut) and two kinds of zombies, which arrive in waves with a final large wave. Players collect sun to buy plants, and each plant has a cooldown before it can be placed again. The code is organized around a small class hierarchy: plants and zombies share a `GameObject` base, and the three projectile types derive from `Bullet`. `System` runs the menus and the main loop, and `Handler` updates the plants, zombies, suns and projectiles on the board.

Plant and zombie stats (health, damage, speed, cost, cooldown and so on) and the timing of the zombie waves are read from `setting.txt`, so the game can be rebalanced without recompiling.

## Building

Requires g++ with C++20 support and SFML 2 (graphics, window, system and audio).

```sh
make
./pvz.out
```

Images, sounds and fonts are in `files/`.
