<script lang="ts">
  export let id: string 
  export let title: string 

  let hidden = true
</script>

<iframe on:load={() => hidden = false} 
  class="absolute top-0 left-0 right-0 bottom-0 z-10 w-full h-full"
  width={640}
  height={360}
  loading="lazy"
  src="https://www.youtube.com/embed/{id}"
  title={title}
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
  allowfullscreen
></iframe>