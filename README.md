<h1 align="center">
  <br>
    <img src="https://raw.githubusercontent.com/PKief/vscode-starlane-icon-theme/main/logo.png" alt="logo" width="200">
  <br><br>
  Starlane Icon Theme
  <br>
  <br>
</h1>

<h4 align="center">Get the Material Design icons into your VS Code.</h4>

<p align="center">
    <a href="https://marketplace.visualstudio.com/items?itemName=PKief.starlane-icon-theme"><img src="https://vsmarketplacebadge.apphb.com/version-short/pkief.starlane-icon-theme.svg?style=for-the-badge&colorA=252526&colorB=43A047&label=VERSION" alt="Version"></a>&nbsp;
    <a href="https://marketplace.visualstudio.com/items?itemName=PKief.starlane-icon-theme"><img src="https://vsmarketplacebadge.apphb.com/rating-short/pkief.starlane-icon-theme.svg?style=for-the-badge&colorA=252526&colorB=43A047&label=Rating" alt="Rating"></a>&nbsp;
    <a href="https://marketplace.visualstudio.com/items?itemName=PKief.starlane-icon-theme"><img src="https://vsmarketplacebadge.apphb.com/installs-short/PKief.starlane-icon-theme.svg?style=for-the-badge&colorA=252526&colorB=43A047&label=Installs" alt="Installs"></a>&nbsp;
    <a href="https://marketplace.visualstudio.com/items?itemName=PKief.starlane-icon-theme"><img src="https://vsmarketplacebadge.apphb.com/downloads-short/PKief.starlane-icon-theme.svg?style=for-the-badge&colorA=252526&colorB=43A047&label=Downloads" alt="Downloads"></a>
</p>

<p align="center"><br>
<b>Sponsored by</b><br><br>
<a title="Try CodeStream" href="https://sponsorlink.codestream.com/?utm_source=vscmarket&amp;utm_campaign=pkief_material&amp;utm_medium=banner"><img width="198px" src="https://alt-images.codestream.com/codestream_logo_pkief_material.png"></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a title="Try Stepsize" href="https://marketplace.visualstudio.com/items?itemName=Stepsize.stepsize"><img width="200px" src="https://raw.githubusercontent.com/PKief/vscode-starlane-icon-theme/main/images/stepsize.png"></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a title="Try Bloop" href="https://bloop.ai/?utm_source=vscmarket&utm_campaign=starlane-icon-theme&utm_medium=banner"><img width="150px" src="https://raw.githubusercontent.com/PKief/vscode-starlane-icon-theme/main/images/bloop.png"></a>
</p>

### File icons

<img src="https://raw.githubusercontent.com/PKief/vscode-starlane-icon-theme/main/images/fileIcons.png" alt="file icons">

### Folder icons

<img src="https://raw.githubusercontent.com/PKief/vscode-starlane-icon-theme/main/images/folderIcons.png" alt="folder icons">

#### Customize folder color

You can change the color of the default folder icon using the command palette:

<img src="https://raw.githubusercontent.com/PKief/vscode-starlane-icon-theme/main/images/set-folder-color.gif" alt="custom folder colors">

or via user settings:

```json
"starlane-icon-theme.folders.color": "#ef5350",
```

#### Folder themes

You can change the design of the folder icons using the command palette:

<img src="https://raw.githubusercontent.com/PKief/vscode-starlane-icon-theme/main/images/set-folder-theme.gif" alt="folder themes">

or via user settings:

```json
"starlane-icon-theme.folders.theme": "specific"
```

## Custom icon opacity

You can set a custom opacity for the icons:

```json
"starlane-icon-theme.opacity": 0.5
```

## Custom icon saturation

If colors do not make you happy you can change the icons to have less saturation making them look grayish or completely grayscale by setting saturation to 0:

```json
"starlane-icon-theme.saturation": 0.5
```

## Custom icon associations

You can customize the icon associations directly in the user settings.

### File associations

With the `*.[extension]` pattern you can define custom file icon associations. For example you could define an icon for `*.sample` and every file that ends with `.sample` will have the defined icon. However, not all files with the same file extension always have the same icon. For some specific file names there is a special icon. In order to overwrite all the specific file icons as well, two asterisks must be set instead of one, i.e. `**.[extension]`.

If there's no leading `*` it will be automatically configured as filename and not as file extension.

```json
"starlane-icon-theme.files.associations": {
    "*.ts": "typescript",
    "**.json": "json",
    "fileName.ts": "angular"
}
```

#### Custom SVG icons

It's possible to add custom icons by adding a path to an SVG file which is located relative to the extension's dist folder. However, the restriction applies that the directory in which the custom icons are located must be within the `extensions` directory of the `.vscode` folder in the user directory.

For example a custom SVG file called `sample.svg` can be placed in an `icons` folder inside of VS Code's `extensions` folder:

```
.vscode
 ┗ extensions
   ┗ icons
     ┗ sample.svg
```

In the settings.json the icon can be associated to a file name or file extension like this:

```json
"starlane-icon-theme.files.associations": {
    "fileName.ts": "../../icons/sample"
}
```

_Note: The custom file name must be configured in the settings without the file ending `.svg` as shown in the example above._

### Folder associations

The following configuration can customize the folder icons. It is also possible to overwrite existing associations and create nice combinations. For example you could change the folder theme to "classic" and define icons only for the folder names you like.

```json
"starlane-icon-theme.folders.associations": {
    "customFolderName": "src",
    "sample": "dist"
}
```

#### Custom SVG folder icons

Similar to the files, it is also possible to reference your own SVG icons for folder icons. Here it's important to provide two SVG files: one for the folder if it's closed and another one for the opened state. These two files - let's call them "folder-sample.svg" and "folder-sample-open.svg" - have to be placed into a directory which is relative to the extensions dist folder. This directory has to be somewhere inside of the `.vscode/extensions` folder.

In our example we place them into an `icons` folder inside of the `.vscode/extensions` folder:

```
.vscode
 ┗ extensions
   ┗ icons
     ┣ folder-sample.svg
     ┗ folder-sample-open.svg
```

In the settings.json the folder icons can be associated to a folder name (e.g. "src") like this:

```json
"starlane-icon-theme.folders.associations": {
    "src": "../../../../icons/folder-sample"
}
```

### Language associations

With the following configuration you can customize the language icons. It is also possible to overwrite existing associations.

```json
"starlane-icon-theme.languages.associations": {
    "languageId": "iconName",
    "json": "json"
}
```

Available language ids:

https://code.visualstudio.com/docs/languages/identifiers#_known-language-identifiers

You can see the available icon names in the overview above.

## One-click activation

After installation or update you can click on the 'Activate'-button to activate the icon theme, if you haven't already. The icons will be visible immediately.

<img src="https://raw.githubusercontent.com/PKief/vscode-starlane-icon-theme/main/images/oneclickactivation.png" alt="activation">

## Commands

Press `Ctrl-Shift-P` to open the command palette and type `Starlane Icons`.

<img src="https://raw.githubusercontent.com/PKief/vscode-starlane-icon-theme/main/images/commandPalette.png" alt="commands">

<p></p>

| Command                           | Description                                                                        |
| --------------------------------- | ---------------------------------------------------------------------------------- |
| **Activate Icon Theme**           | Activate the icon theme.                                                           |
| **Change Folder Color**           | Change the color of the folder icons.                                              |
| **Change Folder Theme**           | Change the design of the folder icons.                                             |
| **Change Opacity**                | Change the opacity of the icons.                                                   |
| **Change Saturation**             | Change the saturation value of the icons.                                          |
| **Configure Icon Packs**          | Select an icon pack that enables additional icons (e.g. for Angular, React, Ngrx). |
| **Hide Folder Arrows**            | Hides the arrows next to the folder icons.                                         |
| **Restore Default Configuration** | Reset the default configurations of the icon theme.                                |
| **Toggle Grayscale**              | Sets the saturation of the icons to zero, so that they are grayscale.              |

## Icon sources

- [Material Design Icons](https://materialdesignicons.com/)
- official icons

## Contributors

<a href="https://github.com/PKief/vscode-starlane-icon-theme/graphs/contributors">
    <img src="https://raw.githubusercontent.com/PKief/vscode-starlane-icon-theme/main/images/contributors.png" alt="Contributors">
</a>

**Would you like to contribute?**

Take a look at the [contribution guidelines](https://github.com/PKief/vscode-starlane-icon-theme/blob/main/CONTRIBUTING.md) and open a [new issue](https://github.com/PKief/vscode-starlane-icon-theme/issues) or [pull request](https://github.com/PKief/vscode-starlane-icon-theme/pulls) on GitHub.

## Related extensions

- [Starlane Icons for GitHub](https://github.com/Claudiohbsantos/github-material-icons-extension)
