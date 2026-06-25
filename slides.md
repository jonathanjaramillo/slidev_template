---
theme: default
highlighter: shiki
css: unocss
colorSchema: dark
title: 'Component Cheat Sheet'
info: |
  ## Slidev Component Cheat Sheet
  Reference deck for reusable slide components.
class: text-center
transition: fade-out
lineNumbers: false
drawings:
  persist: false
mdc: true
vite:
  server:
    fs:
      strict: false
glowSeed: 229
---

# Component Cheat Sheet

### Reusable Slidev building blocks

<div class="pt-6 opacity-80 text-lg">
Reference this deck when specifying slide layouts
</div>

<div class="pt-10 text-sm opacity-60">
`title-slide` · centered layout · glow background
</div>

<!--
title-slide: class: text-center, no layout specified. Title + subtitle + two caption lines.
-->

---
glowSeed: 100
---

# 3-Column Accent Card Grid

Each card clicks in separately with `v-click`. Use any accent color per card.

<div class="grid grid-cols-3 gap-4 mt-8">

<div v-click border="2 solid teal-700" bg="teal-800/20" rounded-lg overflow-hidden>
<div class="text-xs font-mono text-white/25 px-4 pt-2 tracking-wide">accent-card · teal · with stat-value</div>
<div bg="teal-800/40" px-4 py-2 flex items-center gap-2>
<span text-xl>📈</span>
<span font-bold>Card Title</span>
</div>
<div px-4 py-4 text-sm>
<div class="text-3xl font-bold text-teal-400 mb-2">stat-value</div>
Supporting explanation text goes here.
</div>
</div>

<div v-click border="2 solid blue-700" bg="blue-800/20" rounded-lg overflow-hidden>
<div class="text-xs font-mono text-white/25 px-4 pt-2 tracking-wide">accent-card · blue</div>
<div bg="blue-800/40" px-4 py-2 flex items-center gap-2>
<span text-xl>🏗️</span>
<span font-bold>Card Title</span>
</div>
<div px-4 py-3 text-sm>
Supporting text with <strong>bold</strong> where needed.
</div>
</div>

<div v-click border="2 solid orange-700" bg="orange-800/20" rounded-lg overflow-hidden>
<div class="text-xs font-mono text-white/25 px-4 pt-2 tracking-wide">accent-card · orange</div>
<div bg="orange-800/40" px-4 py-2 flex items-center gap-2>
<span text-xl>🔧</span>
<span font-bold>Card Title</span>
</div>
<div px-4 py-3 text-sm>
Supporting text with <em>italic</em> where needed.
</div>
</div>

</div>

<!-- accent colors: teal · blue · orange · red · amber · violet · green -->

---
glowSeed: 175
---

# 3-Column Cards + Bottom Banner

Cards click in, then the `bottom-banner` appears last.

<div class="grid grid-cols-3 gap-4 mt-8">

<div v-click border="2 solid red-800" bg="red-800/20" rounded-lg overflow-hidden>
<div class="text-xs font-mono text-white/25 px-4 pt-2 tracking-wide">accent-card · red</div>
<div bg="red-800/40" px-4 py-2 flex items-center gap-2>
<span text-xl>🖥️</span>
<span font-bold>Card Title</span>
</div>
<div px-4 py-3 text-sm>
Card content with <strong>bold text</strong> for emphasis.
</div>
</div>

<div v-click border="2 solid amber-800" bg="amber-800/20" rounded-lg overflow-hidden>
<div class="text-xs font-mono text-white/25 px-4 pt-2 tracking-wide">accent-card · amber</div>
<div bg="amber-800/40" px-4 py-2 flex items-center gap-2>
<span text-xl>📦</span>
<span font-bold>Card Title</span>
</div>
<div px-4 py-3 text-sm>
Card content with <strong>bold text</strong> for emphasis.
</div>
</div>

<div v-click border="2 solid violet-800" bg="violet-800/20" rounded-lg overflow-hidden>
<div class="text-xs font-mono text-white/25 px-4 pt-2 tracking-wide">accent-card · violet</div>
<div bg="violet-800/40" px-4 py-2 flex items-center gap-2>
<span text-xl>🤖</span>
<span font-bold>Card Title</span>
</div>
<div px-4 py-3 text-sm>
Card content with a key <strong>conclusion</strong>.
</div>
</div>

</div>

<div v-click class="mt-10 flex justify-center">
<div border="2 solid white/5" bg="white/5" backdrop-blur-sm rounded-lg px-6 py-3 text-lg>
<span class="text-xs font-mono text-white/25 mr-3 tracking-wide">bottom-banner</span>
Punchline or summary: <strong>key action</strong> or <strong>conclusion</strong>.
</div>
</div>

---
glowSeed: 123
---

# Numbered List

Items animate in together via `<v-clicks>`. Numbers use `text-teal-400`.

<div class="text-sm opacity-70 mb-6"><span class="text-xs font-mono text-white/25 tracking-wide">subheading</span> · Optional framing sentence.</div>

<v-clicks>

<div border="2 solid white/5" bg="white/5" backdrop-blur-sm rounded-lg flex items-start gap-4 px-5 py-4 mb-4>
<div class="text-4xl font-bold text-teal-400">1</div>
<div class="text-xl pt-1">
<span class="text-xs font-mono text-white/25 block mb-1 tracking-wide">numbered-list-item</span>
First key question or point with <strong>emphasis</strong> on important terms.
</div>
</div>

<div border="2 solid white/5" bg="white/5" backdrop-blur-sm rounded-lg flex items-start gap-4 px-5 py-4 mb-4>
<div class="text-4xl font-bold text-teal-400">2</div>
<div class="text-xl pt-1">
<span class="text-xs font-mono text-white/25 block mb-1 tracking-wide">numbered-list-item</span>
Second key question or point with <strong>emphasis</strong> on important terms.
</div>
</div>

<div border="2 solid white/5" bg="white/5" backdrop-blur-sm rounded-lg flex items-start gap-4 px-5 py-4 mb-4>
<div class="text-4xl font-bold text-teal-400">3</div>
<div class="text-xl pt-1">
<span class="text-xs font-mono text-white/25 block mb-1 tracking-wide">numbered-list-item</span>
Third key question or point with <strong>emphasis</strong> on important terms.
</div>
</div>

</v-clicks>

---
layout: two-cols
layoutClass: gap-8
glowSeed: 180
---

# Two-Column Layout

`layout: two-cols` · left column is default slot, right is `::right::`.

<v-clicks>

- **Point one** — description
- **Point two** — description
- **Point three** — description

Supporting sentence or context.

</v-clicks>

::right::

<div v-click class="mt-8" border="2 solid white/5" bg="white/5" backdrop-blur-sm rounded-lg overflow-hidden>
<div class="text-xs font-mono text-white/25 px-4 pt-2 tracking-wide">glass-card · with icon-header (carbon icon)</div>
<div bg="white/10" backdrop-blur px-4 py-2 flex items-center gap-2>
<div i-carbon:group text-teal-300 text-xl />
<span font-bold>Box Title</span>
</div>
<div px-5 py-4>

<div class="grid grid-cols-2 gap-4 text-center">
<div border="2 solid teal-800" bg="teal-800/20" rounded-lg p-4>
<div class="text-xs font-mono text-white/25 mb-1 tracking-wide">stat-tile · teal</div>
<div class="text-4xl font-bold">42</div>
<div class="text-sm opacity-80">Label A</div>
</div>
<div border="2 solid amber-800" bg="amber-800/20" rounded-lg p-4>
<div class="text-xs font-mono text-white/25 mb-1 tracking-wide">stat-tile · amber</div>
<div class="text-4xl font-bold">18</div>
<div class="text-sm opacity-80">Label B</div>
</div>
</div>

<div class="mt-6 text-sm opacity-80">
Supporting note or footer text.
</div>

</div>
</div>

---
glowSeed: 350
---

# Two-Column Content Cards

Two cards side by side — `glass-card` (neutral) and `accent-card`.

<div class="grid grid-cols-2 gap-8 mt-6">

<div v-click border="2 solid white/5" bg="white/5" backdrop-blur-sm rounded-lg overflow-hidden>
<div class="text-xs font-mono text-white/25 px-4 pt-2 tracking-wide">glass-card · with icon-header (carbon icon)</div>
<div bg="white/10" backdrop-blur px-4 py-2 flex items-center gap-2>
<div i-carbon:flow text-blue-300 text-xl />
<span font-bold>How it works</span>
</div>
<div px-5 py-4>

- **Item one:** description
- **Item two:** description
- **Item three:** description
- **Item four:** description

</div>
</div>

<div v-click border="2 solid teal-800" bg="teal-800/20" rounded-lg overflow-hidden>
<div class="text-xs font-mono text-white/25 px-4 pt-2 tracking-wide">accent-card · teal · with icon-header</div>
<div bg="teal-800/40" px-4 py-2 flex items-center gap-2>
<div i-carbon:idea text-teal-300 text-xl />
<span font-bold>Key insight</span>
</div>
<div px-5 py-4>

Key insight or takeaway paragraph. Keep it short and punchy.

<div class="mt-4 text-sm opacity-80">
Secondary supporting note in smaller text.
</div>

</div>
</div>

</div>

---
glowSeed: 182
---

# Cards with Icon Headers + Nested Callout

`glass-card` and `accent-card` can nest a `callout-box` inside.

<div class="grid grid-cols-2 gap-8 mt-4">

<div v-click border="2 solid blue-800" bg="blue-800/20" rounded-lg overflow-hidden>
<div class="text-xs font-mono text-white/25 px-4 pt-2 tracking-wide">accent-card · blue · with icon-header + bullet list</div>
<div bg="blue-800/40" px-4 py-2 flex items-center gap-2>
<div i-carbon:user-speaker text-blue-300 text-xl />
<span font-bold>Card One</span>
</div>
<div px-5 py-4>

Main content paragraph:

- **Sub-point one** — explanation
- **Sub-point two** — explanation
- **Sub-point three** — explanation

<div class="mt-3 text-sm opacity-80">Footer note in smaller, dimmer text.</div>

</div>
</div>

<div v-click border="2 solid white/5" bg="white/5" backdrop-blur-sm rounded-lg overflow-hidden>
<div class="text-xs font-mono text-white/25 px-4 pt-2 tracking-wide">glass-card · with icon-header + callout-box</div>
<div bg="white/10" backdrop-blur px-4 py-2 flex items-center gap-2>
<div i-carbon:time text-amber-300 text-xl />
<span font-bold>Card Two</span>
</div>
<div px-5 py-4>

Main content paragraph.

<div class="mt-4" border="2 solid red-800" bg="red-800/20" rounded-lg px-4 py-3>
<span class="text-xs font-mono text-white/25 block mb-1 tracking-wide">callout-box · red</span>
⚠️ <strong>Warning or callout heading</strong><br/>
Detail text explaining the callout.
</div>

<div class="mt-3 text-sm opacity-80">Follow-up note after the callout.</div>

</div>
</div>

</div>

---
layout: center
class: text-center
glowSeed: 205
---

# Centered Highlight Slide

`layout: center` · `class: text-center` · items constrained with `max-w-4xl mx-auto`.

<div v-click class="text-2xl mt-4 mb-8">
<span class="text-xs font-mono text-white/25 block mb-2 tracking-wide">hero-text · teal highlight</span>
Big finding: <span class="text-teal-400 font-bold">highlighted result</span> in teal.
</div>

<div class="grid grid-cols-2 gap-8 max-w-4xl mx-auto text-left">

<div v-click border="2 solid amber-800" bg="amber-800/20" rounded-lg overflow-hidden>
<div class="text-xs font-mono text-white/25 px-4 pt-2 tracking-wide">accent-card · amber</div>
<div bg="amber-800/40" px-4 py-2 flex items-center gap-2>
<span text-xl>📦</span>
<span font-bold>Group A</span>
</div>
<div px-4 py-3>
Description of Group A's behavior or result.
</div>
</div>

<div v-click border="2 solid white/5" bg="white/5" backdrop-blur-sm rounded-lg overflow-hidden>
<div class="text-xs font-mono text-white/25 px-4 pt-2 tracking-wide">glass-card</div>
<div bg="white/10" backdrop-blur px-4 py-2 flex items-center gap-2>
<span text-xl>🎓</span>
<span font-bold>Group B</span>
</div>
<div px-4 py-3>
Description of Group B's behavior or result.
</div>
</div>

</div>

<div v-click class="mt-8 text-lg">
<span class="text-xs font-mono text-white/25 block mb-1 tracking-wide">closing-line</span>
Additional finding or implication that reinforces the headline above.
</div>

---
glowSeed: 310
---

# 2×3 Icon List Grid

Each cell is an `icon-list-item` — emoji + bold label + one-sentence description.

<div class="text-xs font-mono text-white/25 mb-4 tracking-wide">subheading · optional framing line</div>

<div class="grid grid-cols-2 gap-4">

<div v-click border="2 solid white/5" bg="white/5" backdrop-blur-sm rounded-lg flex gap-3 items-start px-4 py-3>
<div class="text-2xl">🤖</div>
<div>
<span class="text-xs font-mono text-white/25 block mb-1 tracking-wide">icon-list-item</span>
Item one — <strong>short bold label</strong> followed by one-sentence description.
</div>
</div>

<div v-click border="2 solid white/5" bg="white/5" backdrop-blur-sm rounded-lg flex gap-3 items-start px-4 py-3>
<div class="text-2xl">📋</div>
<div>
<span class="text-xs font-mono text-white/25 block mb-1 tracking-wide">icon-list-item</span>
Item two — <strong>short bold label</strong> followed by one-sentence description.
</div>
</div>

<div v-click border="2 solid white/5" bg="white/5" backdrop-blur-sm rounded-lg flex gap-3 items-start px-4 py-3>
<div class="text-2xl">📊</div>
<div>
<span class="text-xs font-mono text-white/25 block mb-1 tracking-wide">icon-list-item</span>
Item three — <strong>short bold label</strong> followed by one-sentence description.
</div>
</div>

<div v-click border="2 solid white/5" bg="white/5" backdrop-blur-sm rounded-lg flex gap-3 items-start px-4 py-3>
<div class="text-2xl">🔍</div>
<div>
<span class="text-xs font-mono text-white/25 block mb-1 tracking-wide">icon-list-item</span>
Item four — <strong>short bold label</strong> followed by one-sentence description.
</div>
</div>

<div v-click border="2 solid white/5" bg="white/5" backdrop-blur-sm rounded-lg flex gap-3 items-start px-4 py-3 min-h-20>
<div class="text-2xl">✅</div>
<div>
<span class="text-xs font-mono text-white/25 block mb-1 tracking-wide">icon-list-item</span>
Item five — <strong>short bold label</strong> followed by one-sentence description.
</div>
</div>

<div v-click border="2 solid white/5" bg="white/5" backdrop-blur-sm rounded-lg flex gap-3 items-start px-4 py-3 min-h-20>
<div class="text-2xl">🧑‍🏫</div>
<div>
<span class="text-xs font-mono text-white/25 block mb-1 tracking-wide">icon-list-item</span>
Item six — <strong>short bold label</strong> followed by one-sentence description.
</div>
</div>

</div>

---
layout: center
class: text-center
glowSeed: 150
---

# Conclusion — 3-Column Takeaway Cards

`layout: center` · cards use `takeaway-card` style — emoji, bold title, one sentence.

<div class="grid grid-cols-3 gap-6 max-w-5xl mx-auto mt-8 text-left">

<div v-click border="2 solid teal-800" bg="teal-800/20" rounded-lg px-6 py-5>
<div class="text-xs font-mono text-white/25 mb-2 tracking-wide">takeaway-card · teal</div>
<div class="text-3xl mb-2">⚖️</div>
<div class="font-bold mb-2">Takeaway One</div>
One sentence explaining the first takeaway.
</div>

<div v-click border="2 solid amber-800" bg="amber-800/20" rounded-lg px-6 py-5>
<div class="text-xs font-mono text-white/25 mb-2 tracking-wide">takeaway-card · amber</div>
<div class="text-3xl mb-2">📦</div>
<div class="font-bold mb-2">Takeaway Two</div>
One sentence explaining the second takeaway.
</div>

<div v-click border="2 solid violet-800" bg="violet-800/20" rounded-lg px-6 py-5>
<div class="text-xs font-mono text-white/25 mb-2 tracking-wide">takeaway-card · violet</div>
<div class="text-3xl mb-2">🗣️</div>
<div class="font-bold mb-2">Takeaway Three</div>
One sentence explaining the third takeaway.
</div>

</div>

<div v-click class="mt-10 text-lg opacity-90">
<span class="text-xs font-mono text-white/25 block mb-1 tracking-wide">closing-line</span>
Closing sentence that positions the work or points to next steps.
</div>

---
layout: center
class: text-center
glowSeed: 229
---

# end-slide

### `layout: center` · `class: text-center`

<div class="pt-6 opacity-80">
Your Name · Your Organization
</div>

<div class="pt-8 text-sm opacity-60">
Backup slides follow if applicable
</div>
