# utils-field-picker

![This is a screenshot](https://github.com/RallyTechServices/utils-field-picker/raw/master/screenshot.png)

## Installation
1. Install using npm (or yarn) `npm install '@agile-central-technical-services/utils-field-picker' -D`
2. Add the file to the `javascript` section of `config.json`
    ```
     "javascript": [
        "node_modules/@agile-central-technical-services/utils-field-picker/index.js",
        ...
    ```

## Example usage
To use the control on a page:
```
controlsArea.add({
    xtype: 'tsfieldpickerbutton',
    modelNames: [modelName],
    context: this.getContext(),
    stateful: true,
    stateId: this.getViewType() + 'fields', // columns specific to type of object
    alwaysSelectedValues: alwaysSelectedColumns,
    listeners: {
        fieldsupdated: function(fields) {
            // fields is the currently selected fields from the picker
        },
        scope: this
    }
});
```

To get the current selected fields:
```
this.down('tsfieldpickerbutton').getFields()
```

## Developer Notes
To Update
1. `npm version patch` - This will update the package.json to a new version and create a git tag (e.g. `v1.0.1`). It will also run the `postversion` script
to push the changes and tag to GitHub.
2. `npm publish --access public` - This will publish the new version to npmjs.org
3. Create the new release in [`utils-/releases'](https://github.com/RallyTechServices/utils-field-picker/releases)
