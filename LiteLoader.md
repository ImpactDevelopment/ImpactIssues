# Instructions for adding LiteLoader to Impact

## Download the LiteLoader installer

You can find the downloads for LiteLoader [here](https://www.liteloader.com/download)

## Run the LiteLoader installer

Run the LiteLoader installer and create a new profile, extending Impact's

![Installer](https://i.imgur.com/8NnyH1a.png)

## Modify the JSON (for Impact versions before 4.4)

<details>
  
  <summary><strong>As of 4.4, you can keep this part the same!</strong></summary>

Find the new Impact+LiteLoader combo JSON that the installer created, and modify the last argument to read as follows:

![Modify](https://i.imgur.com/6AFFegt.png)

</details>

## Modify the JSON (Applies to all versions)

You will need to modify the LiteLoader jar and the JSON itself to remove the outdated Mixin dependency from LiteLoader. The steps are [Here](https://github.com/ImpactDevelopment/ImpactClient/issues/917#issuecomment-462078924).

## Run the new Profile

Now you can open the Minecraft launcher and run the combo profile as normal.

![Run](https://i.imgur.com/J5wWJt9.png)

## YouTube Tutorial 
https://www.youtube.com/watch?v=0B0dt_ItWpY
