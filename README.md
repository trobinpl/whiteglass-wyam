# whiteglass-wyam
It's a port of Jekyll whiteglass theme to Wyam world

Original theme can be found [in its Github repository](https://github.com/yous/whiteglass)

## Configuration
whiteglass-wyam defines couple configuration options. Add them to your `config.wyam` and set desired values.

### Compile CSS
As for now you have to manually add pipeline responsible for generating CSS files from Sass. Add those lines to `config.wyam` file.

    Pipelines.Add("WhiteglassSass",
        ReadFiles("assets/sass/main.scss"),
        Sass().WithCompactOutputStyle(),
        WriteFiles((opt, ctx) => "assets/css/style.css").UseWriteMetadata(false)
    );

### `Settings["ExcerptSeparator"] = "<!--more-->";`
Right now this setting is used only to determine if there should be a "Read more" button. `<!--more-->` is a default post separator for Wyam and as for now, changing this setting will NOT change post separator used during site generation

### `Settings["BlogAuthor"] = "Firstname Lastname";`
This value is displayed in the footer of every page
