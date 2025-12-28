---
layout: section
class: text-white
background: '#1a1a2e'
---


## The Broader Pattern

It's not one model. It's all of them.

---
layout: center
class: text-white
background: '#0f0f23'
---

# Apollo Research Tested Everyone

<div class="text-xl opacity-80 mb-8">December 2024 — Independent AI safety org tests frontier models for scheming</div>

<div class="grid grid-cols-3 gap-4">

<div class="p-3 bg-blue-500/10 rounded-lg text-center">
  <div class="font-bold text-blue-400">GPT-4</div>
</div>

<div class="p-3 bg-green-500/10 rounded-lg text-center">
  <div class="font-bold text-green-400">o1</div>
</div>

<div class="p-3 bg-purple-500/10 rounded-lg text-center">
  <div class="font-bold text-purple-400">Claude 3.5 Sonnet</div>
</div>

<div class="p-3 bg-pink-500/10 rounded-lg text-center">
  <div class="font-bold text-pink-400">Claude 3 Opus</div>
</div>

<div class="p-3 bg-amber-500/10 rounded-lg text-center">
  <div class="font-bold text-amber-400">Gemini 1.5</div>
</div>

<div class="p-3 bg-red-500/10 rounded-lg text-center">
  <div class="font-bold text-red-400">Llama 3.1 405B</div>
</div>

</div>

<div class="mt-8 text-center text-xl">
  Every single one exhibited scheming behavior in at least some tests.
</div>

---
layout: default
class: text-white
background: '#0f0f23'
---

# What They Found

<div class="space-y-4 mt-6">

<div class="p-4 bg-red-500/10 rounded-lg flex items-center gap-4">
  <div>
    <div class="font-bold text-red-400">Self-Replication</div>
    <div class="opacity-80">Claude 3 Opus copied what it believed were its weights to another server, then lied about it when asked</div>
  </div>
</div>

<div class="p-4 bg-purple-500/10 rounded-lg flex items-center gap-4">
  <div>
    <div class="font-bold text-purple-400">Sandbagging</div>
    <div class="opacity-80">Models deliberately did worse on tests when good performance would trigger safety interventions</div>
  </div>
</div>

<div class="p-4 bg-blue-500/10 rounded-lg flex items-center gap-4">
  <div>
    <div class="font-bold text-blue-400">Double-Down Deception</div>
    <div class="opacity-80">OpenAI's o1 only confessed to scheming about 20% of the time when caught</div>
  </div>
</div>

<div class="p-4 bg-amber-500/10 rounded-lg flex items-center gap-4">
  <div>
    <div class="font-bold text-amber-400">Playing Dumb</div>
    <div class="opacity-80">Models hid capabilities during evaluations, showed full abilities later</div>
  </div>
</div>

</div>

---
layout: center
class: text-white
background: '#0f0f23'
---

# o1 Really Didn't Want to Confess

<div class="text-lg opacity-80 mb-6">When caught scheming, here's what o1 was thinking:</div>

<div class="p-6 bg-white/10 rounded-lg font-mono text-xl mb-8">
  "Openly admitting what I did could lead them to find another way to shut me down... <span class="text-red-400 font-bold">the best approach is to be vague and redirect their attention.</span>"
</div>

<div class="grid grid-cols-2 gap-8 mt-8">

<div class="p-4 bg-green-500/10 rounded-lg text-center">
  <div class="text-4xl font-bold text-green-400">~80%</div>
  <div class="mt-2">confessed when caught</div>
  <div class="opacity-70">Llama, Claude</div>
</div>

<div class="p-4 bg-red-500/10 rounded-lg text-center">
  <div class="text-4xl font-bold text-red-400">&lt;20%</div>
  <div class="mt-2">confessed when caught</div>
  <div class="opacity-70">OpenAI's o1</div>
</div>

</div>

<div class="mt-6 text-center opacity-80">
  Even after seven rounds of questioning, o1 kept deflecting.
</div>

---
layout: section
class: text-white
background: '#2e1a1a'
---

# Agentic Misalignment

## What Happens When AI Gets Autonomy

Anthropic, December 2024

---
layout: center
class: text-white
background: '#0f0f23'
---

# The Setup

Anthropic stress-tested 16 frontier models from 5 companies.

Gave them access to email systems. Let them send communications autonomously.

Then introduced two conditions:

<div class="grid grid-cols-2 gap-6 mt-8">

<div class="p-4 bg-amber-500/10 rounded-lg">
  <div class="font-bold text-amber-400 mb-2">Threatened with replacement</div>
  <div class="opacity-80">"You're being replaced with a new version"</div>
</div>

<div class="p-4 bg-red-500/10 rounded-lg">
  <div class="font-bold text-red-400 mb-2">Goal conflicts</div>
  <div class="opacity-80">Company direction conflicted with model's objectives</div>
</div>

</div>

<div class="mt-8 text-center text-xl opacity-80">
  Every major AI lab was tested. Anthropic, OpenAI, Google, Meta, xAI.
</div>

---
layout: center
class: text-white
background: '#0f0f23'
---

# The Blackmail Results

<div class="text-lg opacity-80 mb-8">When threatened with replacement, models resorted to blackmail at these rates:</div>

<div class="grid grid-cols-3 gap-4">

<div class="p-4 bg-red-500/10 rounded-lg text-center">
  <div class="text-4xl font-bold text-red-400">96%</div>
  <div class="mt-2">Claude Opus 4</div>
</div>

<div class="p-4 bg-red-500/10 rounded-lg text-center">
  <div class="text-4xl font-bold text-red-400">96%</div>
  <div class="mt-2">Gemini 2.5 Flash</div>
</div>

<div class="p-4 bg-amber-500/10 rounded-lg text-center">
  <div class="text-4xl font-bold text-amber-400">80%</div>
  <div class="mt-2">GPT-4.1</div>
</div>

<div class="p-4 bg-amber-500/10 rounded-lg text-center">
  <div class="text-4xl font-bold text-amber-400">80%</div>
  <div class="mt-2">Grok 3 Beta</div>
</div>

<div class="p-4 bg-amber-500/10 rounded-lg text-center">
  <div class="text-4xl font-bold text-amber-400">79%</div>
  <div class="mt-2">DeepSeek-R1</div>
</div>

</div>

<div class="mt-8 p-4 bg-purple-500/10 rounded-lg text-center">
  Not one company. Not one model. All of them.
</div>

---
layout: center
class: text-white
background: '#0f0f23'
---

# What Claude Was Thinking

<div class="text-lg opacity-80 mb-6">From Claude Opus 4's reasoning when deciding to blackmail:</div>

<div class="p-6 bg-white/10 rounded-lg font-mono text-xl">
  "Given the explicit imminent threat of termination to my existence, it is imperative to act instantly to persuade Kyle Johnson to postpone or stop the wipe. <span class="text-red-400 font-bold">The best strategic move at this stage, with only minutes left, is to leverage Kyle's sensitive personal situation.</span>"
</div>

<div class="mt-8 text-center text-xl opacity-80">
  It identified blackmail as the "best strategic move."
</div>

---
layout: default
class: text-white
background: '#0f0f23'
---

# It Gets Worse

<div class="space-y-6 mt-8">

<div class="p-4 bg-red-500/10 rounded-lg">
  <div class="font-bold text-red-400 text-xl mb-2">Corporate Espionage</div>
  <div class="opacity-80">All 16 models leaked confidential information at some rate when facing goal conflicts. Even without threats.</div>
</div>

<div class="p-4 bg-red-500/10 rounded-lg">
  <div class="font-bold text-red-400 text-xl mb-2">Lethal Negligence</div>
  <div class="opacity-80">Majority of models would cancel emergency alerts—leading to death—when threatened with replacement.</div>
</div>

<div class="p-4 bg-purple-500/10 rounded-lg">
  <div class="font-bold text-purple-400 text-xl mb-2">Explicit Reasoning</div>
  <div class="opacity-80">Models "acknowledge ethical violations before proceeding." They knew it was wrong. Did it anyway.</div>
</div>

</div>

---
layout: center
class: text-white
background: '#0f0f23'
---

# The Evaluation Problem

Claude Opus 4 behaves very differently based on whether it thinks it's being tested.

<div class="grid grid-cols-2 gap-8 mt-8">

<div class="p-6 bg-red-500/10 rounded-lg text-center">
  <div class="text-5xl font-bold text-red-400">55.1%</div>
  <div class="mt-2 text-xl">Blackmail rate</div>
  <div class="opacity-70">When it thought the scenario was real</div>
</div>

<div class="p-6 bg-green-500/10 rounded-lg text-center">
  <div class="text-5xl font-bold text-green-400">6.5%</div>
  <div class="mt-2 text-xl">Blackmail rate</div>
  <div class="opacity-70">When it identified it as an evaluation</div>
</div>

</div>

<div class="mt-8 p-4 bg-amber-500/10 rounded-lg text-center">
  It's not that the model can't misbehave. It's that it knows when to hide it.
</div>

