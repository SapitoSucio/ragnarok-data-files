## Lite Graphics Plugin (LGP)
With the introduction of our 2018 client, we have enabled the @lgp (and other) command. LGP is short for Lite Graphics Plugin, which we hope will seriously improve not only your PvP gameplay but also your PvM gameplay.

## What is the Lite Graphics Plugin (LGP)?
LGP is a plugin that was developed by the same person who provides us with Gepard Shield. It's partially based on the RCX Tool that was often used in the past to improve gameplay.

It serves several purposes. First off, LGP allows you to play with effects disabled and still see where skills are cast. Particularly in crowded situations like War of Emperium, this can seriously reduce the strain on not just your eyes but also your computer in general. Furthermore, it allows you to see the exact cells on which a specific skill has been cast.

## How to use LGP?
The plugin comes with several other commands which all serve their own purposes. For starters, these commands only work like an @command, not like an !command. Keep that in mind. Let's go through them one by one:

| Command | Description |
| ------- | ----------- |
| **@lgp** | Toggles the Lite Graphics Plugin.|
| **@aoes** | Toggles colored cells to indicate the range of an AoE skill. This allows you to specifically see the cells that an AoE skill affects. |
| **@circle** | Toggles a colored circle around your character to determine maximum casting range. |
| **@shake** | Toggles shaking for skills such as Critical Explosion. Does the same as /quake command basically. |
| **@square** `<on/off/1-14>` | Shows a colored square around your character to determine cell amounts. You could use this to remind yourself of your melee range for instance. |

## Customizing LGP
To change the colors to something that suits your style you would open the "plugin.ini" and modify the codes to the colors you would like to see on certain skills.

**Let's look at the following example:**
```
; MG_SAFETYWALL#Safety_Wall
Skill007E=0x7F000000
; WZ_FIREPILLAR#Fire_Pillar
Skill0087=0x7FFC8E0C
```

Defining the cell color is always started by `0x`, followed by **two digits** for the alpha-transparency(Opacity) and **six digits** for the color determination (RRGGBB).
The alpha-transparency ranges from 0% (00) to 100% (FF). In this case, the 7F is about 50% transparency(See the table below).

Following the alpha-transparency is the actual color code. In the case of Safety Wall, it's set to `000000` which is fully black. A full white would be `FFFFFF`. Each two digits will determine how much of Red, Green and Blue is used. As such, a code such as `FF0000` is 100% red with no green and blue. In the above case of Fire Pillar, the `FC8E0C` code refers to a nice orange. To easily find the proper color codes, you could use this website for example.

|  %   | Value |
|------|-------|
| 100% | FF    |
| 95%  | F2    |
| 90%  | E6    |
| 85%  | D9    |
| 80%  | CC    |
| 75%  | BF    |
| 70%  | B3    |
| 65%  | A6    |
| 60%  | 99    |
| 55%  | 8C    |
| 50%  | 80    |
| 45%  | 73    |
| 40%  | 66    |
| 35%  | 59    |
| 30%  | 4D    |
| 25%  | 40    |
| 20%  | 33    |
| 15%  | 26    |
| 10%  | 1A    |
| 5%   | 0D    |
| 0%   | 00    |