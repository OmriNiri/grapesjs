<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

## Canvas

You can customize the initial state of the module from the editor initialization, by passing the following [Configuration Object][1]

```js
const editor = grapesjs.init({
 canvas: {
   // options
 }
})
```

Once the editor is instantiated you can use its API. Before using these methods you should get the module from the instance

```js
const canvas = editor.Canvas;
```

-   [getConfig][2]
-   [getElement][3]
-   [getFrameEl][4]
-   [getWindow][5]
-   [getDocument][6]
-   [getBody][7]
-   [getWrapperEl][8]
-   [setCustomBadgeLabel][9]
-   [hasFocus][10]
-   [scrollTo][11]
-   [setZoom][12]
-   [getZoom][13]

## getConfig

Get the configuration object

Returns **[Object][14]** 

## getElement

Get the canvas element

Returns **[HTMLElement][15]** 

## getFrameEl

Get the iframe element of the canvas

Returns **[HTMLIFrameElement][16]** 

## getWindow

Get the window instance of the iframe element

Returns **[Window][17]** 

## getDocument

Get the document of the iframe element

Returns **HTMLDocument** 

## getBody

Get the body of the iframe element

Returns **[HTMLBodyElement][18]** 

## getWrapperEl

Get the wrapper element containing all the components

Returns **[HTMLElement][15]** 

## setCustomBadgeLabel

Set custom badge naming strategy

### Parameters

-   `f` **[Function][19]** 

### Examples

```javascript
canvas.setCustomBadgeLabel(function(component){
 return component.getName();
});
```

## getRect

Get canvas rectangular data

Returns **[Object][14]** 

## hasFocus

Check if the canvas is focused

Returns **[Boolean][20]** 

## scrollTo

Scroll canvas to the element if it's not visible. The scrolling is
executed via `scrollIntoView` API and options of this method are
passed to it. For instance, you can scroll smoothly by using
`{ behavior: 'smooth' }`.

### Parameters

-   `el` **([HTMLElement][15] | Component)** 
-   `opts` **[Object][14]** Options, same as options for `scrollIntoView` (optional, default `{}`)
    -   `opts.force` **[Boolean][20]** Force the scroll, even if the element is already visible (optional, default `false`)

### Examples

```javascript
const selected = editor.getSelected();
// Scroll smoothly (this behavior can be polyfilled)
canvas.scrollTo(selected, { behavior: 'smooth' });
// Force the scroll, even if the element is alredy visible
canvas.scrollTo(selected, { force: true });
```

## setZoom

Set zoom value

### Parameters

-   `value` **[Number][21]** The zoom value, from 0 to 100

Returns **this** 

## getZoom

Get zoom value

Returns **[Number][21]** 

[1]: https://github.com/artf/grapesjs/blob/master/src/canvas/config/config.js

[2]: #getconfig

[3]: #getelement

[4]: #getframeel

[5]: #getwindow

[6]: #getdocument

[7]: #getbody

[8]: #getwrapperel

[9]: #setcustombadgelabel

[10]: #hasfocus

[11]: #scrollto

[12]: #setzoom

[13]: #getzoom

[14]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object

[15]: https://developer.mozilla.org/docs/Web/HTML/Element

[16]: https://developer.mozilla.org/docs/Web/API/HTMLIFrameElement

[17]: https://developer.mozilla.org/docs/Web/API/Window

[18]: https://developer.mozilla.org/docs/Web/HTML/Element/body

[19]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function

[20]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean

[21]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number
