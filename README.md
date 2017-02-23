[![Dependency Status](https://david-dm.org/plantain-00/schema-based-json-editor.svg)](https://david-dm.org/plantain-00/schema-based-json-editor)
[![devDependency Status](https://david-dm.org/plantain-00/schema-based-json-editor/dev-status.svg)](https://david-dm.org/plantain-00/schema-based-json-editor#info=devDependencies)
[![Build Status](https://travis-ci.org/plantain-00/schema-based-json-editor.svg?branch=master)](https://travis-ci.org/plantain-00/schema-based-json-editor)
[![npm version](https://badge.fury.io/js/schema-based-json-editor.svg)](https://badge.fury.io/js/schema-based-json-editor)
[![Downloads](https://img.shields.io/npm/dm/schema-based-json-editor.svg)](https://www.npmjs.com/package/schema-based-json-editor)

# schema-based-json-editor

#### install

`npm i schema-based-json-editor`

#### reactjs component demo

```js
import { JSONEditor } from "schema-based-json-editor/dist/react";
```

```jsx
<JSONEditor schema={schema}
    initialValue={initialValue}
    updateValue={this.updateValue}
    theme="bootstrap3"
    icon="fontawesome4"
    locale="zh-cn" />
```

the online demo: https://plantain-00.github.io/schema-based-json-editor/demo/react/index.html

the source code of the demo: https://github.com/plantain-00/schema-based-json-editor/tree/master/demo/react

#### angular2 component demo

```js
import { JSONEditorComponent, BooleanEditorComponent, ArrayEditorComponent, EditorComponent, NullEditorComponent, NumberEditorComponent, ObjectEditorComponent, StringEditorComponent, IconComponent, OptionalComponent, DescriptionComponent } from "schema-based-json-editor/dist/angular";

@NgModule({
    imports: [BrowserModule, FormsModule],
    declarations: [MainComponent, JSONEditorComponent, BooleanEditorComponent, ArrayEditorComponent, EditorComponent, NullEditorComponent, NumberEditorComponent, ObjectEditorComponent, StringEditorComponent, IconComponent, OptionalComponent, DescriptionComponent],
    bootstrap: [MainComponent],
})
class MainModule { }
```

```jsx
<json-editor [schema]="schema"
    [initialValue]="value"
    (updateValue)="updateValue($event)"
    theme="bootstrap3"
    icon="fontawesome4"
    locale="zh-cn">
</json-editor>
```

the online demo: https://plantain-00.github.io/schema-based-json-editor/demo/angular/index.html

the source code of the demo: https://github.com/plantain-00/schema-based-json-editor/tree/master/demo/angular

#### vuejs component demo

`npm i vue vue-class-component`

```js
import "schema-based-json-editor/dist/vue";
```

```jsx
<json-editor :schema="schema"
    :initial-value="value"
    @update-value="updateValue(arguments[0])"
    theme="bootstrap3"
    icon="fontawesome4"
    locale="zh-cn">
</json-editor>
```

the online demo: https://plantain-00.github.io/schema-based-json-editor/demo/vue/index.html

the source code of the demo: https://github.com/plantain-00/schema-based-json-editor/tree/master/demo/vue

#### properties of the component

+ schema: the json schema object
+ initialValue: the initial json
+ updateValue: the function that is invoked when the json is edited in the editor
+ theme: optional, support "bootstrap3" for now
+ icon: optional, support "bootstrap3" and "fontawesome4" for now
+ locale: optional, support "zh-cn" for now
+ readonly: optional, a boolean value
+ dragula: optional, the `dragula` library object if you want to reorder array by drag and drop
+ markdownit: optional, the `markdown-it` library object if you want to preview markdown
+ hljs: optional, the `highlight.js` library object if you want to highlight code
+ forceHttps: optional, a boolean value, if true, the preview url of images will be `https://` rather than `http://`

#### features

+ reactjs component
+ angular2 component
+ vuejs component
+ common schema fields: title, description, default, readonly, propertyOrder
+ object schema fields: properties, required, maxProperties, minProperties, collapsed
+ array schema fields: items, minItems, uniqueItems
+ number and integer shema fields: minimum, exclusiveMinimum, maximum, exclusiveMaximum, enum, multipleOf, collapsed
+ string schema fields: format, enum, minLength, maxLength, pattern
+ image preview, code highlight, markdown preview

#### change logs

https://github.com/plantain-00/schema-based-json-editor/tree/master/change_logs.md
