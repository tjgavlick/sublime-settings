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

I've added this to the following items in the base Agila Oceanic Next .thTheme:

- Keyword, Storage: `keyword, storage.type, storage.modifier`
- Attributes: `entity.other.attribute-name`

And in User/Color Highlighter/themes/Agila Oceanic Next.tmTheme:

- Keyword, Storage: `keyword, storage.type, storage.modifier`

And added the following to the base theme to cover some JS language features:

```
<dict>
    <key>name</key>
    <string>JavaScript italics</string>
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
    <string>JavaScript italics overrides</string>
    <key>scope</key>
    <string>keyword.operator.comparison.js, storage.type.function.arrow.js, keyword.operator.assignment.js, keyword.operator.assignment.augmented.js, keyword.operator.arithmetic.js, keyword.operator.logical.js, keyword.operator.relational.js, punctuation.definition.comment.js, keyword.operator.ternary.js, keyword.control.cshtml</string>
    <key>settings</key>
    <dict>
        <key>fontStyle</key>
        <string>normal</string>
    </dict>
</dict>
```

And to the color highlighter override XML:

```
<dict>
    <key>name</key>
    <string>CSS italics</string>
    <key>scope</key>
    <string>entity.other.pseudo-class.css.sass, comment.line.sass, comment.block.css.sass, entity.other.pseudo-class.css, comment.line.css, comment.block.css</string>
    <key>settings</key>
    <dict>
        <key>fontStyle</key>
        <string>italic</string>
    </dict>
</dict>
<dict>
    <key>name</key>
    <string>CSS italics overrides</string>
    <key>scope</key>
    <string>keyword.other.parent-selector.sass, keyword.operator.css.sass, keyword.other.unit.css.sass, variable.parameter.sass, keyword.operator.css, keyword.other.unit.css, variable.parameter.css, keyword.control.interpolation.sass</string>
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
