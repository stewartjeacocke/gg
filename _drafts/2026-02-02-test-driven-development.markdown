---
layout: post
title:  "Spec Driven Development"
---
Inspired by some posts and discussions with my colleaguesincluding [Simon Greig]('https://www.linkedin.com/pulse/trying-out-vibe-coding-verifying-emperors-nudist-tendencies-greig-tcpne') 
and [Jack Stevenson]('https://www.linkedin.com/posts/activity-7419744043078676481-PJI8?utm_source=share&utm_medium=member_desktop&rcm=ACoAAAAyu5ABlZMsnnn-DjNgTQ1SY-gPO1UCrkA') 
I've bene experimenting with spec-driven AI coding.

Over the past few weeks I’ve been experimenting with spec‑driven development using spec‑kitty as a way of quickly prototyping software ideas. It’s been an interesting reminder that, while the tools are new, the underlying idea is not.
I tend to think of spec‑driven development as part of a long continuum that includes 4GLs and CASE tools. All of these approaches aim to move the centre of gravity away from hand‑coded implementation and towards a more explicit, structured articulation of intent. What’s different now is how effectively large language models can engage with those specifications and help explore them interactively.


As a concrete experiment, over four sessions of around two hours each, I built up a working prototype of a very simple case list application. The work had to be spread across multiple sessions because the approach is quite token‑hungry; I repeatedly ran into the limits of my Claude subscription and had to pause and resume. That cadence actually reinforced the idea of specifications as durable artefacts you can return to and refine, rather than a single prompt you “fire and forget”.
Where spec‑kitty really shone was in helping me think through the requirements. It continuously prompted me to be more explicit about details I might otherwise have glossed over. Seemingly small questions — Should users be able to see who a case is allocated to? Is that always appropriate? — surfaced naturally through the dialogue. I can easily see this being a powerful complement for a business analyst, especially in the early stages of shaping and stress‑testing requirements.
There were also some useful lessons about limits. I explicitly stated that unit tests were required, but in the initial iterations none were created. That instruction was effectively ignored until the omission was noticed and corrected in a later pass. It was a good reminder that, even in a spec‑driven approach, intent still needs to be checked, reinforced, and validated — the tooling doesn’t remove the need for professional scepticism.
Overall, the experiment left me optimistic. Spec‑driven development won’t replace traditional engineering skills, but as part of a broader lineage running from 4GLs through CASE to today’s AI‑assisted tooling, it feels like a genuinely useful step forward — particularly for rapid exploration, shared understanding, and early validation.
