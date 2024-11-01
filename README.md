# ToME: the Tales of Maj'Eyal ported to ARM64

It's based on the source code of ToME4 v1.7.6 from te4.org.
I've just ported it to android, however the lua related part is broken,
so you have to manually edit the `build/TEngine.make` to force it to link
to `/lib/libluajit-5.1.so` instead of liblua.a after running `premake4 gmake` (I didn't found a way to do it automatically).

However, it won't start: a Window will be started, but nothing appeared on the screen... It seems that it stucked on the lua init...... , but that's out of my ability(I just know nothing about lua...)

P.S. I've just splited two large files to avoid LFS, run
```
cat game/modules/tome-1.7.6-gfx.team-* > game/modules/tome-1.7.6-gfx.team
cat game/modules/tome-1.7.6-music.team-* > game/modules/tome-1.7.6-music.team
```
Welcome for anyone's help! :-D
