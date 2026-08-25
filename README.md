# uxn-playground

A couple of small [Varvara](https://wiki.xxiivv.com/site/varvara.html) programs written in [uxntal](https://wiki.xxiivv.com/site/uxntal.html):

- **[flappy.tal](flappy.tal)** — a small side-scrolling "running dino" style game. Based on [keijiro/uxn-sketches/flappy.tal](https://github.com/keijiro/uxn-sketches/blob/main/flappy.tal).
- **[guardian.tal](guardian.tal)** — an intro splash + clickable news headline viewer (a work-in-progress text viewer).

Both are assembled and run with the [uxn2](https://git.sr.ht/~rabbits/uxn2) emulator, which also ships the `drifblim.rom` assembler.

## Requirements

- The [uxn2](https://git.sr.ht/~rabbits/uxn2) emulator and its `drifblim.rom` assembler. See the [installation instructions](https://git.sr.ht/~rabbits/uxn2#building) for building from source (you'll need [SDL2](https://www.libsdl.org/)) or grabbing a prebuilt binary.
- The commands below assume `uxn2` is on your `PATH` and `drifblim.rom` is in the current directory. Adjust the paths to match wherever you installed them.

## Running

Each program is assembled from its `.tal` source into a `.rom`, then run with the emulator.

The assembler is itself a rom, so assembling looks like:

```sh
uxn2 drifblim.rom <source>.tal <output>.rom
```

### flappy.tal

```sh
# assemble
uxn2 drifblim.rom flappy.tal flappy.rom
# run
uxn2 flappy.rom
```

Controls: press the **up** key (controller button) to flap/jump. Crashing restarts the game.

### guardian.tal

```sh
# assemble
uxn2 drifblim.rom guardian.tal guardian.rom
# run
uxn2 guardian.rom
```

Controls: move the **mouse** over a headline to highlight it in grey.

## Screenshots

### flappy.tal

<img width="511" height="350" alt="flappy" src="https://github.com/user-attachments/assets/fb119b76-b03c-4354-a51e-3825570f79bc" />

<!-- Add a screenshot below, e.g. ![flappy](docs/flappy.png) -->

### guardian.tal
<img width="514" height="303" alt="Screenshot 2026-08-24 at 16 52 49" src="https://github.com/user-attachments/assets/63dd65a6-8635-455b-9205-f4fdeb51b707" />
<!-- Add a screenshot below, e.g. ![guardian](docs/guardian.png) -->
