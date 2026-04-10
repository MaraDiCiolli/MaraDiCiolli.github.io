---
layout: post
title: "Maintaining a project nobody stars but everyone uses"
date: 2025-11-15
tag: Open Source
excerpt_text: "On the strange life of infrastructure software — downloaded millions of times, mass-ignored on GitHub."
---

I maintain a small utility library that processes config files. It has 47 stars on GitHub and, according to npm, about 2 million weekly downloads. These two numbers tell very different stories about what "success" means in open source.

Nobody gets excited about config parsing. Nobody tweets about it. But when it breaks, I hear about it within minutes — because it's buried four or five levels deep in dependency trees that power tools people actually do care about.

The experience has taught me that the most important software is often the most invisible. And that maintaining it is less about heroic feature work and more about the quiet discipline of not breaking things — of being boring, reliably.
