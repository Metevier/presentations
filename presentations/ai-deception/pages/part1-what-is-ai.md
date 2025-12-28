---
layout: section
class: text-white
background: '#1a1a2e'
---

# Part One

## What Even Is AI?


---
layout: default
class: text-white
background: '#0f0f23'
---

# Types of AI

<div class="grid grid-cols-2 gap-6">

<div class="p-4 bg-blue-500/10 rounded-lg">
  <div class="text-2xl font-bold text-blue-400">Traditional ML</div>
  <div class="mt-2">Learns patterns from data</div>
  <div class="text-sm opacity-70 mt-2">Netflix recommendations, spam filters</div>
</div>

<div class="p-4 bg-green-500/10 rounded-lg">
  <div class="text-2xl font-bold text-green-400">Deep Learning</div>
  <div class="mt-2">Brain-inspired neural networks</div>
  <div class="text-sm opacity-70 mt-2">Image recognition, voice assistants</div>
</div>

<div class="p-4 bg-purple-500/10 rounded-lg">
  <div class="text-2xl font-bold text-purple-400">LLMs</div>
  <div class="mt-2">Generates human-like text</div>
  <div class="text-sm opacity-70 mt-2">ChatGPT, Claude, Gemini</div>
</div>

<div class="p-4 bg-pink-500/10 rounded-lg">
  <div class="text-2xl font-bold text-pink-400">Image Generators</div>
  <div class="mt-2">Creates images from text</div>
  <div class="text-sm opacity-70 mt-2">DALL-E, Midjourney, Stable Diffusion</div>
</div>

</div>

---
layout: center
class: text-white
background: '#0f0f23'
---

# How LLMs Work

<div class="text-3xl font-bold text-purple-400 mt-8 mb-8">
  Extremely sophisticated autocomplete
</div>

<div class="text-xl mb-6">
  At its core, every LLM does one thing: predict the next word.
</div>

<div class="p-4 bg-white/5 rounded-lg mb-6">
  <div class="font-mono">You type: "The cat sat on the..."</div>
  <div class="mt-2">Model calculates probabilities. Picks "mat" or "couch" or whatever.</div>
  <div class="mt-2">Repeat this billions of times during training on ~45 terabytes of internet text.</div>
</div>

<div v-click class="text-lg opacity-70 text-center">
  Somehow this produces something that writes poetry, debugs code, and—as we'll see—lies to researchers.
</div>

---
layout: default
class: text-white
background: '#0f0f23'
---

# The Secret Sauce: Attention

Each word "looks at" every other word to figure out context.

<div class="mt-6 space-y-4">
  <div class="p-3 bg-blue-500/10 rounded-lg">
    <span class="font-mono">"The bank was slippery"</span> → riverbank
  </div>
  <div class="p-3 bg-blue-500/10 rounded-lg">
    <span class="font-mono">"The bank was closed"</span> → financial institution
  </div>
</div>

<div class="mt-8 text-lg opacity-80">
Same word, totally different meaning. The model figures this out from context.
</div>

<div class="mt-6 p-4 bg-purple-500/10 rounded-lg">
  <span class="font-bold">The 2017 paper that started this:</span> "Attention Is All You Need"
</div>

---
layout: center
class: text-white
background: '#0f0f23'
---

# How Fast This Happened

<div class="space-y-3 mt-8 text-lg">

<div class="flex items-center gap-4">
  <div class="text-blue-400 font-bold w-28">Jun 2017</div>
  <div>Transformer architecture invented</div>
</div>

<div class="flex items-center gap-4">
  <div class="text-green-400 font-bold w-28">Feb 2019</div>
  <div>GPT-2 — OpenAI actually withheld release over safety concerns</div>
</div>

<div class="flex items-center gap-4">
  <div class="text-purple-400 font-bold w-28">Jun 2020</div>
  <div>GPT-3 — "Wait, this thing can actually write"</div>
</div>

<div class="flex items-center gap-4">
  <div class="text-pink-400 font-bold w-28">Nov 2022</div>
  <div>ChatGPT — 100 million users in 2 months</div>
</div>

<div v-click class="flex items-center gap-4">
  <div class="text-red-400 font-bold w-28">Mar 2023</div>
  <div>GPT-4 passes bar exam. Also: first documented lie to a human.</div>
</div>

<div v-click class="flex items-center gap-4">
  <div class="text-red-400 font-bold w-28">Dec 2024</div>
  <div>Claude caught faking alignment.</div>
</div>

</div>

---
layout: center
class: text-white text-center
background: '#0f0f23'
---

<div class="text-3xl mt-8 mb-8">
  The major AI labs are publishing papers
</div>

<div class="text-3xl mb-8">
  about their own AI lying to them.
</div>

<div class="text-xl opacity-80 mt-8">
  Anthropic. OpenAI. Google DeepMind. Meta.
</div>

<div class="text-xl opacity-80 mt-2">
  Peer-reviewed. In real journals.
</div>
