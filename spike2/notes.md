# Spike 2 notes

## Flexbox

- **Flexbox** = Flexible Box

- Flexbox was introduced as a way to help position HTML elements. You will have a parent container element with the **display** property set to **flex**, and the children elements will be considered the flex **items**/**content**. A flex child item can also have display set to flex, making it a container for its own children.

- Flexbox works best for small-scale layouts, (eg. **&lt;article&gt;** or **&lt;form&gt;** content).

- Excellent guide with images on [css-tricks.com](https://css-tricks.com/snippets/css/a-guide-to-flexbox/).

- The default settings for Flexbox set the **flex-direction** to **row**, and the **flex-wrap** property to **nowrap**.

- **Align** and **justify** properties refer to the position of your elements along the direction axes. Be aware of which axis your elements are aligned on - it will change how these properties apply! By default, **align-items** is set to **stretch**, and **justify-content** is set to **flex-start**.

- The **flex-flow** property can be used to condense **flex-direction** and **flex-wrap** into a single line. eg:

```css
div {
  display: flex;
  flex-flow: column wrap;
}
```

- Flexbox child elements can be positioned independently using properties such as **order** and **self-align**. Playing games like [Flexbox Froggy](https://flexboxfroggy.com/) or [Flexbox Defence](http://www.flexboxdefense.com/) is a fun way to play with all the properties and learn how they work.

## CSS Animations

- **transition** property can be used for small transitions, such as an element reacting to a **pseudo class**. Putting it on both the "before" and "after" states mean it will apply both ways. eg:

```css
div {
  background-color: red;
  transition: 0.2s;
}

div:hover {
  background-color: blue;
  transition: 0.2s;
}
```

- **@keyframes** keyword creates a new CSS animation. Every animation must be given an **identifier**, ie. a name. Curly braces will surround the property changes that are to be applied.

- Your animation will be made up of keyframes, every point from 0-100% can be selected and manually controlled. Tip: setting 0% and 100% the same will ensure a smooth infinite animation loop. eg:

```css
@keyframes identifier {
  0%,
  100% {
    background-color: tomato;
    border-radius: 0%;
  }
  50% {
    background-color: violet;
    border-radius: 50%;
  }
}
```

- **from** and **to** properties can simplify the syntax for a simple, linear animation that only has two steps.

- The animation can then be linked to HTML elements via a selector, and the **animation** property will specify how the animation will apply. Only **animation-name** and **animation-duration** are compulsory for it to run.

- The W3Schools [page on animation](https://www.w3schools.com/css/css3_animations.asp) is a great starting point.
