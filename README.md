##  this is a fork, bring me the knife.

An [issue on github] and an [announcement on reddit] got posted yesterday. Stating that the lead developers of [i3] will merge [i3-gaps] to the main project. The reason being *the overwhelming demand the fork has*.

This clearly goes against: *(from the official [i3] website)*
  8. The usual elitism amongst minimal window managers: Don’t be bloated, don’t be fancy (**simple borders are the most decoration we want to have**). 

In my opinion it is letting a loud intolerant minority dictating yet another thing in this day and age (we live in a society). I believe this will be the beginning of the end of i3. It also annoys me that these features are getting implemented when there are functionality in i3 that could be improved, added or removed that would benefit the project, the enduser and the developers in a greater way. All discussion that isn't in favor for the change is being muted (you can see that my comment in the issue thread has been deleted)... whatever.

## why fork i3 if it is bad?

i3 is not bad. It is by far the best and most advanced dynamic window manager. But there are some things that really annoys me. I have since a couple of years maintained a repository with bash scripts, called [i3ass] that add or fixes the behavior i would like to have in i3. But there are some things that i3ass doesn't do, and it's 3rd party dirt hack bash scripts, that could be implemented directly into the window manager.  

## why fork i3 if it is not bad?

### Things that are unnecessary that could be **removed** from i3:
- i3bar, there are better standalone statusbar alternatives and there is no reason to include one with the windowmanager.
- internal hotkey daemon, same, a system like bspwm+sxhkd is better
- gaps (not implemented yet), bloat

### Things that are bad, but could be good if **reworked**:
- layout saving/restoring, the current system is confusing to say the least, it is also slow, and creates these strange empty containers and stuff. It could be implemented differently.
- window rules. there is a strange issue with window rules getting re-triggered when i3 is reloaded that needs to get fixed. I also believe that the syntax and system could be re-designed and the layout restoring thing could be replaced with a better window/container-rule system.
- tabs. currently tabbed containers are treated just as any other container, this make switching, creating, moving tabs unnecessary complex. imo, tabs is the best, most useful feature of i3 that other wms lack, and it is a shame it doesn't get more attention.
- ipc. the current ipc API in i3 is fine. but i would like more (a lot more) commands that would return specific information about the session. This is what the scripts [i3list] and [i3get] in [i3ass] does.
- moving and resizing could be done in a different way, see [i3Kohrne].

### Things that could be **added**:  
- run-or-raise-or-hide function. This is included with f.i. awesomewm, and also with [i3run]. the ability to minimize/hide a window/container is great.
- floating-to-tabbed mode. this one is a bit controversial. but imo the most natural "mode" for a window manager is that all new "unknown" windows (without rules) should be spawned floating. With the ability to make them tiled in a tabbed container. and from this tabbed state the window can be moved around in a tiled grid. this is almost impossible to do in a sane way in current i3 due to the strange design of tabs. the [i3ass] version of this is [i3fyra].
- session persistent variables, that could be altered and retrieved both in the config file and IPC.

## cool, how do i get this bwm?

well.. I just have to modify the old i3 source. I guess i need to learn C, setting up a testing environment, figure out how things work first. So it will probably be ready in a year or two or never.

## sounds like you need help

maybe in the future, but right now i think i want to get a grasp of the whole thing and do some stupid experiments on my own.

#### budRich - 2019-06-18

[i3get]: https://github.com/budlabs/i3ass/wiki/12AS_i3get
[i3fyra]: https://github.com/budlabs/i3ass/wiki/11AS_i3fyra
[i3Kornhe]: https://github.com/budlabs/i3ass/wiki/14AS_i3Kornhe
[i3list]: https://github.com/budlabs/i3ass/wiki/15AS_i3list
[i3run]: https://github.com/budlabs/i3ass/wiki/17AS_i3run
[i3ass]: https://github.com/budlabs/i3ass
[i3]: https://i3wm.org/
[i3-gaps]: https://github.com/Airblader/i3
[issue on github]: https://github.com/i3/i3/issues/3724
[announcement on reddit]: https://old.reddit.com/r/i3wm/comments/c1r58x/we_may_finally_bring_gaps_into_i3/
