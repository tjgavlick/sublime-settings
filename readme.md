# Sublime Settings

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

- Language methods: `variable.language`
- Attributes: `entity.other.attribute-name`

And added the following to cover some JS keywords:

```
<dict>
    <key>name</key>
    <string>JavaScript keywords</string>
    <key>scope</key>
    <string>constant.language.null.js, constant.language.boolean.true.js, constant.language.boolean.false.js, constant.language.undefined.js, constant.language.nan.js, support.type.object.dom.js, support.class.builtin.js</string>
    <key>settings</key>
    <dict>
        <key>fontStyle</key>
        <string>italic</string>
    </dict>
</dict>
```

