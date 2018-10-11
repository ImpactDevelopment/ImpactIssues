# Instruction for adding optifine into impact
If you prefer watching a vidoe please watch [this](https://www.youtube.com/watch?v=o1LHq6L0ibk)
## Download optifine here
You can find it [here](optifine.net)

## Run the optifine installer
you will need java on your system to do so

## Navigate to your .minecraft folder
if you dont know where it probably is in `%appdata%/.minecraft` (for windows)
press win+r and paste that or paste it in window explore and hit enter

## Copying the optifine file
navigate into /versions
you will find the optifine and impact jsons here
first navigate into the folder of optifine that you want to install

You will see
```
    {
      "name": "optifine:OptiFine:1.12.2_HD_U_E2" //can be anything else depending on your version
    },
```
copy that from YOUR optifine.json FILE

## Editing impact.json
now go up one directory and navigate to impact.json you wanted to install for
You will need to add paste what you copied here
```
  "libraries": [
    {
      "name": "optifine:OptiFine:1.12.2_HD_U_E2"
    },
    { ...
```
like this

now go to
```
"minecraftArguments": "--username ${auth_player_name} --version ${version_name} --gameDir ${game_directory} --assetsDir ${assets_root} --assetIndex ${assets_index_name} --uuid ${auth_uuid} --accessToken ${auth_access_token} --userType ${user_type} --tweakClass clientapi.load.ClientTweaker",
```
and add in `--tweakClass optifine.OptiFineForgeTweaker`
like this
```
  "minecraftArguments": "--username ${auth_player_name} --version ${version_name} --gameDir ${game_directory} --assetsDir ${assets_root} --assetIndex ${assets_index_name} --uuid ${auth_uuid} --accessToken ${auth_access_token} --userType ${user_type} --tweakClass clientapi.load.ClientTweaker --tweakClass optifine.OptiFineForgeTweaker",
```
when it's completed it should be done

## [Advanced] have multiple profiles consist of one having optifine and the other dont
Before the editing impact.json step, you should make a copy of impact's folder
make sure to remember+copy what the folder was named
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
now restart your launcher and you will find a new profile named whatever the folder was named if you did it correctly
