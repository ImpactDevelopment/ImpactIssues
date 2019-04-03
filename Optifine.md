# Instruction for adding OptiFine into Impact

If you prefer watching a video tutorial watch [this](https://www.youtube.com/watch?v=o1LHq6L0ibk)

## Download optifine here

You can find it [here](optifine.net)

## Run the optifine installer

You will need Java on your system to do so

## Navigate to your .minecraft folder

- If you don't know where it probably is in `%appdata%/.minecraft` (for Windows)
- Press <kbd>Win+r</kbd> and paste, or paste it in Windows Explore and hit <kbd>enter</kbd>

## Copying the OptiFine file

- Navigate into `/versions`
- You will find the OptiFine and Impact folders here
- First navigate into the folder of OptiFine that you want to install

You will see

```
    {
      "name": "optifine:OptiFine:1.12.2_HD_U_E2" //can be anything else depending on your version
    },
```

- Copy that from YOUR optifine.json FILE

## Editing Impact.json

- Now go back to the `versions` and navigate to the folder and find the `.json` inside you wanted to install for
- You will need to add paste what you copied here

```
  "libraries": [
    {
      "name": "optifine:OptiFine:1.12.2_HD_U_E2"
    },
    { ...
```

_like this_

### Adding OptiFine's tweaker

<details><summary><strong>Versions between 4.0 and 4.5 (and 4.6 1.12.2) </strong></summary>

- Go to

```
"minecraftArguments": "--username ${auth_player_name} --version ${version_name} --gameDir ${game_directory} --assetsDir ${assets_root} --assetIndex ${assets_index_name} --uuid ${auth_uuid} --accessToken ${auth_access_token} --userType ${user_type} --tweakClass clientapi.load.ClientTweaker",
```

and add in `--tweakClass optifine.OptiFineForgeTweaker` to the end of the argument/line
_like this_

```
  "minecraftArguments": "--username ${auth_player_name} --version ${version_name} --gameDir ${game_directory} --assetsDir ${assets_root} --assetIndex ${assets_index_name} --uuid ${auth_uuid} --accessToken ${auth_access_token} --userType ${user_type} --tweakClass clientapi.load.ClientTweaker --tweakClass optifine.OptiFineForgeTweaker",
```

</details>

<details><summary><strong>Versions from 4.6 (1.13.2) and up</strong></summary>

Find the `"arguments": { "game": [] }` section, it'll look like this:

```json
"arguments": {
  "game": [
    "--tweakClass",
    "clientapi.load.ClientTweaker",
    "--tweakClass",
    "baritone.launch.BaritoneTweaker"
  ]
},
```

Add `"--tweakClass"` and `"optifine.OptiFineForgeTweaker"` to the `game` array so that it looks like:

```json
"arguments": {
  "game": [
    "--tweakClass",
    "clientapi.load.ClientTweaker",
    "--tweakClass",
    "baritone.launch.BaritoneTweaker",
    "--tweakClass",
    "optifine.OptiFineForgeTweaker"
  ]
},
```

</details>

When it's completed just restart your launcher and you should have OptiFine

## [Advanced] Have multiple profiles consist of one having OptiFine and the other without

Before the editing impact.json step, you should make a copy of Impact's folder
make sure to remember & copy what the folder was named
and also rename the impact.json to whatever the folder was named

After done editing impact.json you will want to edit

```
  "id": "1.12.2-Impact_4.3",
```

to whatever the folder was named
example of mine is

```
"id": "1.12.2-Impact_4.3-Optifine",
```

Now restart your launcher and you will find a new profile named whatever the folder was named if you did it correctly
