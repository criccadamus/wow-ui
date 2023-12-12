# New fonts to `ElvUI`

## Adding the font files

* Localize the folder `\World of Warcraft\_retail_\Interface\AddOns\ElvUI\Core\Media\Fonts` and add the font files to it.  

    > Sans-serif font suggestions: [San Francisco Bold](sanfrancisco-bold.ttf), [San Francisco Regular](sanfrancisco-regular.otf), [San Francisco Rounded](sanfrancisco-rounded.ttf)

## Edits

* Edit the file `SharedMedia.lua` in the directory `\World of Warcraft\_retail_\Interface\AddOns\ElvUI\Core\Media` adding extra lines for every new font following this format:  

    > `AddMedia('font','<fontfile-name>.<fontfile-format>', '<Descriptive Name>', nil, westAndRU)`

    after the default programmatic `AddMedia` font lines.  
    Notes:

  * Include the `westAndRU` flag if the font supports cyrillic characters.  
  * Keep the `nil` tag if the font does not need a `Mask`.

    * Example:

    ```lua
    AddMedia('font','sanfrancisco-bold.ttf',			'San Francisco Bold', nil, westAndRU)
    AddMedia('font','sanfrancisco-regular.otf',			'San Francisco Regular', nil, westAndRU)
    AddMedia('font','sanfrancisco-rounded.ttf',			'San Francisco Rounded', nil, westAndRU)
    ```

## Restart the game

> Every time this addon updates will break this edit; make a backup somewhere and readd the fonts and the lines after updating `ElvUI`.
