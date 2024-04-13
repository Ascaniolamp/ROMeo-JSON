# ROMeo default JSONs

## Configuration file (`config.json`)
The configuration file must be called `config.json` and placed in the same directory as the index.html file, it contains multiple optional and essential configuration parameters:

### Essential parameters
- `defaultConsole` : string - The `consoles` key string value of the first console the page will load.
- `consoles` : {key : string} - Keys are the console' names and their values are the paths to their respective JSON file.

### Optional parameters
The default values are used in case the parameters haven't been set.

- `styleLogos` : boolean (default : `true`) - If set to `false` the download buttons won't show the website's logo.
- `maxItems` : number (default : `0`) - The maximum number of items to display in a single page. If set to a number smaller than one, all the items will be shown in a single page.
- `sitesLogos` : {key : string} = Keys are the website's domain name (ex. `"vimm.net"`), values are paths to their respective logo file.
- `logoThemes` : {key : string} = Keys are logo file paths, values are their themes (`"dark"` or `"light"`).

## Console files
Console files paths **MUST** be referenced in the `config.json` file to work, they can be placed anywhere as long as they're in the configuration file's `consoles` object.
Every console file is actually an array of ROM items, which are objects that contain the following parameters:
- `title` : The ROM's title
- `link` : A URL to the ROM's download page (or to the file itself)
- `altLinks` : An array of alternative download links
- `description` : The ROM's description
- `release` : The ROM's date of release

Every ROM with a missing `title` or `link` parameter will be marked by a yellow border.
If it's missing both parameters, the border will be red instead.

## Logos
The repo's `res` folder contains the logo files which are linked inside the configuration file.
