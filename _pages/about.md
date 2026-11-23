---
permalink: /
title: About me
author_profile: true
redirect_from:
- /about/
- /about.html
---

I'm a research engineer in Berlin working on generative and multimodal models,
currently on text/image-to-3D foundation models at 404-GEN. I care about the part
of ML that happens after the paper: making models faster, measuring whether they
are actually better, and getting them in front of users.

Before that I led diffusion projects at Picsart AI Research, where our stylized
font model shipped to millions of users, and spent several years in academia
working on multimodal perception. My PhD produced EMOTIC, a benchmark for
recognizing emotions from scene context that has been cited 1,000+ times.


## What I'm working on now

*Updated Nov 2026*

- Post-training text/image-to-3D generators with reinforcement learning from human preferences.
- Agent-orchestrated evaluation: LLM/VLM judges validated against gold-standard labels.
- Serving 3D generation as a production API, with vLLM and GPU failover.


## Highlights

- Open-source text/image-to-mesh generator consistently ranked **top-5** on Hugging Face 3D Arena.
- Optimized mesh generation for **33–50% faster inference and 50% lower VRAM** usage (96GB → 48GB) than the baseline model, with no quality loss and deterministic outputs.
- Shipped generative **diffusion models to production** in the Picsart app serving millions of global users.
- Created and open-sourced **EMOTIC** (34K in-the-wild subjects); published in **IEEE TPAMI** & **CVPR** with 1,000+ citations.

Project write-ups are in the [portfolio](/portfolio/).


## News

- **Jan 2025:** Joined 404-GEN in Berlin to work on text/image-to-3D foundation models.
- **Oct 2024:** Soft-labeled contrastive learning for domain adaptation published at MICCAI 2024.
- **Nov 2022:** Joined Picsart AI Research as Senior ML Scientist / Research Lead.
- **2022:** 3rd Prize for Best Scientific Work at BVM 2022, for few-shot unsupervised multimodal segmentation.


## Recently on GitHub


<div id="gh-repos" data-user="rkosti" data-count="6">
  <p><a href="https://github.com/rkosti?tab=repositories">See my repositories on GitHub</a>.</p>
</div>

<style>
  #gh-repos ul { list-style: none; margin: 0; padding: 0; }
  #gh-repos li { margin: 0 0 0.9em; }
  #gh-repos .gh-meta { display: block; font-size: 0.8em; opacity: 0.75; }
</style>

<script>
(function () {
  var box = document.getElementById("gh-repos");
  var user = box.dataset.user, count = parseInt(box.dataset.count, 10) || 6;
  var skip = [user.toLowerCase(), user.toLowerCase() + ".github.io"];
  fetch("https://api.github.com/users/" + user + "/repos?sort=pushed&per_page=50")
    .then(function (r) { if (!r.ok) throw new Error(r.status); return r.json(); })
    .then(function (repos) {
      repos = repos.filter(function (r) {
        return !r.fork && !r.archived && skip.indexOf(r.name.toLowerCase()) === -1;
      }).slice(0, count);
      if (!repos.length) return;
      var ul = document.createElement("ul");
      repos.forEach(function (r) {
        var li = document.createElement("li");
        var a = document.createElement("a");
        a.href = r.html_url; a.textContent = r.name;
        li.appendChild(a);
        if (r.description) li.appendChild(document.createTextNode(": " + r.description));
        var meta = document.createElement("span");
        meta.className = "gh-meta";
        var bits = [];
        if (r.language) bits.push(r.language);
        if (r.stargazers_count) bits.push(r.stargazers_count + (r.stargazers_count === 1 ? " star" : " stars"));
        bits.push("updated " + new Date(r.pushed_at).toLocaleDateString("en-GB", { month: "short", year: "numeric" }));
        meta.textContent = bits.join(", ");
        li.appendChild(meta);
        ul.appendChild(li);
      });
      box.innerHTML = "";
      box.appendChild(ul);
      var more = document.createElement("p");
      more.innerHTML = '<a href="https://github.com/' + user + '?tab=repositories">All repositories on GitHub</a>';
      box.appendChild(more);
    })
    .catch(function () { /* keep the fallback link */ });
})();
</script>
