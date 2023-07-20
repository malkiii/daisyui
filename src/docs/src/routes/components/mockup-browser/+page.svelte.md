---
title: Browser mockup
desc: Browser mockup shows a box that looks like a browser window.
published: true
---

<script>
  import Component from "@components/Component.svelte"
  import ClassTable from "@components/ClassTable.svelte"
  import { prefix } from '$lib/stores';
  import { replace } from '$lib/actions';
</script>

<ClassTable
data="{[
  { type:'component', class: 'mockup-browser', desc: 'Container element' },
]}"
/>

<Component title="browser mockup with border">
<div class="border mockup-browser border-base-300 w-full">
  <div class="toolbar">
    <div class="input border border-base-300">https://daisyui.com</div>
  </div>
  <div class="flex justify-center px-4 py-16 border-t border-base-300">Hello!</div>
</div>
<pre slot="html" use:replace={{ to: $prefix }}>{
`<div class="$$mockup-browser border border-base-300">
  <div class="toolbar">
    <div class="input border border-base-300">https://daisyui.com</div>
  </div>
  <div class="flex justify-center px-4 py-16 border-t border-base-300">Hello!</div>
</div>`
}</pre>
</Component>

<Component title="browser mockup with background color">
<div class="border mockup-browser bg-base-300 w-full">
  <div class="toolbar">
    <div class="input">https://daisyui.com</div>
  </div>
  <div class="flex justify-center px-4 py-16 bg-base-200">Hello!</div>
</div>
<pre slot="html" use:replace={{ to: $prefix }}>{
`<div class="$$mockup-browser border bg-base-300">
  <div class="toolbar">
    <div class="input">https://daisyui.com</div>
  </div>
  <div class="flex justify-center px-4 py-16 bg-base-200">Hello!</div>
</div>`
}</pre>
</Component>
