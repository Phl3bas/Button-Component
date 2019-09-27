# Vue-Button-Component: Fennec


## A Simple button component for Vue.js made for learning purposes


This is a project i started to learn how Vue.js works and how Component frameworks work under the hood. Any suggestions welcome, 
this is only the start (will plan on slowly building other components to make a full library one day!)

This idea was to keep syntax as simple but flexible as possible.

#### Full List of Attributes:
- `red`
- `blue`
- `yellow`
- `green`
- `dark`
- `tall`
- `long`
- `small`
- `tile`
- `flat`
- `round`
- `outline`
- `none`
- `height`
- `width`
- `textsize`


#### Colors:
+ `red`: [No Value] sets background style to default red with white text
```
{
background-color: rgb(235, 77, 77);
color: white;
text-shadow: 1px 2px 3px rgba(0, 0, 0, 0.3);
}
```
+ `blue`: [No Value] sets background style to default blue with white text
```
{
background-color: rgb(68, 70, 167);
color: rgb(255, 255, 255);
text-shadow: 1px 2px 3px rgba(0, 0, 0, 0.3);
}
```
+ `yellow`: [No Value] sets background style to default yellow with ochre text
```
{
background-color: rgb(244, 247, 112);
color: rgb(101, 116, 16);
text-shadow: 1px 2px 3px rgba(0, 0, 0, 0.3);
}
```
+ `green`: [No Value] sets background style to default green with white text
```
{
background-color: rgb(90, 189, 95);
color: white;
text-shadow: 1px 2px 3px rgba(0, 0, 0, 0.3);
}
```
+ `dark`: [No Value] default dark style button with white text
```
{
  background-color: rgb(68, 67, 67);
  color: white;
  text-shadow: 1px 2px 3px rgba(255, 255, 255, 0.3);
}
```

#### Size:
+ `tall`: [No Value] Changes button height and font size
```
{
  height: 60px;
  font-size: 25px;
}
```
+ `long`: [No Value] Changes button width to default 200px
```
{
width: 200px;
}
```
+ `small`: [No Value] Shrinks button height and width, font-size is also scaled down
```
{
  height: 35px;
  width: 60px;
  font-size: 13px;
}
```

+ `height`: [String] takes a string representation of desired height will be converted to 'px'

+ `width`: [String] takes a string representation of desired width will be converted to 'px'

+ `textsize`: [String] takes a string representation of desired fontsize will be converted to 'rem'


#### Style:
+ `tile`: [No Value] Removes border radius of styling to make a tradition material design square button
```
{
border-radius: 0;
}
```
+ `flat`: [No Value] Removes default box shadow to make button appear flat on page
```
{
 box-shadow: none;
}
```
+ `round`: [No Value] Add border radius to make button round
```
{
  border-radius: 20px;
}
```
+ `outline`: [No Value] Adds black border outline to button
```
{
 border: 2px solid black;
  box-shadow: none;
}
```
+ `none`: removes all default styling of button (does not remove default hover/active states at type of writing) 
none is overridden by any other non value attribute
```
{
  box-shadow: none;
  border: none;
  background-color: transparent;
  border-radius: 0;
}
```


