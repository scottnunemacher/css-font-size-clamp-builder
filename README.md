# CSS Font Size Clamp Builder

View here: [codesandbox.io/s/github/scottnunemacher/css-font-size-clamp-builder](https://codesandbox.io/s/github/scottnunemacher/css-font-size-clamp-builder)

Originally created by: [codesandbox.io/u/pprg1996](https://codesandbox.io/u/pprg1996)

## Style Notes for CSS Font-Size Clamp Builder

Some example h1-h6 heading settings to create good resizable headers between the viewport sizes of 479 and 1200.

***NOTE:*** These settings use the "62.5% font-size trick". If you are not using `html {font-size: 62.5%;}` in your CSS then change each `1rem equals (px)` value to `16` and change Min-Max font sizes accordingly. Missing these adjustments will greatly change your font size outputs.

### Settings

|Field|h1|h2|h3|h4|h5|h6|
|---|---|---|---|---|---|---|
|Minimum viewport width (px)|479|479|479|479|479|479|
|Maximum viewport width (px)|1200|1200|1200|1200|1200|1200|
|Minimum font size (rem)|3.2|2.8|2.4|2.2|2.0|1.8|
|Maximum font size (rem)|4.2|3.4|2.8|2.4|2.2|2.0|
|1rem equals (px)|10|10|10|10|10|10|

*Creates:*

```css
h1 { 
  font-size: clamp(3.2rem, 2.5356rem + 1.3870vw, 4.2rem);
}
h2 { 
  font-size: clamp(2.8rem, 2.4014rem + 0.8322vw, 3.4rem);
}
h3 { 
  font-size: clamp(2.4rem, 2.1343rem + 0.5548vw, 2.8rem);
}
h4 { 
  font-size: clamp(2.2rem, 2.0671rem + 0.2774vw, 2.4rem);
}
h5 { 
  font-size: clamp(2rem, 1.8671rem + 0.2774vw, 2.2rem);
}
h6 { 
  font-size: clamp(1.8rem, 1.6671rem + 0.2774vw, 2rem);
}
```
