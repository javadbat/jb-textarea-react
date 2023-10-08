# jb-textarea-react

simple textarea react component to input long text

- lightweight
- zero dependancy
- help you manage validation in easy way
- config auto height grow ability with max height

sample: <https://codepen.io/javadbat/pen/poRZVXe>

## installation and setup

```cmd
npm i jb-textarea-react
```

```jsx
import {JBTextarea} from 'jb-textarea-react';

<JBTextarea label="label" value={valueState} message="text under the box"></JBTextarea>
```

## get and set value

```jsx
<JBTextarea label="label" value={valueState} onChange={(e)=>{setValueState(e.target.value)}}></JBTextarea>
```

### events

```js
<JBTextarea  onChange={(e)=>{}}></JBTextarea>
<JBTextarea  onKeydown={(e)=>{}}></JBTextarea>
<JBTextarea  onKeyup={(e)=>{}}></JBTextarea>
<JBTextarea  onKeypress={(e)=>{}}></JBTextarea>
```

### auto height grow

you can set `autoHeight` to true so when user type something and text overflow a textarea height component will grow by itself in boundary of `--jb-textarea-min-height` and `--jb-textarea-max-height` that you set by css variable 

```js
<JBTextarea  autoHeight></JBTextarea>
```

the good point of set boundary with css variable is you can set different min or max base on device by CSS media queries.

### set custome style

in some cases in your project you need to change defualt style of web-component for example you need zero margin or different border-radius and etc.    
if you want to set a custom style to this web-component all you need is to set css variable in parent scope of web-component 
| css variable name                     | description                                                                                   |
| -------------                         | -------------                                                                                 |
| --jb-textarea-margin                  | web-component margin defualt is `0 12px`                                                      |
| --jb-textarea-border-radius           | web-component border-radius defualt is `16px`                                                 |
| --jb-textarea-border-width            | web-component border-width defualt is `1px`                                                   |
| --jb-textarea-border-color            | border color of select in normal mode                                                         |
| --jb-textarea-border-color-focus      | border color of select in normal mode                                                         |
| --jb-textarea-bgcolor                 | background color of input                                                                     |
| --jb-textarea-border-botton-width     | border bottom thickness desualt is `3px`                                                      |
| --jb-textarea-label-font-size         | font size of input label defualt is `0.8em`                                                   |
| --jb-textarea-value-font-size         | font size of input value defualt is `1.1em`                                                   |
| --jb-textarea-value-color             | color of value defualt in `initial`                                                           |
| --jb-textarea-message-font-size       | font size of message we show under input                                                      |
| --jb-textarea-message-error-color     | change color of error we show under input defualt is `red`                                    |
| --jb-textarea-min-height              | minimum height of text area defualt is `80px`                                                 |
| --jb-textarea-max-height              | minimum height of text area defualt is `none`                                                 |
| --jb-textarea-placeholder-color       | placeholder color defualt is 'initial'                                                        |
| --jb-textarea-placeholder-font-size   | placeholder font-size defualt is `initial`                                                    |
| --jb-textarea-label-color             | label color defualt is `#1f1735`                                                              |    
| --jb-textarea-value-color             | value color                                                                                   |