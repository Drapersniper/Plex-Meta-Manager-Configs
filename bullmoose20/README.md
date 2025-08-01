# bullmoose20 Kometa files
## Basics
I run Quickstart (https://github.com/Kometa-Team/Quickstart) from my local machine (Windows). I don't use the Quickstart Docker or Quickstart single file releases because the local python install on Windows/Linux/Mac has the most features. The local install could be on a Windows/Linux/Mac VM if you wanted. I run Plex(hotio image) on Unraid 7.1.4.

In addition to creating a config file through a Web UI, Quickstart allows us to create test libraries that you can then have Plex access to test things out in terms of Kometa. Using Quickstart, it can also setup Kometa to run right next to Quickstart. Kometa can then be run from the Quickstart app with different run commands and arguments and all within the app itself. This way you can add and remove options from within Quickstart and run it against the test libraries until you are satisfied with the results.

> [!CAUTION]
> **I strongly recommend running Quickstart instead of my config here because this "Kitchen-Sink" config will likely be problematic for you as it is considered advanced and overkill for 99.9% of people!**
>
> https://github.com/Kometa-Team/Quickstart
>

## Instructions

> [!CAUTION]
> **Did you use [Quickstart](https://github.com/Kometa-Team/Quickstart)? If so, skip to the Posterizarr section. The only thing in my config that Quickstart won't do is the ratings overlays and the custom fonts associated to those ratings overlays**
>

Take what you need from my config.yml. I run everything stock from the github default Kometa and tweak from within my config.yml to "make it my own". If you perform a straight copy, search for `(redacted)` as you will need to replace that with your own information. Search for `db_cache` which is for Plex and now available to set via Kometa. I use 2048 MB (2GB) as my system has 168 GB of RAM. You will want to improve it from the default 40 MB that Plex sets.
> [!TIP]
> **The above is handled for you in [Quickstart](https://github.com/Kometa-Team/Quickstart).**

> [!NOTE]
> If you want to set the language file to something other than fr (french) do not forget to make that change to `language: fr` lines in the config.yml file before running. As for the `placeholder_imdb_id:` ensure that you read and understand those lines as you may need to choose your own **Movie** or **TV Show** as your library may not have the two references that I have.

> [!TIP]
> **The above is handled for you in [Quickstart](https://github.com/Kometa-Team/Quickstart).**

Nothing is custom other than the fonts which are included in this repo (fonts.zip). These fonts are the best match I could find per ratings site and the ratings overlays. 

Unzip the fonts into `config/metadata/overlays/fonts/` to use this config without modifications.

> [!WARNING]
> You can put the fonts elsewhere, but if you choose to do that, you will need to adjust the ratings section (rating1_font:, rating2_font:, rating3_font:) of the overlays within the config.yml file to point to the location you chose.

> [!CAUTION]
> **Ratings overlays and the associated fonts are currently not a feature of Quickstart. It will be there at some point.**
>

## Assets

> [!IMPORTANT]
> I also prefer to have a copy of the local assets so that if I need to recover to the original posters, they are there. I use Posterizarr.ps1 from FSCorrupt's repo to help with that: https://github.com/fscorrupt/Posterizarr . I also use Kometa's assets in a folder structure as described in the wiki here: https://kometa.wiki/en/nightly/kometa/guides/assets/

> [!TIP]
> **The above regarding the setup of assets is handled for you in [Quickstart](https://github.com/Kometa-Team/Quickstart).**

## Posterizarr

I use Posterizarr to populate the assets folder for Kometa to leverage. For Posterizarr, essentially, I prefer `tmdb` as a source and textless images all around `["xx"]`. Then I apply a gradient of my choice (`bottom-up-fade.png` & `bottom-up-fade-background.png`), and font of my choice (`Comfortaa-Medium.ttf`) which happens to match the Kometa defaults for Collections. The secrets to all of this are found in the `bullmoose20config.json` file found in the posterizarr subdirectory along with the font and the gradient files.

Unraid Docker-Compose file is also shared and when prompted in Unraid to add a UI Label Icon, use this link: https://raw.githubusercontent.com/fscorrupt/Posterizarr/main/images/webhook.png

After Posterizarr applies my settings Movie example:

![](./posterizarr/images/movie_example_posterizarr.png)

After Kometa applies overlays to Movie example:

![](./posterizarr/images/movie_example_posterizarr_kometa.png)

After Posterizarr applies my settings Show example:

![](./posterizarr/images/shows_example_posterizarr.png)

After Kometa applies overlays to Show example:

![](./posterizarr/images/shows_example_posterizarr_kometa1.png)
![](./posterizarr/images/shows_example_posterizarr_kometa2.png)
![](./posterizarr/images/shows_example_posterizarr_kometa3.png)

<br>

Feel free to ask me questions in the Kometa Discord channel.

<br>
