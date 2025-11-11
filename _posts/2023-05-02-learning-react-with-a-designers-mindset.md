---
title: "Learning React with a designer’s mindset"
layout: post
---

When I started learning React, I did what most people do: followed tutorials, copied some code, and tried to understand what `useState` actually _does_.

But the thing is — I came to React mostly from a design background. My brain doesn’t start with “how do I structure this in code?” — it starts with _“what should this look and feel like?”_ and _“how does the user move through it?”_

At first, that felt like a disadvantage. I wasn’t thinking in components and props — I was thinking in buttons, screens, flows.

But then I realized: that’s exactly what components are.

React just gave me names for things I was already designing — “Card”, “Button”, “Form”, “List”. Suddenly, I wasn’t writing code to write code. I was building an interface the same way I’d sketch one: thinking in reusable pieces, visual consistency, and interaction patterns.

Here’s what helped me the most:

- **Start with layout**: I sketched the UI first (even on paper), and then mapped components to parts of the layout.
- **Think in boxes**: Every component is a box with inputs and outputs — props in, UI out.
- **Name with intention**: If I’d call it a “PrimaryButton” in Figma, that’s what I call it in my code.
- **Keep styling scoped**: Just like in design, I try to contain styles to a single idea. CSS modules or Tailwind help.

React started to feel less like a “framework” and more like a toolbox for building the same things I used to draw. It just happens that now I can ship them too.

---

> TL;DR: A designer learning React is not behind. They're just thinking in components before they even touch code.
