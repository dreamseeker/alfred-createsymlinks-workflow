# CreateSymlinks for Alfred 2

A workflow of Alfred 2 that create symbolic links from JSON format file.

## Requirements

- Alfred 2 + Powerpack
- PHP 5（OSX 10.6 or later, it comes bundled）

## Installation

After download. Double-click the [CreateSymlinks.alfredworkflow](https://raw.github.com/dreamseeker/alfred-createsymlinks-workflow/master/CreateSymlinks.alfredworkflow),  add to Alfred.

## Usage

`symlink [filepath]`

Choose either `CreateSymlinks` or `ForceCreateSymlinks`.  
`ForceCreateSymlinks` is forced to overwrite the existing symbolic links.

Tips : When file path begins with `~/` strings, auto-replace absolute path.

![ScreenShot](https://raw.github.com/dreamseeker/alfred-createsymlinks-workflow/master/screenshot.png)

When selected the file extension `.json`, you can use the Actions panel.

![ScreenShot2](https://raw.github.com/dreamseeker/alfred-createsymlinks-workflow/master/screenshot2.png)

## JSON Sample

<table>
  <tr>
    <th>Key</th>
    <th>Type</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>source</td>
    <td>Array</td>
    <td>set either as a file/directory.</td>
  </tr>
  <tr>
    <td>dist</td>
    <td>Array</td>
    <td>distribute to these directory path. if these doesn't exists, make directory.</td>
  </tr>
</table>

The following code is generate symbolic links of `~/node_modules` and `~/package.json` to `~/MyProject`.

```json
[
  {
    "source": [
      "~/node_modules",
      "~/package.json"
    ],
    "dist": [
      "~/MyProject"
    ]
  }
]
```

Please try to reference the [sample.json](https://raw.github.com/dreamseeker/alfred-createsymlinks-workflow/master/sample.json).

## License and Authors

Authors: TORU KOKUBUN
