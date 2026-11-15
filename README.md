# LIB_BVH

The BVH motion library for the games: motion-capture clips that LIB_MOCAP turns into stick
clips (Vibecode3D) and skinned bodies (xt3D). Moved out of `LIB_MOCAP/input/BVH` on
2026-11-12 so games and tools share one library and LIB_MOCAP keeps only its pipeline.

| Folder | What |
|---|---|
| `Animazoo/` | 41 clips (see `about_animazoo_bvh.txt`) |
| `FreeBVH/` | Truebones FreeBVH collection |
| `iGame3D/` | iGame3D's own animations, converted to BVH by `LIB_MOCAP/tools/wif.py` |
| `iGame3D_DeadDays/` | 58 animations from the owner's 2008 DeadDays models (officer, human, zombietobi, robothead, robotheadgun), each on its own 13- or 14-bone rig; made by `LIB_MOCAP/tools/wtf_anim.py` (A-85). The owner's own work; rotation order not yet seen on screen |
| `iGame3D_2008/` | the 2008 iGame3D BVH scripts and dialogs (parsers, builder, BVH browser, BVH→WIF) |

**Rights:** the Animazoo and Truebones clips are third-party and their licences are not
settled yet. Local use only: this repository has no remote and must not be published
until that is cleared.

Use: `cd ../LIB_MOCAP && python3 -I tools/mocap_lib.py process <Folder>_<file>` (clip names are
`<folder>_<file name>`, e.g. `Animazoo_gangster_walk`); `mocap_lib.py` reads this folder,
`../LIB_LLMIN/LIB_MOCAP` (new captures) and `LIB_MOCAP/input`.
