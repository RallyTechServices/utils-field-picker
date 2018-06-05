# utils-field-picker

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
