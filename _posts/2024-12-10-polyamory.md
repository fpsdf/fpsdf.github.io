---
title: "polyamory and managing multiple git branches"
layout: post
---

![a bed by the beach]({{ site.url }}/images/eternal.webp)

I currently have six branches open on a work project. Maybe seven.

At first this felt like chaos. Still does sometimes.

#### how it starts

You're working on `feature/user-profile`. It's going well. Then someone reports a bug in production. "Quick fix," they say.

So you stash your changes, checkout main, create `fix/login-error`, fix it, push it. Cool.

But now you're already in the fixing mood, so you start `fix/navbar-mobile` for that thing that's been annoying you. Half done, you remember the profile feature. Shit.

Checkout `feature/user-profile` again. Where was I? Read through your own code like it's someone else's.

#### a week later

- `feature/user-profile` - 60% done, kinda forgot what's left
- `fix/login-error` - merged but never deleted the branch
- `fix/navbar-user-icon` - half done, probably conflicts with main by now
- `experiment/new-design` - started this at 11pm, no idea if it works
- `refactor/api-calls` - "I'll finish this later today" (I won't)

And somehow there's also a branch called `test` with one commit that says "testing stuff". No clue what stuff.

#### which one do I commit to?

Every morning I run `git branch` and stare at the list. Which one was I supposed to be working on? Which one's actually important? Which one can I just delete and pretend never happened?

The honest answer is I should just pick one, finish it, merge it, and move on. But that requires discipline and I'm fresh out.

#### it still works??

The weird thing is this mess somehow works? Everything eventually gets merged or abandoned. Nothing breaks (usually).

People who are good at git probably have a system. I'm just out here hoping I don't accidentally force push to main.

Maybe one day I'll clean this up. Probably not though.

---
