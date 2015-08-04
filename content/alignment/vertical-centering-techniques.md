# Vertical centering techniques

In this chapter you will learn how to center content vertically using different techniques.

## Center content without a fixed height

If you don't know the size of the content, you can set `position: absolute` along with `top` and `bottom` properties. The browser will set those values automatically.

```css
div{
    position: absolute;
    top: 50px;
    left: 50px;
    bottom: 50px;
    right: 50px;
}
```

## Center content with a fixed height

If the height of the content is a known value, you can use this simple technique to vertically center it. If the box has 300px height, you need to move it 50% down with the `top` property and moving up half the height with the `margin-top` property with a negative value. This CSS trick also centers content horizontally.

```css
div{
    height: 300px;
    position: absolute;
    top: 50%;
    margin-top: -150px;
    left: 50%;
    margin-left: -150px;
}
```

## Center content using flexbox

`flexbox` comes with a nice centering statement that makes the browser do the math. If you center it and make flexbox work in column direction, the content will be vertically centered. Use this technique only when the supported browser implements flexbox.

```css
div{
    display: flex;
    flex-direction: column;
    justify-content: center;
}
```

## Center content using display table

`display: table-cell;` makes an element to behave like a table cell, so `vertical-align: middle;` will just work :)

```css
div{
    display: table-cell;
    vertical-align: middle;
}
```

## Info

__Demo__: http://codepen.io/asainz/pen/yyXaZO  
__Gist__: https://gist.github.com/asainz/4b60ab0e30901d0fc87f

## Credits

Andres Sainz de Aja - andres.sainz@globant.com
