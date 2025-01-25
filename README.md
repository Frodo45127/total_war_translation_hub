# Total War Translation Hub
The Total War Translation Hub, the one place to find translations for mods for Total War Games since Empire.

Please note that these translations are community-generated. Don't come asking for translations for specific mods here.

For more info about what mods are translated and their current status, check the [STATUS.md](https://github.com/Frodo45127/total_war_translation_hub/blob/master/STATUS.md) file. 

If you want to contribute fixes for vanilla localisation bugs (yes, this repo also supports fixes for vanilla loc bugs), just export the Loc file with the fixed loc entries, call it "vanilla_fixes_XX.tsv" where XX is the language code the fixes are for (EN for English, SP for Spanish,...) and put it in the game folder, the same place where the vanilla_english.tsv file is. 

# How does this work?

This repo contains translations for mods in a kinda standarized format, so they can be easily used by tools to, for example, automatically translate the mods you download. To explain it more in detail:

- These translations are created with RPFM's translator tool. Said tool can be used to translate a mod, either manually or by importing a translation already done in another pack, and to analyze mod updates and find exactly what loc entries need translation, either because they're new in the mod update, or because the mod's original text for them changed.
- Once you "finish" a translation, it'll create a translated loc file in your Pack (so you can test the translation directly), and a translation file in "rpfm's config folder/translations_local/game_key/pack_name/LANGUAGE.json". RPFM uses that json file to store the translation in a way that can be shared. Those json files are what this repo contains. If you made a translation with RPFM, feel free to contribute those files to this repo. Why?
- If a user uses Runcher and enables the launch option "Enable Translations", Runcher will automatically download this repo, detect what translations can be applied to the user's load order, and automatically apply them without altering the mods themselfs. Not only that, but if the translation is outdated, it'll also detect what lines are not valid anymore because the original mod changed them, and not use them. This means that, unlike with "translated mod packs", you don't need to worry about the game having mistranslated lines because the translation is not up-to-date. 

And while this is primarly used by RPFM and Runcher, the translation format can be easily read by any other tool, should another dev want to support them on their own tool.

# TL;DR

If you use Runcher, whatever mod that has a translation here will be automatically trasnlated for you, without any mistranslated line due to the translation being updated. Like magic.

If you're a modder or a translator, you can generate a translation json with RPFM, upload it here either through an issue or a pull request, and it'll automatically be available for anyone using Runcher with the "Enable Translations" option toggled on. Like magic.

# But why?
Because I like my games in spanish, and if I managed to get two different 800 mod stable load orders running in Skyrim almost entirely in spanish, I can also do it with Total War.
