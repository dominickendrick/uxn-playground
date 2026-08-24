# uxn-playground

A couple of small [Varvara](https://wiki.xxiivv.com/site/varvara.html) programs written in [uxntal](https://wiki.xxiivv.com/site/uxntal.html):

- **[flappy.tal](flappy.tal)** — a small side-scrolling "running dino" style game.
- **[guardian.tal](guardian.tal)** — an intro splash + clickable news headline viewer (a work-in-progress text viewer).

Both are assembled and run with the emulator and assembler bundled in [uxn2/](uxn2/).

## Requirements

- The prebuilt `uxn2` emulator and `drifblim.rom` assembler are included in [uxn2/bin/](uxn2/bin/).
- If you need to rebuild the emulator, you'll need [SDL2](https://www.libsdl.org/) — see [uxn2/README.md](uxn2/README.md).

## Running

Each program is assembled from its `.tal` source into a `.rom`, then run with the emulator.

The assembler is itself a rom, so assembling looks like:

```sh
uxn2/bin/uxn2 uxn2/bin/drifblim.rom <source>.tal <output>.rom
```

### flappy.tal

```sh
# assemble
uxn2/bin/uxn2 uxn2/bin/drifblim.rom flappy.tal flappy.rom
# run
uxn2/bin/uxn2 flappy.rom
```

Controls: press the **up** key (controller button) to flap/jump. Crashing restarts the game.

### guardian.tal

```sh
# assemble
uxn2/bin/uxn2 uxn2/bin/drifblim.rom guardian.tal guardian.rom
# run
uxn2/bin/uxn2 guardian.rom
```

Controls: move the **mouse** over a headline to highlight it in grey.

## Screenshots

### flappy.tal

<!-- Add a screenshot below, e.g. ![flappy](docs/flappy.png) -->

### guardian.tal

<!-- Add a screenshot below, e.g. ![guardian](docs/guardian.png) -->
