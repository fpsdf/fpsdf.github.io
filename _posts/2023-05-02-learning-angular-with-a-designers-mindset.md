---
title: "learning Angular with a designer’s mindset"
layout: post
---

when I started learning Angular, I did what most people do: followed tutorials, copied some code, and tried to understand what `rxjs` actually does.

but the thing is — I came to Angular mostly from a design background. my brain doesn’t start with “how do I structure this in code?” — it starts with _“what should this look and feel like?”_ and _“how does the user move through it?”_

at first, that felt like a disadvantage. I wasn’t thinking in components and inputs — I was thinking in buttons, screens, flows.

but then I realized: that’s exactly what components are.

Angular just gave me names for things I was already designing — “Card”, “Button”, “Form”, “List”. suddenly, I wasn’t writing code to write code. I was building an interface the same way I’d sketch one: thinking in reusable pieces, visual consistency, and interaction patterns.

here’s what helped me the most:

- **start with layout**: I sketched the UI first (even on paper), and then mapped components to parts of the layout.
- **think in boxes**: every component is a box with an input and an outputs — data in, UI and events out.
- **name with intention**: if I’d call it a “PrimaryButton” in Figma, that’s what I call it in my code.
- **keep styling scoped**: Angular scopes styles to components by default.

Angular started to feel less like a framework and more like a toolbox for building the same things I used to draw.

---
