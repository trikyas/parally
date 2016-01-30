# parally

Small, simple, flexible scrolling parallax effect jQuery library.

Check out the **[demo][demo]** to see examples. Also note that this plugin requires **[jQuery][jquery]**!

## Simple HTML

Create any element to show image, it can be `<div>` element with CSS `background-image` or just `<img>` tag. Common markup:

```html
<div class="background-img"></div>
<img src="img/example.png" />
```

## Simple JavaScript

Initialize parally with default options.
This will give us parallax effect on elements with CSS `background-image`.

```javascript
$('.background-img').parally();
```

To use parallax effect on `<img>` or anything else, we have to use CSS transforms.

```javascript
$('img').parally({
    mode: 'transform'
});

```

## Configuration

You can pass multiple configuration paramters to the plugin. Below is example code and table of all parameters.

```javascript
$('.img-background').parally({
    speed: 0.4,
    mode: 'background',
    xpos: '50%',
    outer: true,
    offset: -8,
});
```

| Parameter     | Values                                         | Default      | Description                                                                                                                                                                                     |
| ------------- | ---------------------------------------------- | ------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `speed`       | `number`                                       | 0.2          | Parallax moving speed, for comparison: 0.0 doesn't move, 1.0 moves in same rate as screen scrolls.                                                                                              |
| `mode`        | 'background','transform',`function(x,y){}`     | 'background' | Effect mode, used to apply CSS to element, `'background'` - sets elements' `'background-position'`, `'transform'` - uses CSS transforms, also can be callback function with `(x,y)` parameters. |
| `xpos`        | CSS `'background-position'` value              | '50%'        | Used only for 'background' mode, to set background images' X position. Valid values are `left|center|right|0-100%|`.                                                                            |
| `outer`       | `boolean`                                      | true         | Should we use the outer height of element, including margin.                                                                                                                                    |
| `offset`      | `number`                                       | 0            | Vertical offset in pixels. Ff your elements' parallax position doesn't feel right, you can add custom offset.                                                                                   |

## Author

Davis Miculis - [@DavisMiculis][twitter]

## License

Licensed under [MIT][mit].

[demo]: http://davismiculis.github.io/parally/
[jquery]: http://jquery.com/
[twitter]: http://twitter.com/davismiculis
[mit]: /LICENSE