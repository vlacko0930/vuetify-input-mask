# vuetify-input-mask

Yet another Vuetify component for input masking. Based on [vue-input-mask](https://github.com/xdimedrolx/vue-input-mask).

#### [Demo](http://sanniassin.github.io/react-input-mask/demo.html)

## Install
```
npm i -S vuetify-input-mask
```

## Properties
### `mask` : `string`

Mask string. Default format characters are:<br/>
`9`: `0-9`<br/>
`a`: `A-Z, a-z`<br/>
`*`: `A-Z, a-z, 0-9`

Any character can be escaped with a backslash. It will appear as a double backslash in JS strings. For example, a German phone mask with unremoveable prefix +49 will look like <code>mask="+4\\9 99 999 99"</code> or <code>mask={'+4\\\\9 99 999 99'}</code>

### `maskChar` : `string`

Character to cover unfilled parts of the mask. Default character is "\_". If set to null or empty string, unfilled parts will be empty as in ordinary input.

### `formatChars` : `object`

Defines format characters with characters as a keys and corresponding RegExp strings as a values. Default ones:
```js
{
  '9': '[0-9]',
  'a': '[A-Za-z]',
  '*': '[A-Za-z0-9]'
}
```

### `alwaysShowMask` : `boolean`

Show mask when input is empty and has no focus.

## Example
```js
import Vue from 'vue';
import InputMask from 'vuetify-input-mask';

Vue.component('v-input-mask', InputMask)
```

In template:
```html
    <v-input-mask v-model="value" mask="+4\9 99 999 99" maskChar=" "></v-input-mask>
```

## Todo
- [ ] Refactoring
- [ ] Tests
- [ ] Implementation of `componentWillReceiveProps`

## Thanks
Thanks @sanniassin for the awesome component
