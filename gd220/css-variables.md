---

# CSS variables


???
First thing's first...


--
count: false

- What's a **variable**?


???
shorthand, alias, nickname


--
count: false

- Why would we use variables?


???
reduce repetition, reduce errors


---

# CSS variables

- What do they look like?

```css
--color-crimson: hsl(360, 90%, 15%);
```

--
count: false

```css
--font-serif: 'Merriweather', 'Georgia', serif;
```


???
- two dashes in front of name
- no spaces in name
- variable name is case sensitive
- my examples are for color and font names, but can be used elsewhere
- I recommend starting with these things, however
- Limitations: Can only be used as property values NOT property names



---
count: false

# CSS variables

## Global

```css
:root {
--color-crimson: hsl(360, 90%, 15%);
}
```

--
count: false

## Scoped

```css
.your-class {
--color-crimson: hsl(360, 90%, 15%);
}
```


---

# CSS variables

## Using CSS variables

### Before

```css
p {
color: hsl(360, 90%, 15%);
}
```


---
count: false

# CSS variables

## Using CSS variables

### After

```css
:root {
--color-crimson: hsl(360, 90%, 15%);
}
```

```css
p {
color: var(--color-crimson);
}
```


???
replaces traditional value

like CSS classes -- you have to create them in the HTML, then attach styles to them in your stylesheet -- here you have to create and define the variable before you can use it

- @timer = 10m / 115


---
# CSS variables

## CodePen demo

[![codepen link](img/logo_codepen.png)](https://codepen.io/angeliquejw/pres/drpgJx)



???
### https://codepen.io/angeliquejw/pres/drpgJx
- cascade
- @timer = 10m / 125


---
class: center, middle, title
count: false

# CSS Variables Q&A


???
@timer 5m / 135

