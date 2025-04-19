# Responsive design - Piano Project

## Key words

`inherit` | `::before` | `::after` | `float` | `content` | `@media`

## What I learnt

### ::before & ::after

These create pseudo-selectors `::before` **_creates_** an element which is the **_1st child_** of the selected element. Whilst `::after` **_creates_** a pseudo-element which is the **_last child_** of the selected element

By default these pseudo-elements are **_empty_** and won't be displayed on the page. We can use `content: ""` to override this to ensure the elements aren't empty.

[youTube](https://www.youtube.com/watch?v=dIUOWdwwZBw)

### Media queries

Used to apply CSS based on conditions, typically `max-width` | `min-width`

## Reflection

I couldn't understand the use of `float: left` when positioning they keys. We need to also consider the `overflow: hidden` on its .keys container.

So each key is a **_block_** <div> element with a height of 175px which is only 5px less than it's parent container. `overflow: hidden` will hide all but the firs `key` <div>.

To show all the other keys **_within_** the parent container use `float: left` to display all the other keys next to each other inside the parent container.

Styling the black keys: `::after` creates another element after each **_key_** element, initially these elements wont' be displayed. Use `position: absolute` displays these elements by taking them out of the normal document flow. `left: -18px` positions the black keys where we would expect them to be on a keyboard.

**_NOTE:_** `position: absolute` will only work if an elements **_parent_** container has `position: relative` set.¡

## References

[::before MDN Docs](https://developer.mozilla.org/en-US/docs/Web/CSS/::before)

[::after MDN Docs](https://developer.mozilla.org/en-US/docs/Web/CSS/::after)

[float MDN Docs](https://developer.mozilla.org/en-US/docs/Web/CSS/float)

[Media queries MDN Docs](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_media_queries/Using_media_queries)

[Media queries CSS-Tricks](https://css-tricks.com/a-complete-guide-to-css-media-queries/)
