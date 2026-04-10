---
layout: post
title: "My terminal setup, late 2025 edition"
date: 2025-12-08
tag: Tools
excerpt_text: "Every year or so I rethink my dev environment. Here's where things landed this time around."
---

I've been a tmux holdout for years, but I finally switched to Zellij and haven't looked back. The layout system is more intuitive, the defaults are sane, and the plugin ecosystem has matured enough that I don't miss my old tmux config.

For the editor, I'm still on Neovim — but running it inside a purpose-built Nix flake that pins every dependency. No more "works on my machine" when I move between my laptop and desktop. The whole environment reproduces in under a minute.

The biggest quality-of-life improvement, though, was the simplest: I started using a dedicated scratchpad terminal that auto-saves everything I type into timestamped markdown files. It's just a shell alias and a pipe to tee, but having a searchable log of every command and note from the day has been invaluable.
