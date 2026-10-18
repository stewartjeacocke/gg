---
layout: post
title: "Podtastic Mac GPU access"
---

Love local inference? 

Not quite brave enough to leave your agent in full YOLO mode with free rein over your laptop?

Use podman on a Mac?

Know Debian better than Redhat?

Then you may enjoy [debian-mesa-libkrun-vulkan](https://github.com/stewartjeacocke/debian-mesa-libkrun-vulkan): a rebuilt Debian `mesa-vulkan-drivers` package that lets Debian-based podman containers access GPU acceleration through `libkrun`.

And yes Claude Code did help me figure this all out. 
