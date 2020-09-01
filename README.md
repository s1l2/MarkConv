# MarkConv (Markdown Converter)

Converts markdown of different types to each other.

Platform: NET Core 3.1 (Crossplatform).

## Using

The following command:

```
dotnet MarkConv.Cli.dll -f "my_awesome_article.md" -o Habr
```

Creates the output file `my_awesome_article-Common-Habr.md`.

All cli parameters are optional except of `-f`.

### `-f`

File to convert.

### `-i` or `-o`

Supported values:

* Default
* Common
* Habr

### `-l` or `--linesLength`

Max length of line. `0` - not change, `-1` - merge lines

### `-m` or `imagesMap`

source -> replacement map for image paths. Example of such file:

```
ANTLR.png https://habrastorage.org/files/3ce/bab/ae6/3cebabae6be0455587bc3a379dc7a4f9.png
GitHub.png https://habrastorage.org/webt/v3/gk/id/v3gkidocqqefcthmlywi_c5bjww.png
```

If not defined the file with name `ImagesMap` in the directory of input file will be chosen.

### `--headerimagelink`

Specify link to atricle that can be used for header image link.

### `--removetitleheader`

Removes title header.

### `--tableofcontents`

Generates TOC that based on headers and inserts it at the beginning of output article.

## Build Status

| Windows & Linux Build Status |
|---|
| [![Build status](https://ci.appveyor.com/api/projects/status/jc9rqhgf7k8h5ajc?svg=true)](https://ci.appveyor.com/project/KvanTTT/markconv) |