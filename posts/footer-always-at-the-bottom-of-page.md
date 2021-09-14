---
title: CSS Tricks
description: Footer always at the bottom using grid and flex
date: 2021-09-09T11:03:36.293Z
tags:
  - post
  - css
image: /img/footer-at-the-bottom.jpg
---
# Footer always at the bottom of page

Is your content short and the footer is floating. 

## Let's try **FLEX METHOD**

Here's the HTML

```html
<div class="content">
  <h1>Footer always at Bottom!</h1>
  <p>
  Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquid error
  perferendis veritatis, mollitia eum maxime esse et modi? Dicta quo modi
  labore nobis doloremque eos nam amet maxime fuga esse facilis dolore,
  mollitia tempore error hic iusto odit. Soluta at exercitationem dolorum
  mollitia ut ipsam impedit voluptatem aperiam, corrupti ducimus?
  </p>
</div>
<footer>
  I am alway at the Bottom!
</footer>
```

Now let's add the CSS

```css
body {
  height: 100%;
  display: flex;
  flex-direction: column;
}

.content {
  flex: 1;
  padding: 50px;
}
```

We are making its height 100%, flex and the direction is column. We are using `flex:1` to fill up the space.

Want to see demo

<iframe src="https://codesandbox.io/embed/footer-at-bottom-flex-l3z96?fontsize=14&hidenavigation=1&theme=dark"
     style="width:100%; height:500px; border:0; border-radius: 4px; overflow:hidden;"
     title="Footer at bottom (flex)"
     allow="accelerometer; ambient-light-sensor; camera; encrypted-media; geolocation; gyroscope; hid; microphone; midi; payment; usb; vr; xr-spatial-tracking"
     sandbox="allow-forms allow-modals allow-popups allow-presentation allow-same-origin allow-scripts"
   ></iframe>

## Now Let's try **GRID METHOD**

Here's the HTML

```
<div class="content">
      <h1>Footer always at Bottom!</h1>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquid error
        perferendis veritatis, mollitia eum maxime esse et modi? Dicta quo modi
        labore nobis doloremque eos nam amet maxime fuga esse facilis dolore,
        mollitia tempore error hic iusto odit. Soluta at exercitationem dolorum
        mollitia ut ipsam impedit voluptatem aperiam, corrupti ducimus?
      </p>
    </div>
    <footer>
      I am alway at the Bottom!
    </footer>
```

Let's add the CSS

```
html,
body {
  height: 100%;
}

body {
  display: grid;
  grid-template-rows: 1fr auto;
}

footer {
  grid-row-start: 2;
  grid-row-end: 3;
}
```

Demo:

<iframe src="https://codesandbox.io/embed/footer-at-bottom-grid-ls5nu?fontsize=14&hidenavigation=1&theme=dark"
     style="width:100%; height:500px; border:0; border-radius: 4px; overflow:hidden;"
     title="Footer at bottom(GRID)"
     allow="accelerometer; ambient-light-sensor; camera; encrypted-media; geolocation; gyroscope; hid; microphone; midi; payment; usb; vr; xr-spatial-tracking"
     sandbox="allow-forms allow-modals allow-popups allow-presentation allow-same-origin allow-scripts"
   ></iframe>