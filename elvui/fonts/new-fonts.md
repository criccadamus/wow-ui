# Add new fonts to `ElvUI`

## Adding the font files

* Locate in your World of Warcraft addons folder the `ElvUI` one: `\World of Warcraft\_retail_\Interface\AddOns\ElvUI\Core\Media\Fonts` and add any font files to it.  

    > Sans-serif font suggestions: [San Francisco Bold](sanfrancisco-bold.ttf), [San Francisco Regular](sanfrancisco-regular.otf), [San Francisco Rounded](sanfrancisco-rounded.ttf)

## File edits

1. Edit the file `SharedMedia.lua` in the directory `\ElvUI\Core\Media`.  

   * Every new font requires an new line that has to follow this structure:  

      `AddMedia('font','<fontfile-name>.<fontfile-format>', '<Descriptive Name>', nil, westAndRU)`

      * Where the `<fontfile-name>` is the name of the font file,
      * `<fontfile-format>` is the format of the font file (like TrueType, OpenType...),
      * `<Descriptive Name>` is the name the font will have inside the `ElvUI` dropdown select menus.

    After the default `AddMedia` lines.  
    Notes:

     * Include the `westAndRU` flag if the font supports cyrillic characters.  

     * Keep the `nil` tag if the font does not need a `Mask`.

    Example:

    ```lua
    AddMedia('font','sanfrancisco-bold.ttf',			'San Francisco Bold', nil, westAndRU)
    AddMedia('font','sanfrancisco-regular.otf',			'San Francisco Regular', nil, westAndRU)
    AddMedia('font','sanfrancisco-rounded.ttf',			'San Francisco Rounded', nil, westAndRU)
    ```

## Save the file and restart the game

## Notes

* Every time you update `ElvUI` you will have to do this again as the file you just edited has been replaced.  
