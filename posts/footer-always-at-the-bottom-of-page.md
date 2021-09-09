---
title: Footer always at the bottom of page
description: Is your content short and the footer is floating. Then let's fix it using flex
date: 2021-09-09T11:03:36.293Z
tags:
  - post
  - css
image: https://images.unsplash.com/photo-1621839673705-6617adf9e890?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=889&q=80
---
Let's make HTML

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

Want to see demo

<https://codesandbox.io/embed/footer-at-bottom-flex-l3z96?fontsize=14&hidenavigation=1&module=%2Fstyle.css&theme=dark&view=preview>