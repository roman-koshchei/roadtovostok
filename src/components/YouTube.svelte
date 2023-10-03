<script lang="ts">

  export let id: string 
  export let title: string 

  let hidden = true
  let load = false
</script>

{#if !load}
<button 
  class="absolute top-0 left-0 right-0 bottom-0 z-10 w-full h-full 
  grid place-content-center"   on:click={() => load = true}
>
  <svg class="w-16" version="1.1" viewBox="0 0 68 48" width="100%">
    <path  d="M66.52,7.74c-0.78-2.93-2.49-5.41-5.42-6.19C55.79,.13,34,0,34,0S12.21,.13,6.9,1.55 C3.97,2.33,2.27,4.81,1.48,7.74C0.06,13.05,0,24,0,24s0.06,10.95,1.48,16.26c0.78,2.93,2.49,5.41,5.42,6.19 C12.21,47.87,34,48,34,48s21.79-0.13,27.1-1.55c2.93-0.78,4.64-3.26,5.42-6.19C67.94,34.95,68,24,68,24S67.94,13.05,66.52,7.74z" fill="#f00"></path>
    <path d="M 45,24 27,14 27,34" fill="#fff"></path>
  </svg>
</button>
{:else}
<iframe on:load={() => hidden = false} 
  class="absolute top-0 left-0 right-0 bottom-0 z-10 w-full h-full"
  width={640}
  height={360}
  loading="lazy"
  src="https://www.youtube.com/embed/{id}?autoplay=1"
  title={title}
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
  allowfullscreen
></iframe>
{/if}