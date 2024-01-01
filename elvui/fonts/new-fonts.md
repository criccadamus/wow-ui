# Add new fonts to `ElvUI`

## Adding the font files

* Locate in your World of Warcraft addons folder the `ElvUI` one: `\World of Warcraft\_retail_\Interface\AddOns\ElvUI\Core\Media\Fonts` and add any font files to it.  

## Procedure

1. Edit the file `SharedMedia.lua` in the directory `\ElvUI\Core\Media`.  

   * Every new font requires an new line after the default `AddMedia` lines that has to follow this structure:  

      `AddMedia('font','<fontfile-name>.<fontfile-format>', '<Descriptive Name>', nil, westAndRU)`

      * Where the `<fontfile-name>` is the name of the font file added to the `Fonts` folder,
      * `<fontfile-format>` is the format of the font file (like TrueType, OpenType...),
      * `<Descriptive Name>` is the name the font will have inside the `ElvUI` dropdown and any `SharedMedia` compatible addons select menus.

    Notes:

     * Include the `westAndRU` flag if the font supports cyrillic characters.  

     * Keep the `nil` tag if the font does not need a `Mask`.

    Example:

    ```lua
    AddMedia('font','sanfrancisco-bold.ttf',			'San Francisco Bold', nil, westAndRU)
    AddMedia('font','sanfrancisco-regular.otf',			'San Francisco Regular', nil, westAndRU)
    AddMedia('font','sanfrancisco-rounded.ttf',			'San Francisco Rounded', nil, westAndRU)
    ```

2. Save the file. For the changes to appear, restart the game if running.  

## Notes and recommendations

* Every time you update `ElvUI` you will have to do this again as the file you just edited has been replaced.  
* Try to use serif fonts (*suggested: the default Fritz Quadrata TT and [CMU Serif](cmu-serif.ttf)*) for numbers and sans-serif fonts (*suggested: [San Francisco Bold](sanfrancisco-bold.ttf), [San Francisco Regular](sanfrancisco-regular.otf), [San Francisco Rounded](sanfrancisco-rounded.ttf)*)
 for text.  
