## Caravan SandWitch Switch Optimization

This repo contains a mod, which will stabilize performance of the game Caravan Sand Witch on Switch, and also improve shadows quality.
The effect was achieved by improving ini files.

### Requirements

Unfortunately, this game is not optimized very well, so default Switch hardware cannot run it with stable fps. Simple ini tweaks are not enough here.

So I have made this mod with overclocked Switch in mind, and it's a requirement.

I'm running my CPU at 1683 MHz, and GPU at 768 MHz.

### Changes

- FPS locked to 30
- Stuttering improvements
- Garbage collection improvements
- Further shadow distance
- Reduced dynamic resolution
- FXAA anti aliasing

### Stutters

Due to broken implementation of garbage collection in this game the stutters are impossible to eliminate. Every time gc will analyze current memory the fps will hitch. But I was able to change time period of analysis from60 seconds to 120 seconds, so you should see these hitches less often.

### Installation

Put the `.pak` file into `atmosphere\contents\0100d5801e904000\romfs\CaravanSandWitch\Content\Paks` on your sd card.

### Packing

To pack source into a `.pak` you need [Repak](https://github.com/trumank/repak).

Pack the mod with command `repak.exe pack -v ZZ-pakchunk0-Switch_P` inside this repo.