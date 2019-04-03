# Instructions for adding LiteLoader to Impact

## Download the LiteLoader installer

You can find the downloads for LiteLoader [here](https://www.liteloader.com/download)

## Run the LiteLoader installer

Run the LiteLoader installer and create a new profile, extending Impact's

![Installer](https://i.imgur.com/8NnyH1a.png)

## Modify the JSON (for Impact versions before 4.4)

<details>
  
  <summary><strong>Do this if using 4.3 or older</strong></summary>

Find the new Impact+LiteLoader combo JSON that the installer created, and modify the last argument to read as follows:

![Modify](https://i.imgur.com/6AFFegt.png)

</details>

## Modify the JSON (Applies to all versions)

You will need to modify the LiteLoader jar and the JSON itself to remove the outdated Mixin dependency from LiteLoader.

<details><summary><strong>Instructions</strong></summary>

### 1) Delete the Mixin version from the LiteLoader jar

Delete the "org" folder in the root directory of the LiteLoader jar, it should only contain Mixin so this will be fine. Mine is already deleted.

![image](https://user-images.githubusercontent.com/24485393/52526197-e4eed380-2c7a-11e9-99fb-87880ad29887.png)

### 2) Remove the URL from the LiteLoader JSON
> Psst! If your game wont launch, leave the url field there, but replace it with `"https://www.google.com"`

This will prevent the LiteLoader jar from being "fixed" and having the Mixin version restored. Below is what it should look like once removed.

![image](https://user-images.githubusercontent.com/24485393/52526233-34cd9a80-2c7b-11e9-9255-e770420ed389.png)


</details>

## Run the new Profile

Now you can open the Minecraft launcher and run the combo profile as normal.

![Run](https://i.imgur.com/J5wWJt9.png)

## YouTube Tutorial 
https://www.youtube.com/watch?v=0B0dt_ItWpY
