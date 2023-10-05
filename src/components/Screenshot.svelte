<script lang="ts">

  export let src: string
  let dialog: HTMLDialogElement
</script>

<button 
  class="hover:brightness-50 transition-all cursor-zoom-in" 
  on:click={() => dialog.showModal()}
>
  <slot/>
</button>

<dialog bind:this={dialog} on:click={() => dialog.close()}>
  <img src={src} alt=""/>
</dialog>
