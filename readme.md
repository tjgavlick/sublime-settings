# Sublime Settings

## Operator Mono

For better usage of the Operator Mono typeface, some items may be made italic in the theme. To do this:

1. Install Package Resource Viewer
2. Use "Package Resource Viewer: Open Resource"
3. Navigate to your theme (the .tmTheme specified in your prefs — mine is Agila)
4. Add an italic specification to taste.

Specify italics by inserting the following block inside a setting's inner `<dict>`:

```
<key>fontStyle</key>
<string>italic</string>
```

I've added this to the following items in Agila Oceanic Next:

- Keyword, Storage: `keyword, storage.type, storage.modifier`
- Attributes: `entity.other.attribute-name`

And added the following to cover some JS language features:

```
<dict>
    <key>name</key>
    <string>JavaScript keywords</string>
    <key>scope</key>
    <string>constant.language.null.js, constant.language.boolean.true.js, constant.language.boolean.false.js, constant.language.undefined.js, constant.language.nan.js, support.type.object.dom.js, support.class.builtin.js, comment.block.js, comment.line.double-slash.js</string>
    <key>settings</key>
    <dict>
        <key>fontStyle</key>
        <string>italic</string>
    </dict>
</dict>
<dict>
    <key>name</key>
    <string>Ligs</string>
    <key>scope</key>
    <string>keyword.operator.comparison.js, storage.type.function.arrow.js, keyword.operator.assignment.js, keyword.operator.assignment.augmented.js, keyword.operator.arithmetic.js, punctuation.definition.comment.js</string>
    <key>settings</key>
    <dict>
        <key>fontStyle</key>
        <string>normal</string>
    </dict>
</dict>
```

## Ligatures

I'm using the wonderful [operator-mono-lig](https://github.com/kiliman/operator-mono-lig) by kiliman to upgrade Operator Mono with Fira Code-like ligatures.

Use Sublime Text build 3146 or later to get full ligature support.
